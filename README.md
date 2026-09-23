# Reference Dashboard Demo

完全独立的 Vue 3 + TypeScript Viewer SDK 接入示例，不引用 `twin-Meteor/src`。

```bash
pnpm install
pnpm dev
```

集成入口在 `src/App.vue`，Viewer Contract 与实时数据投影集中在 `src/useTwinDashboard.ts`。示例从 `public/zero-carbon-demo.twin.zip` 直接加载项目包。

SDK 离线安装方式：

```bash
pnpm add ./vendor/twin-studio-viewer-0.1.0.tgz
```
