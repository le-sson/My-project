# net-music

## 项目安装

1. 安装 vue3 运行环境
2. 安装项目依赖

```bash
yarn install
```

## 运行

```bash
yarn serve
```

## 格式化代码和提交规范

所有的代码规范、格式化规范、提交规范都使用[Alibaba/f2e-spec](https://github.com/alibaba/f2e-spec)

1. 分支新建

   - 正常维护项目新建分支应该放在 feature 目录下面，标明日期和负责人。开发完成后合并到 dev 分支。例如：

     > feature/(日期)-(开发者)-(任务) (e.g. feature/20201210-silk-featUserMessage)

   - 当线上出现问题需要紧急修复的时候,从 master 分支新建分支。测试完成直接合并线上
     > hotfix/(日期)-(开发者)-(任务) (e.g. hotfix/20201210-silk-featUserMessage)

2. 格式化代码

    ```bash
    yarn f2elint-fix
    ```

3. 提交代码规范

    |   type   | des                                                 |
    | :------: | :-------------------------------------------------- |
    |   feat   | 新增功能                                            |
    |   fix    | 修复 bug                                            |
    |   docs   | 修改文档                                            |
    | refactor | 代码重构，未新增任何功能和修复任何 bug              |
    |  build   | 改变构建流程，新增依赖库、工具等（e.g.webpack 修改) |
    |  style   | 仅仅修改了空格、缩进等，不改变代码逻辑              |
    |   perf   | 改善性能和体现的修改                                |
    |  chore   | 构建过程或辅助工具的变动                            |
    |   test   | 增加测试                                            |
    |    ci    | 自动化流程配置修改                                  |
    |  revert  | 回滚到上一个版本                                    |

    例如，当我们修复了某个 bug：

    ```git
    git commit -m 'fix(scope): fix ie6 margin bug'
    ```

    - fix 表示 commit 的类型。
    - scope 表示 作用的范围（可选）。
    - 冒号后 表示 commit 对应的信息。

## 项目目录
<!-- markdownlint-disable -->
├─document 项目文档（记录遇到的问题）  
├─public 静态资源，pwa 图标  
│ └─img  
│ └─icons  
├─src 项目代码  
│ ├─@types 第三方 ts 声明添加修正  
│ ├─api api 入口  
│ ├─assets 静态资源  
│ ├─components 公共组件  
│ │ └─template 组件模板  
│ ├─config 项目配置  
│ ├─router 路由  
│ │ └─modules 模块路由  
│ ├─store 状态管理  
│ │ └─modules 模块状态管理  
│ ├─style 样式文件  
│ ├─tool 工具文件  
│ │ ├─ajax http 请求  
│ │ ├─cookie cookie 操作  
│ │ └─utils 工具类  
│ └─views 页面组件  
│ ├─home 首页  
│ ├─login 登录  
│ └─notFound 404  
└─tests 测试模块
<!-- markdownlint-restore -->