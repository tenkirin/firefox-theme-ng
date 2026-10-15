# Publishing

Firefox Theme NG is published to the VS Code Marketplace by GitHub Actions. Pushing a `v*.*.*` tag runs `.github/workflows/publish.yml`. The workflow:

1. checks that the tag matches `version` in `package.json`,
2. packages the `.vsix` once,
3. publishes it to the **VS Code Marketplace**, skipping it if this version is
   already there, so a failed run can be re-run safely,
4. creates a GitHub Release with the `.vsix` attached and generated notes.

You can also start it by hand from **Actions → Publish → Run workflow**. A
manual run publishes the current `package.json` version but doesn't create a
release.

## One-time setup

**VS Code Marketplace token → repo secret `VSCE_PAT`**

1. The publisher `tenkirin` must exist at <https://marketplace.visualstudio.com/manage>.
2. Create a Personal Access Token in [Azure DevOps](https://dev.azure.com/tenkirin/_usersSettings/tokens)

**Add the secret** in GitHub under *Settings → Secrets and variables → Actions →
New repository secret*, or with the CLI:

```bash
gh secret set VSCE_PAT
```

## Release steps

```bash
git status                  # working tree must be clean
npx @vscode/vsce package    # optional: check that the VSIX builds
npm version patch           # or minor | major | 1.3.0: bumps version, commits, tags v1.2.5
git push --follow-tags      # pushing the tag triggers the publish workflow
```

Follow the run under the repo's **Actions** tab. The Marketplace usually shows
the new version within a few minutes, after verification.

## Manual fallback

If CI isn't available, publish from your machine.

### Setup (one time)

1. Install Node.js (current LTS). `vsce` runs through `npx`, so you don't need
   to install it globally.
2. Get a Marketplace PAT, as described in [One-time setup](#one-time-setup).
3. Log in so `vsce` stores the PAT locally:

   ```bash
   npx @vscode/vsce login tenkirin   # paste the PAT when prompted
   npx @vscode/vsce verify-pat tenkirin   # optional: check that the PAT works
   ```

### Pack

```bash
git status                         # working tree must be clean
npm version patch                  # or minor | major | 1.3.0: bumps version, commits, tags
npx @vscode/vsce package           # -> firefox-theme-ng-<version>.vsix
npx @vscode/vsce ls                # optional: list the files in the package
code --install-extension firefox-theme-ng-<version>.vsix   # optional: try it locally
```

### Publish

```bash
npx @vscode/vsce publish --packagePath firefox-theme-ng-<version>.vsix
git push --follow-tags
gh release create v<version> firefox-theme-ng-<version>.vsix --generate-notes   # optional
```

If the workflow is enabled, pushing the tag still starts it. It skips the
Marketplace, because the version is already there, and creates the GitHub
Release, so you can skip `gh release create`.
