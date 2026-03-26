# cmake-js-napi-template

一个基于 **Node-API（node-addon-api）+ CMake.js** 的原生模块开发模板，适用于快速构建跨平台的 `.node` 插件。

---

## ✨ 特性

* 使用 Node-API（ABI 稳定，跨 Node 版本）
* 基于 CMake 构建（比 binding.gyp 更灵活）
* 支持 Windows / Linux / macOS
* 可扩展为多架构（x86 / x64 / arm64）构建
* 简洁模板，开箱即用

---

## 📦 安装依赖

```bash
yarn install
```

---

## ⚙️ 配置说明

在使用前，请根据你的需求修改以下配置：

### 1️⃣ `package.json`

设置 N-API 版本（根据你的 Node 版本）：

```json
"binary": {
  "napi_versions": [8]
}
```

可通过以下命令查看：

```bash
node -p "process.versions.napi"
```

---

### 2️⃣ CMake / cmake-js 参数

根据需要调整：

* `runtime`（node / electron）
* `arch`（x64 / ia32 / arm64）

---

## 🚀 构建

```bash
yarn build
```
---

## 📁 项目结构

```txt
.
├── src/                # C++ 源码
├── CMakeLists.txt      # CMake 构建配置
├── package.json
├── out/                # 编译产物
└── build/              # CMake 中间文件
```

---

## 🧠 技术说明

* 使用 `node-addon-api`（C++ 封装）开发
* 通过 `cmake-js` 桥接 Node 和 CMake 构建系统

---