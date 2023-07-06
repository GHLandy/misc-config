# @ghlandy/eslint-config-prettier

## 使用

```bash
pnpm i -D @ghlandy/eslint-config-prettier eslint prettier
pnpm i -D eslint-config-prettier eslint-plugin-prettier
```

> 在 eslint 配置文件 (`.eslintrc.cjs` 或 `.eslintrc.js`) 中引入使用

```js
module.exports = {
  // ... 其他配置
  extends: [
    'eslint:recommended'
    // ... 其他配置
    '@ghlandy/eslint-config-prettier', // 放在最后
  ],
  // ... 其他配置
};
```

## 配置详细

```js
module.exports = {
  extends: ['plugin:prettier/recommended'],
  rules: {
    'prettier/prettier': 'warn',
  },
};
```

`plugin:prettier/recommended` 的实际作用如下：

```js
module.exports = {
  extends: ['prettier'],
  plugins: ['prettier'],
  rules: {
    'prettier/prettier': 'error',
    'arrow-body-style': 'off',
    'prefer-arrow-callback': 'off',
  },
};
```

设置规则 `prettier/prettier': 'warn'`，另外去设置保存自动 `prettier` 格式化或者 `pre-commit` 钩子去格式化即可

## 更多阅读

- [https://eslint.org/docs/latest/extend/shareable-configs](https://eslint.org/docs/latest/extend/shareable-configs)
- [https://github.com/prettier/eslint-plugin-prettier/#recommended-configuration](https://github.com/prettier/eslint-plugin-prettier/#recommended-configuration)

## License

[MIT](https://github.com/GHLandy/misc-config/blob/main/LICENSE.md)
