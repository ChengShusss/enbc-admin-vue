[D2Admin](https://github.com/d2-projects/d2-admin) is a fully open source and free enterprise back-end product front-end integration solution, using the latest front-end technology stack, javascript files loading of local first screen less than 60kb, has prepared most of the project preparations, and with a lot of sample code to help the management system agile development.

[中文](https://github.com/d2-projects/d2-admin-start-kit/blob/master/README.zh.md) | **English**

## Preview

![Deploy preview](https://github.com/d2-projects/d2-admin-start-kit/workflows/Deploy%20preview/badge.svg)
[![Netlify Status](https://api.netlify.com/api/v1/badges/08ff8c93-f0a8-497a-a081-440b31fb3aa4/deploy-status)](https://app.netlify.com/sites/d2-admin-start-kit/deploys)

The following access addresses are built and deployed by the latest master branch code at the same time. The access effect is completely consistent. Please select the appropriate access link according to your own network situation.

| server     | link                                                                                         | server       |
| ---------- | -------------------------------------------------------------------------------------------- | ------------ |
| d2.pub     | [d2.pub/d2-admin-start-kit/preview](https://d2.pub/d2-admin-start-kit/preview)               | China server |
| cdn.d2.pub | [cdn.d2.pub/d2-admin-start-kit/preview](https://cdn.d2.pub/d2-admin-start-kit/preview)       | qiniu CDN    |
| github     | [d2-projects.github.io/d2-admin-start-kit](https://d2-projects.github.io/d2-admin-start-kit) | GitHub pages |
| netlify    | [d2-admin-start-kit.netlify.com](https://d2-admin-start-kit.netlify.com)                     | Netlify CDN  |

## Other synchronous repositories

| type   | link                                                                                                                       |
| ------ | -------------------------------------------------------------------------------------------------------------------------- |
| gitee  | [https://gitee.com/d2-projects/d2-admin](https://gitee.com/d2-projects/d2-admin)                                           |
| coding | [https://d2-projects.coding.net/p/d2-projects/d/d2-admin/git](https://d2-projects.coding.net/p/d2-projects/d/d2-admin/git) |

## VS Code configuation

```
  "editor.defaultFormatter": "esbenp.prettier-vscode", //编辑器格式化工具
  "[vue]": {
    "editor.defaultFormatter": "octref.vetur"
  }, //vue格式化工具
  "editor.insertSpaces": false,
  "workbench.editor.enablePreview": false, //打开文件不覆盖
  "search.followSymlinks": false, //关闭rg.exe进程
  "editor.minimap.enabled": false, //关闭快速预览
  "editor.lineNumbers": "on", //开启行数提示
  "editor.quickSuggestions": {
    //开启自动显示建议
    "other": true,
    "comments": true,
    "strings": true
  },
  "editor.tabSize": 2, //制表符符号eslint
  "editor.formatOnSave": true, //每次保存自动格式化
  // "eslint.codeActionsOnSave": {
  //     "source.fixAll.eslint": true
  // },
  "prettier.semi": true, //去掉代码结尾的分号
  "prettier.singleQuote": false, //使用单引号替代双引号
  "javascript.format.insertSpaceBeforeFunctionParenthesis": true, //让函数(名)和后面的括号之间加个空格
  "vetur.format.defaultFormatter.html": "js-beautify-html", //格式化.vue中html
  "vetur.format.defaultFormatter.js": "vscode-typescript", //让vue中的js按编辑器自带的ts格式进行格式化
  "vetur.format.defaultFormatterOptions": {
    "js-beautify-html": {
      "wrap_attributes": "force-aligned" //属性强制折行对齐
    },
    "prettier": {
      "semi": false,
      "singleQuote": true
    },
    "vscode-typescript": {
      "semi": false,
      "singleQuote": true
    }
  },
  "eslint.validate": [
    "vue",
    // "javascript",
    "typescript",
    "typescriptreact",
    "html"
  ],
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  }
```
