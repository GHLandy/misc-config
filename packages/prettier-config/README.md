# @ghlandy/prettier-config

## 使用

```bash
pnpm i -D @ghlandy/prettier-config prettier@2
pnpm i -D prettier-plugin-organize-imports@3 typescript prettier-plugin-packagejson@2
pnpm i -D @volar/vue-typescript # 格式化 .vue 文件内的 import 时需要
```

> 在 prettier 配置文件 (`.prettierrc.cjs` 或 `.prettierrc.js`) 中引入使用

```js
const config = require('@ghlandy/prettier-config');

module.exports = {
  ...config,
};
```

## 配置详细

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

> `prettier-plugin-organize-imports` 自动排序 `import` (需要 `typescript` 依赖包)
>
> `.vue` 文件里边的自动排序 `import`，还需要按 `@volar/vue-typescript`
>
> `prettier-plugin-packagejson` 自动排序 JSON

## License

[MIT](https://github.com/GHLandy/misc-config/blob/main/LICENSE.md)
