# 环境笔记

## 1. 创建Vite项目

```bash
# 创建vite项目
yarn create vite front-demo

# 添加依赖
yarn

# 启动项目
yarn dev
```

## 2. 添加tailwindcss

```bash

# 安装依赖
yarn add -D tailwindcss@latest postcss@latest autoprefixer@latest

# or
npm install -D tailwindcss@latest postcss@latest autoprefixer@latest

# create tailwind.config.cjs and postcss.config.cjs file
npx tailwindcss init -p
```

`tailwind.config.cjs` 文件中的`content`部分添加 `"./src/**/*.{html,js}"`，使tailwindcss生效

## `src`目录下添加`input.css`, 内容如下：

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```
## start the Tailwind CLI build process
```bash
npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
```

# `main.ts`中引入`output.css`
```typescript
import './output.css'
```
