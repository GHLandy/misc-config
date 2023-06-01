# @ghlandy/prettier-config

## 安装及使用

```bash
pnpm i -D @ghlandy/prettier-config
```

> 在 prettier 配置文件 (`.prettierrc.cjs` 或 `.prettierrc.js`) 中引入使用

```js
const config = require('@ghlandy/prettier-config');

module.exports = {
  ...config,
};
```

## 本配置详细为

> 包含自动排序 import，自动排序 JSON 字段
> vue 里边的自动排序 import，还需要按 `@volar/vue-typescript`

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
  htmlWhitespaceSensitivity: 'ignore',
  vueIndentScriptAndStyle: false,
  endOfLine: 'lf',
  plugins: ['prettier-plugin-organize-imports', 'prettier-plugin-packagejson'],
};
```

## License

[MIT](https://github.com/GHLandy/misc-config/blob/main/LICENSE.md)
