# Miniprogram Template

📦 一个快速搭建「微信小程序」的模版！小程序端使用组件化开发框架 [WePY](https://github.com/Tencent/wepy)，后端使用微框架 [Flask](https://github.com/pallets/flask)。

## 使用方法

1. 点击本项目右上角的绿色按钮 `Use this template`（使用此模板），输入名称和说明，完成创建。

2. 将刚刚创建好的项目克隆到本地，这里以本项目为例，实际操作时这里需要替换你自己的项目。

    ```bash
    git clone https://github.com/HaveTwoBrush/miniprogram-template.git --depth 1
    ```

3. 安装环境依赖，本项目需要 Node 环境 和 Python 环境，如果对这部分不熟悉的看本文档最后的参考文章。

    ```bash
    # 小程序端环境依赖安装
    cd miniprogram
    yarn
    
    # 后端环境依赖安装
    cd back
    pip install -r requirements.txt
    ```

4. 打开两个终端，分别启动小程序端和后端。

    ```bash
    # 启动小程序端
    cd miniprogram
    yarn dev

    # 启动后端
    cd back
    python app.py
    ```

5. 使用「微信开发者工具」将 `miniprogram` 的目录导入进去即可预览。

6. 根据你的需求修改代码。

## 项目结构

```
.
├── LICENSE # 许可证
├── .gitignore
├── README.md
├── back
│   ├── app.py
│   └── requirements.txt # 后端依赖
└── miniprogram # 小程序端
    ├── .editorconfig
    ├── .eslintignore
    ├── .eslintrc.js
    ├── .gitignore
    ├── .prettierrc
    ├── .wepycache
    ├── .wepyignore
    ├── package.json # 前端依赖
    ├── project.config.json # 小程序项目配置
    ├── src
    │   ├── app.wpy
    │   ├── common
    │   │   └── eventHub.js
    │   ├── components
    │   │   ├── counter.wpy
    │   │   ├── group.wpy
    │   │   ├── groupitem.wpy
    │   │   ├── list.wpy
    │   │   ├── panel.wpy
    │   │   └── wepy-list.wpy
    │   ├── mixins
    │   │   └── test.js
    │   ├── pages
    │   │   └── index.wpy
    │   └── store
    │       └── index.js
    ├── wepy.config.js
    └── yarn.lock
```

## 附加

### 添加 iView UI

1. 下载 [iView Weapp](https://github.com/TalkingData/iview-weapp) 的代码，
将 `dist` 目录拷贝到 `miniprogram-template/miniprogram/src/` 下面。

2. 在要使用的 `*.wpy` 文件中引入配置，这里以 `button` 为例。

    ```html
    <config>
    {
        usingComponents: {
            "i-button": "../dist/button/index"
        }
    }
    </config>
    ```

3. 在 `html` 部分中可直接使用。

    ```html
    <i-button type="primary" bind:click="handleClick">这是一个按钮</i-button>
    ```

## 许可

[![](https://award.dovolopor.com?lt=License&rt=MIT&rbc=green)](./LICENSE)

## 参考

- [WePY document](https://wepyjs.github.io/wepy-docs/)
- [iView Weapp document](https://weapp.iviewui.com/)
- [Flask document](https://dormousehole.readthedocs.io/en/latest/)
- [如何安装 Node 开发环境？](https://v2ai.cn/linux/2018/11/11/LX-10.html)
- [如何安装 Python 开发环境？](https://v2ai.cn/linux/2018/04/29/LX-2.html)

## TODO

- [ ] 小程序端接口。