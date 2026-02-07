# Publishing Kraken VS Code Extension

## Prerequisites

1. **Install vsce** (VS Code Extension Manager):
```bash
npm install -g @vscode/vsce
```

2. **Create a Microsoft Account** (if you don't have one):
   - Go to https://login.live.com

3. **Create an Azure DevOps Organization**:
   - Go to https://dev.azure.com
   - Sign in with your Microsoft account
   - Create a new organization (e.g., "kraken-lang")

4. **Create a Personal Access Token (PAT)**:
   - Go to https://dev.azure.com/[your-org]/_usersSettings/tokens
   - Click "New Token"
   - Name: "VS Code Marketplace"
   - Organization: All accessible organizations
   - Scopes: Custom defined → Marketplace → **Manage**
   - Click "Create"
   - **SAVE THE TOKEN** - you won't see it again!

5. **Create a Publisher**:
```bash
vsce create-publisher jamesgober
# Enter your PAT when prompted
# Fill in display name, email, etc.
```

Or create via web:
- Go to https://marketplace.visualstudio.com/manage
- Click "Create publisher"
- Publisher ID: `jamesgober`
- Display name: `James Gober`

## Package the Extension

```bash
cd /Users/james/Development/Kraken/kraken-vscode

# Install dependencies (if any)
npm install

# Package the extension
vsce package

# This creates: kraken-lang-0.2.0.vsix
```

## Test Locally

```bash
# Install in VS Code
code --install-extension kraken-lang-0.2.0.vsix

# Test with a .kr file
# Verify syntax highlighting works
```

## Publish to Marketplace

```bash
# Login (one-time)
vsce login jamesgober
# Enter your PAT

# Publish
vsce publish

# Or publish with version bump
vsce publish patch  # 0.1.0 -> 0.1.1
vsce publish minor  # 0.1.0 -> 0.2.0
vsce publish major  # 0.1.0 -> 1.0.0
```

## Update Extension

After making changes:

```bash
# Update version in package.json
# Publish update
vsce publish patch
```

## Unpublish (if needed)

```bash
vsce unpublish jamesgober.kraken-lang
```

## Important Files Checklist

Before publishing, ensure you have:

- [x] `package.json` - Extension manifest
- [x] `README.md` - Extension documentation
- [x] `LICENSE` - License file (Apache-2.0)
- [x] `syntaxes/kraken.tmLanguage.json` - Syntax grammar
- [x] `language-configuration.json` - Language config
- [x] `snippets/kraken.json` - Code snippets
- [ ] `images/icon.png` - Extension icon (128x128 PNG)
- [ ] `images/file-icon.svg` - File icon (optional)
- [x] `.vscodeignore` - Files to exclude from package

## Create Icon (Optional but Recommended)

Create a 128x128 PNG icon and save as `images/icon.png`.

You can use the Kraken logo or create a simple icon with:
- Background color
- "Kr" or "Kraken" text
- Simple graphic

## Marketplace Page

After publishing, your extension will be at:
```
https://marketplace.visualstudio.com/items?itemName=jamesgober.kraken-lang
```

Users can install with:
```bash
code --install-extension jamesgober.kraken-lang
```

## Tips

1. **Version Control**: Commit everything before publishing
2. **Test Thoroughly**: Test on multiple files before publishing
3. **Icon**: A good icon makes your extension more discoverable
4. **Keywords**: Use relevant keywords in package.json
5. **Screenshots**: Add screenshots to README for better presentation
6. **Updates**: Keep the extension updated with language changes

## Troubleshooting

### "Publisher not found"
```bash
vsce login jamesgober
# Re-enter your PAT
```

### "Missing icon"
- Add `images/icon.png` (128x128)
- Or remove icon reference from package.json

### "Validation failed"
- Check package.json for errors
- Ensure all referenced files exist
- Run `vsce package` to see specific errors

## Resources

- [VS Code Extension API](https://code.visualstudio.com/api)
- [Publishing Extensions](https://code.visualstudio.com/api/working-with-extensions/publishing-extension)
- [Extension Manifest](https://code.visualstudio.com/api/references/extension-manifest)
- [Marketplace](https://marketplace.visualstudio.com/vscode)
