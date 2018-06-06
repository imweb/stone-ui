# Stone UI Components

## 运行指南

```js
// 先安装
tnpm i

// 然后执行
npm run dev
```

最后打开`http://localhost:6060/` 即可看到组件demo

## 创建组件

可以使用[generator-stone-component](https://github.com/imweb/generator-stone-component)脚手架来创建组件

先全局安装 `yo` 和 `generator-stone-component`
```bash
npm install -g yo
npm install -g generator-stone-component
```

然后运行命令
```
yo stone-component
```

根据交互提示输入组件名字及描述，注意组件名为首字母大写的驼峰格式 `/^[A-Z][a-zA-Z]*$/`

创建成功后，生成的组件可在 `src/components` 目录中看到。

## 组件预览

注：由于 DEMO 中左侧的菜单现在是按分类罗列的，所以现在需要手动把自己写的组件添加进根目录`styleguide.config.js`配置文件的相应分类中。

组件 DEMO 是调用组件中的 readme 文件进行渲染的，编辑比较简单，可参考已有例子，或[官方文档](https://react-styleguidist.js.org/docs/documenting.html)，如有疑问请询问ycxu

## 使用组件

每个包名字前面会有一个`stone-`前缀，使用 tnpm 安装，所有大写字母转成小写，使用`-`连接，如安装 `RadioCheckbox` 组件：

```js
tnpm i @tencent/stone-radio-checkbox
```

有些组件默认并没有导出，如 Table，默认导出的只有 Table 组件，其他的使用需要到 HOC 目录去引入，如需要使用排序，则

```js
import Table from '@tencent/stone-table';
import { tableSort } from '@tencent/stone-table/HOC';

const TableSort = tableSort(Table);
```

具体每个组件的目录，在组件 demo 预览中可见路径。

## 设计特色

- 单包管理多包，每个 component 都可以单独引用
- 组件通过 readme 文件直接生成 demo， 且可在线编辑
- eslint, sytlelint 验证，commit 的时候会验证
- PostCSS

## 使用技术

- [lerna](https://github.com/lerna/lerna)：多包管理
- [react styleguide](https://github.com/styleguidist/react-styleguidist)：负责组件 demo 生成

## FAQ

- [如何编写 readme](https://react-styleguidist.js.org/docs/documenting.html#writing-code-examples)
- [props 属性说明](Code comments and propTypes)
- [readme 与 example 关系](https://react-styleguidist.js.org/docs/documenting.html#usage-examples-and-readme-files)
- [react styleguidist 官方入门实例](https://github.com/styleguidist/react-styleguidist/tree/master/examples/basic)
