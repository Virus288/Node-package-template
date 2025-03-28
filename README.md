# Node package template

This project is template for building npm packages. This repo is written in esm, with rollup config for commonjs support.

## How to build

As mentioned previously, this package natively is written for esm, but does support commonjs. In order to build code, simply run

```shell
npm run build / yarn build
```

In order to build for commonjs, first make sure that you build the code first. Then run 


```shell
npm run build:common
```

> [!TIP]
> `build:watch` does not recompile code on change to commonjs. You need to manually build for commonjs.

If you even encounter strange build behavior, tsconfig is set to create build with cache. Set option `incremental` in tsConfig to false. In addition to that, remove `tsconfig.tsbuildinfo`, which contains cached information about build
