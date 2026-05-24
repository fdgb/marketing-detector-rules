# 营销号鉴别器 - 远程规则仓库

营销号鉴别器浏览器扩展的远程规则托管仓库，通过 GitHub Pages 提供规则热更新。

## 使用方式

扩展会自动从本仓库拉取最新 `rules.json`，无需重新安装。

### 规则端点

```
https://<YOUR_USERNAME>.github.io/marketing-detector-rules/rules.json
```

## 更新规则

1. 编辑 `rules.json`，递增 `version` 字段
2. 更新 `updatedAt` 为当前时间
3. 填写 `changelog` 说明本次变更
4. Push 到 main 分支，GitHub Pages 自动部署

## 规则结构

| 字段 | 说明 |
|------|------|
| `version` | 规则版本号，整数递增 |
| `updatedAt` | ISO 8601 更新时间 |
| `changelog` | 变更日志 |
| `bilibili` | B站特定规则（广告参数等） |
| `accountNamePatterns` | 账号名匹配模式 |
| `titlePatterns` | 标题匹配模式 |
| `contentPatterns` | 内容特征匹配 |
| `dataAnomaly` | 数据异常阈值 |
| `weights` | 各信号权重 |
| `thresholds` | 风险等级阈值（high/medium） |

## 状态页

访问 `https://<YOUR_USERNAME>.github.io/marketing-detector-rules/` 可查看规则服务状态。

## License

MIT
