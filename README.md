---
marp: true
---

# Make your own extensions for vscode.dev!

This whole slideshow is on vscode.dev right now!


----

## If you only remember one thing: [Web Extension Guide](https://code.visualstudio.com/api/extension-guides/web-extensions)


---

## Not so different from normal extensions

----

### Breakdown of the differences
<br>

| Normal extension | Web extension |
|--------------|-----------|
| Can be bundled or not.  | Needs to be bundled into 1 JavaScript file. |
| Has a `main` in its `package.json` | Has `browser` in its `package.json` |
| Can use node libraries like `fs` or `path` | Needs web compliant alternatives like `path-browserify` |
| Can use `fs` for accessing files | Use VS Code's [`FileSystemProvider`](https://github.com/microsoft/vscode/blob/fc41c9fb60ccb9d9aaa2c62165ed979d69256adc/src/vs/vscode.d.ts#L7190) instead to access files. |