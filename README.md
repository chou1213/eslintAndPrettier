```json
{
  "editor.defaultFormatter": "esbenp.prettier-vscode", // 设置默认格式化工具为 prettier
  "editor.formatOnSave": true, // 保存的时候自动格式化
  "editor.codeActionsOnSave": {
    "source.fixAll": true,
    "source.fixAll.eslint": true
  }
}
```

这个配置，在 vscode 保存后，看到自动格式化后，index.js 依然有 eslint 报错信息。这是用 prettier 格式化后导致和 eslint 配置有冲突。

```json
{
  // "editor.defaultFormatter": "esbenp.prettier-vscode", // 设置默认格式化工具为 prettier
  "editor.formatOnSave": true, // 保存的时候自动格式化
  "editor.codeActionsOnSave": {
    "source.fixAll": true,
    "source.fixAll.eslint": true
  }
}
```

这个配置，去掉 prettier 格式化配置，vscode 保存后，看到自动格式化后，index.js 没有了 eslint 报错信息。这是直接用 eslint fix 错误。
