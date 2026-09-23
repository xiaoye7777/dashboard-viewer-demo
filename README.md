# Reference Dashboard Demo

运行环境：Node.js `20.16.0+`、pnpm `10.20.0`。

完全独立的 Vue 3 + TypeScript Viewer SDK 接入示例，不引用 `twin-Meteor/src`。

```bash
pnpm install
pnpm data-server
pnpm dev
```

集成入口在 `src/App.vue`，Viewer Contract 与实时数据投影集中在 `src/useTwinDashboard.ts`。示例从 `public/zero-carbon-demo.twin.zip` 直接加载项目包。

SDK 离线安装方式：

```bash
pnpm add ./vendor/twin-studio-viewer-0.1.2.tgz
```

页面可在 `Mock` 与 `WebSocket` 间切换。WebSocket 测试服务默认监听
`ws://127.0.0.1:8787/realtime`，连接数可通过
`http://127.0.0.1:8787/status` 查看。可用 `VITE_TWIN_WS_URL` 覆盖地址。

测试服务每秒发送 8 个储能柜的 JSON 数据；ESS-003 会周期性进入 `75℃ / alarm=true`，用于验证外部网络数据触发项目包内 Visual Rule 与 3D Effect。
