## Comentários
```cs
# Comentar:
➡️ CTRL + k + c

# Descomentar:
➡️ CTRL + k + u

# uma linha
// uma linha
/* muitas linhas */

SHIFT + ALT + DOWN -> Duplicar para baixo
SHIFT + ALT + UP -> Duplicar para cima
```

## Debugar
```powershell
# Abrir Box
➡️ CTRL + SHIFT + D

# Depurar
➡️ F5

👉 # Obs.: No topo tem um console com todos os botões do Debug
```

## Vs Code ligaduras
```powershell
💻 File ➜ Preferences ➜ Settings
	➜ Text Editor
		┕ Font
			┕ Font Ligatures
				┕ Edit in settings.json
```
CTRL + SHIFT + P ➜ `settings.json`
```json
{
	"[dart]": {
		"editor.formatOnSave": true,
		"editor.formatOnType": true,
		"editor.rulers": [
			80
		],
		"editor.selectionHighlight": false,
		"editor.suggest.snippetsPreventQuickSuggestions": false,
		"editor.suggestSelection": "first",
		"editor.tabCompletion": "onlySnippets",
		"editor.wordBasedSuggestions": false,
		"editor.tabSize": 4,
		"editor.insertSpaces": false,
		"editor.detectIndentation": false,
		"editor.wrappingIndent": "deepIndent",
		"editor.autoIndent": "full"
	},
    "editor.minimap.enabled": false,
	"editor.fontLigatures": true,
	"editor.fontFamily": "'Victor Mono ExtraLight', Consolas, 'Courier New', monospace",
	"editor.fontSize": 20,
	"editor.tabSize": 4,
    "editor.insertSpaces": false,
    "editor.detectIndentation": false,
    "editor.wrappingIndent": "deepIndent",
	"editor.autoIndent": "full",
	"dart.enableSdkFormatter": false,
	"workbench.colorTheme": "Dracula Soft",
	"workbench.productIconTheme": "material-product-icons",
	"terminal.integrated.fontFamily": "'Victor Mono ExtraLight', Consolas, 'Courier New', monospace",
	"terminal.integrated.fontSize": 18,
	"workbench.iconTheme": "simple-icons",
	"explorer.confirmDelete": false,
	"window.menuBarVisibility": "compact",
	"javascript.updateImportsOnFileMove.enabled": "always",
	"oneDarkPro.bold": true,
	"oneDarkPro.editorTheme": "One Dark Pro Darker",
	"security.workspace.trust.untrustedFiles": "open",
	"markdown-preview-enhanced.previewTheme": "github-dark.css"
}
```