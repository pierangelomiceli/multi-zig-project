
# ⚡ Zig + VS Code Multi-Project Debug Setup

This repository is a **starter template** for working with **multiple Zig projects** in a single workspace using **VS Code**, with:

- ✅ A single `tasks.json`
- ✅ A single `launch.json`
- ✅ Dynamic project selection at debug/build time (via input dropdown)
- ✅ LLDB debugger support
- ✅ No scripts, no `.env`, no bash tricks

---

## 📁 Project structure

```
multi-zig-project/
├── project1/
│   ├── src/
│   └── build.zig
├── project2/
│   ├── src/
│   └── build.zig
└── .vscode/
    ├── tasks.json
    └── launch.json
```

---

## 🧠 How it works

When you press ▶️ **Run and Debug** in VS Code or press F5 key:

1. You're prompted to pick the project (`project1` or `project2`) to debug
1. You're prompted to pick the project (`project1` or `project2`) to build
3. The correct `zig build` command runs automatically in the right folder
4. The debugger starts the corresponding executable from `zig-out/bin/`
5. You have full step-debugging and breakpoints with **LLDB**

All this is handled using **VS Code's built-in `inputs` API**, so:

- No external files
- No shell scripts
- No hardcoded paths

---

## 🚀 How to use it

1. Open the workspace in VS Code
2. Place a breakpoint on project1 or project2 `main.zig` files.
3. Press `F5` to Debug 
4. you'll be prompted to pick a project to Debug
5. you'll be prompted to pick a project for pre-build

---

## 🛠 Requirements

- [Zig](https://ziglang.org/download/)
- [VS Code](https://code.visualstudio.com/)
- [CodeLLDB Extension](https://marketplace.visualstudio.com/items?itemName=vadimcn.vscode-lldb)

---

## 📚 Why this setup?

Zig doesn't yet have a built-in package manager or multi-project workflow like `cargo` in Rust.  
This setup gives you:

- Clean structure
- One config for all projects
- Less duplication
- Fully native integration with VS Code

---

Fully working with breakpoint on vscode.

## 💡 Inspired by

This was built out of necessity — because we were tired of repeating configurations on `launch.json` and `tasks.json` files during my learning experiments. 
Hope it helps others looking for a clean Zig + VS Code workflow!

---

## 📦 License

MIT – Free to use, modify, fork, or scream at.