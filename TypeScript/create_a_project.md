# 创建 TypeScript 版本 Vue 项目

> 说明：针对 `@vue/cli` 3.x 版本。

## 1 安装 @vue/cli

Vue CLI 需要 8.9 或以上版本的 [Node.js](https://nodejs.org/en/) 环境（推荐 8.11.0+）。在同一个机器上可使用 [nvm](https://github.com/creationix/nvm) 或 [nvm-windows](https://github.com/coreybutler/nvm-windows) 来管理多个 Node 版本。

```bash
npm install -g @vue/cli
# 或
yarn global add @vue/cli
```

检查版本并查看是否安装成功：

```bash
vue --version
```

## 2 创建项目

```bash
vue create your-project-name
```

选择 `Manually select features`，勾选 `TypeScript`，选择 `Y`，选择 `Y`，选择 `TSLint`，剩余的按实际情况勾选。