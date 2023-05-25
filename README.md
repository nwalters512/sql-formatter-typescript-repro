# sql-formatter-typescript-repro

This repository reproduces an issue with the TypeScript types for the `sql-formatter` package.

## Reproduction steps

- Clone repository
- Run `yarn`
- Run `yarn build`
- Observe the following error:

```
src/index.ts:1:24 - error TS1479: The current file is a CommonJS module whose imports will produce 'require' calls; however, the referenced file is an ECMAScript module and cannot be imported with 'require'. Consider writing a dynamic 'import("sql-formatter")' call instead.
  To convert this file to an ECMAScript module, change its file extension to '.mts', or add the field `"type": "module"` to '/Users/nathan/git/sql-formatter-typescript-repro/package.json'.

1 import { format } from 'sql-formatter';
                         ~~~~~~~~~~~~~~~


Found 1 error in src/index.ts:1
```
