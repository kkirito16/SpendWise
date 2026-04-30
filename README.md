# SpendWise

SpendWise 是一款基于 **React Native** 的本地个人记账与债务管理应用：日常支出、分类、多币种、报表与借贷记录均保存在设备本地（Realm），不依赖云端账号。

## 技术栈

- React Native 0.72、React 18、TypeScript
- 导航：React Navigation（Stack + Bottom Tabs）
- 状态：Redux Toolkit + Redux-Saga
- 本地数据：Realm
- 其他：AsyncStorage、Zod 校验、图表（react-native-svg-charts）等

## 环境要求

- Node.js ≥ 16
- JDK 17（与 Android Gradle 插件要求一致即可）
- Android Studio（含 Android SDK、平台工具、模拟器或真机 USB 调试）

## 安装与运行

```bash
yarn install
# 终端 1：Metro
yarn start
# 终端 2：安装到设备/模拟器
yarn android
```

也可在 **Android Studio** 中打开项目下的 `android` 目录，同步 Gradle 后选择 `app` 运行；首次仍需在项目根目录执行 `yarn start` 以启动 Metro，或在 Run 配置中按需指定 bundler（与团队习惯一致即可）。

## 应用标识

- **JS 注册名 / 显示名**：`SpendWise`（见 `app.json`）
- **Android applicationId / namespace**：`com.spendwise`

## 常用脚本

| 命令           | 说明                      |
| -------------- | ------------------------- |
| `yarn start`   | 启动 Metro 打包服务       |
| `yarn android` | 构建并安装 Android 调试包 |
| `yarn test`    | 运行 Jest 测试            |
| `yarn lint`    | ESLint 检查               |

## 目录结构（摘要）

- `src/screens`：各业务页面
- `src/components`：原子/分子组件
- `src/redux`：全局状态与 saga
- `src/services`、`src/schemas`：Realm 与数据模型
- `assets`：字体、图片与默认 JSON 数据
- `android`：Android 原生工程
