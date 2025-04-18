## eslint-js简介@about

<!--
keyword: 语法校验,语法检查,eslint
-->

eslint-js, 用于校验js和html中的js代码

[eslint-js插件安装地址](https://ext.dcloud.net.cn/plugin?id=2037)

## 错误提示

如下图所示，当检查到错误时，会出现红色波浪线

<img src="/static/snapshots/tutorial/plugins/eslint-js-error.png" class="hd-img" />

## 插件配置

点击菜单【工具】【设置 -> 插件配置】【eslint-js】，即可看到eslint-js相关配置。

<img src="/static/snapshots/tutorial/eslint/eslint-js.png" />

**实时校验、自动修复**

> HBuilderX 2.6.8+版本起，新增eslint 实时校验、自动修复错误的功能。注意：此功能不适用于2.6.8之前的版本

1. 使用此功能，必须安装[eslint-js](https://ext.dcloud.net.cn/plugin?id=2037)插件
2. `vue-cli`项目，需要安装eslint库，并配置eslint规则.
3. 若满足上述条件，当编写完代码，保存时，若代码中存在错误，自动修复;
4. 实时校验功能，默认未开启，需要手动开启此功能


## eslint-js插件配置文件

eslint-js的配置文件为.eslintrc.js。
点击菜单工具 -> 插件配置 -> eslint-js -> .eslintrc.js，即可打开.eslintrc.js文件。

选项对应说明如下：

```js
module.exports = {
    "plugins": [],          //插件
    "env": {
        "browser": true,
        "node": true
    },
    "parser": "esprima",    //指定解析器
    "parserOptions": {},
    "rules": {}             //规则
}
```

更多配置说明可以参考[options](https://cn.eslint.org/docs/user-guide/configuring)

## 如何增加规则?

[官方规则列表https://cn.eslint.org/docs/rules/](https://cn.eslint.org/docs/rules/)

规则设置：
- "off" 或 0 - 关闭规则
- "warn" 或 1 - 开启规则，使用警告级别的错误：warn (不会导致程序退出)
- "error" 或 2 - 开启规则，使用错误级别的错误：error (当被触发的时候，程序会退出)

规则示例
```js
"rules": {
  "camelcase": 2,           //强制驼峰法命名,
  "indent": [2, 4],         //缩进风格
  "id-match": 0,            //命名检测
  "init-declarations": 1,   //声明时必须赋初值
  "no-undef": 1,            //不能有未定义的变量
}
```


## 示例：普通web项目

使用eslint, 校验多余的空格，并自动修复

<img src="/static/snapshots/tutorial/plugins/eslint-html-example.gif" style="zoom: 90%; border: 1px solid #eee;" />

配置文件

```js
module.exports = {
    "plugins": [
        "html"
    ],
    "parserOptions": {
        "ecmaVersion": "latest",
        "sourceType": "module",
        "ecmaFeatures": {
            "jsx": true
        },
        "allowImportExportEverywhere": false
    },
    rules: {
        "no-alert": 0,
        "semi": [2, "always"],
        "no-multi-spaces": "error",
       "quotes": ["error", "single"]
    }
}
```

## 示例：uni-app项目

特别说明：
- vue文件，校验vue语法，需要安装`eslint-vue`插件，[插件地址](https://ext.dcloud.net.cn/plugin?id=2005)
- vue文件, 校验规则，需要从`eslint-vue`插件中配置。
- 菜单【工具】->【设置 -> 插件配置 -> eslint-vue -> .eslintrc.js】,编辑`.eslintrc.js`文件

【示例】eslint自动修复双引号为单引号，如下：

<img src="/static/snapshots/tutorial/eslint/eslint-uniapp-example.gif" style="zoom: 90%; border: 1px solid #eee;" />


## 示例：vue-cli项目

vue-cli项目，如果使用项目下的配置规则，需要安装`相关库`、并在项目根目录创建`.eslintrc.js`文件

备注：
1. 注意：项目下`eslint规则`会覆盖HBuilderX编辑器`eslint插件中的规则`
2. 校验vue语法，需要安装`eslint-vue`插件，[插件地址](https://ext.dcloud.net.cn/plugin?id=2005)

```shell
npm install --save eslint eslint-plugin-vue eslint-plugin-html eslint-config-standard eslint-plugin-import eslint-plugin-node eslint-plugin-promise eslint-plugin-standard babel-eslint
```


.eslintrc.js配置文件示例

```js
module.exports = {
    extends: [
        'plugin:vue/recommended'
    ],
	parserOptions: {
		'ecmaVersion': "latest",
		'sourceType': 'module',
		'ecmaFeatures': {
			'jsx': true
		},
		'allowImportExportEverywhere': false
	},
    rules: {
        "no-alert": 0,
        "no-multi-spaces": "error", // 禁止多个空格
        "semi": [2, "always"] ,// 自动补充分号
       "quotes": ["error", "single"] // 使用单引号
    }
}
```

示例：使用eslint, 自动补充分号

![](https://img-cdn-qiniu.dcloud.net.cn/uploads/article/20200317/911ea4cac9f2c4d80ec502b1384e7a58.gif)
