# @ghlandy/prettier-config

## 安装及使用

```bash
pnpm i -D @ghlandy/prettier-config
```

> 在 prettier 配置文件中引入使用 `.prettierrc.js`

```js
const config = require('@ghlandy/prettier-config');

module.exports = {
  ...config,
};
```

## 本配置详细为

> 包含自动排序导入的包，自动排序 JSON 字段

```js
module.exports = {
  printWidth: 100,
  tabWidth: 2,
  useTabs: false,
  semi: true,
  singleQuote: true,
  quoteProps: 'as-needed',
  jsxSingleQuote: false,
  trailingComma: 'all',
  bracketSpacing: true,
  bracketSameLine: false,
  arrowParens: 'always',
  vueIndentScriptAndStyle: false,
  endOfLine: 'lf',
  plugins: ['prettier-plugin-organize-imports', 'prettier-plugin-packagejson'],
};
```

## License

[MIT](../../LICENSE.md)
