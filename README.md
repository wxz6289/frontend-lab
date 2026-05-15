# frontend-lab

聚合本地目录 **`~/learn`** 下前端相关学习项目，以 **Git 子模块** 方式统一到本仓库；各子模块远程为 **`wxz6289/*`**。

本地工作区对应路径：`~/learn` 下各同名目录；本仓库路径：`~/frontend-lab`。

## 子模块一览

| 路径 | 远程仓库 | 说明 |
|------|----------|------|
| `frontend-interview/` | [`wxz6289/frontend-interview`](https://github.com/wxz6289/frontend-interview) | 前端面试题与资料 |
| `html-css/` | [`wxz6289/learn-html`](https://github.com/wxz6289/learn-html) | HTML / CSS 学习 |
| `js/` | [`wxz6289/js`](https://github.com/wxz6289/js) | JavaScript 学习 |
| `typescript/` | [`wxz6289/learn-typescript`](https://github.com/wxz6289/learn-typescript) | TypeScript 学习 |
| `react/` | [`wxz6289/react`](https://github.com/wxz6289/react) | React 示例 |
| `vue/` | [`wxz6289/vue`](https://github.com/wxz6289/vue) | Vue 示例 |
| `next/` | [`wxz6289/next`](https://github.com/wxz6289/next) | Next.js 示例 |
| `nuxt/` | [`wxz6289/nuxtjs`](https://github.com/wxz6289/nuxtjs) | Nuxt 示例 |
| `webpack/` | [`wxz6289/webpack`](https://github.com/wxz6289/webpack) | Webpack 学习 |
| `vite/` | [`wxz6289/vite`](https://github.com/wxz6289/vite) | Vite 学习 |
| `electron/` | [`wxz6289/electron`](https://github.com/wxz6289/electron) | Electron 桌面端 |
| `tauri/` | [`wxz6289/tauri`](https://github.com/wxz6289/tauri) | Tauri 桌面端 |
| `threejs/` | [`wxz6289/threejs`](https://github.com/wxz6289/threejs) | Three.js 3D |
| `rxjs/` | [`wxz6289/rxjs`](https://github.com/wxz6289/rxjs) | RxJS 响应式 |
| `uniapp/` | [`wxz6289/uni-app`](https://github.com/wxz6289/uni-app) | uni-app 跨端 |
| `flutter/` | [`wxz6289/flutter`](https://github.com/wxz6289/flutter) | Flutter 跨端（`learn/fultter`） |
| `admin/` | [`wxz6289/admin`](https://github.com/wxz6289/admin) | 管理后台示例 |
| `learn-qiankun/` | [`wxz6289/learn-qiankun`](https://github.com/wxz6289/learn-qiankun) | qiankun 微前端 |

## 克隆

```bash
git clone --recurse-submodules git@github.com:wxz6289/frontend-lab.git
cd frontend-lab
```

已克隆父仓、子模块为空时：

```bash
git submodule update --init --recursive
```

## 在子模块中开发

```bash
cd react   # 任选子模块目录
git checkout main   # 或该仓库的默认分支
# 修改、提交、推送到子模块自己的远程
git add -A && git commit -m "feat: ..." && git push origin HEAD
# 回到父仓更新指针
cd ..
git add react && git commit -m "chore: bump react submodule" && git push
```

父仓只记录各子模块的 **commit SHA**；日常改代码在对应子仓库完成。

### 体积较大的子模块

`threejs/` 对应远程仓库体积较大，首次 `git submodule update --init threejs` 可能耗时较久，可单独执行、耐心等待；网络不稳定时可重试同一命令。
