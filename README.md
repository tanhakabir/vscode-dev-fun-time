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
| Same with no code/no `main` | Same with no code/no `main` |
| Can be bundled or not.  | Needs to be bundled into 1 JavaScript file. |
| Has a `main` in its `package.json` | Has `browser` in its `package.json` |
| Can use node libraries like `fs` or `path` | Needs web compliant alternatives like `path-browserify` |
| Can use `fs` for accessing files | Use VS Code's [`FileSystemProvider`](https://github.com/microsoft/vscode/blob/fc41c9fb60ccb9d9aaa2c62165ed979d69256adc/src/vs/vscode.d.ts#L7190) instead to access files. |

----

#### Sample changes made to popular extensions
<br>

| Extension| Pull Request |
|--------------|-----------|
|[Indent Rainbow](https://marketplace.visualstudio.com/items?itemName=oderwat.indent-rainbow) | [vscode-indent-rainbow#114](https://github.com/oderwat/vscode-indent-rainbow/pull/114) |
| [Color Highlight](https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight) | [vscode-ext-color-highlight#148](https://github.com/enyancc/vscode-ext-color-highlight/pull/148) |
| [Peacock](https://marketplace.visualstudio.com/items?itemName=johnpapa.vscode-peacock) | [vscode-peacock#461](https://github.com/johnpapa/vscode-peacock/pull/461) |
| [OneDark Pro Theme](https://marketplace.visualstudio.com/items?itemName=zhuangtongfa.Material-theme) | [OneDark-Pro#601](https://github.com/Binaryify/OneDark-Pro/pull/601) |
| [YAML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml) | [vscode-yaml#594](https://github.com/redhat-developer/vscode-yaml/pull/594) |
| [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) | [prettier-vscode#2180](https://github.com/prettier/prettier-vscode/pull/2180) |