# Miniprogram Template

📦 一个快速搭建「微信小程序」的模版！

## 使用方法

1. 点击本项目右上角的绿色按钮 `Use this template`（使用此模板），输入名称和说明，完成创建。

2. 将刚刚创建好的项目克隆到本地，这里以本项目为例，实际操作时这里需要替换你自己的项目。

    ```bash
    git clone https://github.com/Ailln/miniprogram-template.git --depth 1
    ```

3. 安装环境依赖，启动后端。(本项目需要 Python 环境，如果对这部分不熟悉的看最后的参考文章)

    ```bash
    # 后端环境依赖安装
    cd back
    pip install -r requirements.txt

    # 启动后端
    python app.py
    ```

4. 使用「微信开发者工具」将 `miniprogram` 的目录导入进去即可预览。

5. 根据你的需求修改代码。

## 项目结构

```
.
├── LICENSE
├── README.md
├── back
│   ├── app.py
│   └── requirements.txt
└── miniprogram
    ├── app.js
    ├── app.json
    ├── app.wxss
    ├── pages
    │   ├── index
    │   │   ├── index.js
    │   │   ├── index.json
    │   │   ├── index.wxml
    │   │   └── index.wxss
    │   └── logs
    │       ├── logs.js
    │       ├── logs.json
    │       ├── logs.wxml
    │       └── logs.wxss
    ├── project.config.json
    ├── sitemap.json
    └── utils
        └── util.js
```

## 附加

### 添加 WeUI

1. 下载 [weui-wxss](https://github.com/Tencent/weui-wxss) 的代码，
将 `dist` 目录拷贝到 `miniprogram-template/miniprogram/` 下面。

2. 在 `app.wxss` 中全局引入，在第一行添加：

    ```css
    @import "./dist/style/weui.wxss";
    ```

3. 在wxml 中使用样式：

    ```html
    <button class="weui-btn" type="primary">页面主操作</button>
    ```

### 添加 iView Weapp

1. 下载 [iView Weapp](https://github.com/TalkingData/iview-weapp) 的代码，
将 `dist` 目录拷贝到 `miniprogram-template/miniprogram/` 下面。

2. 在页面的 json 中配置需要使用的组件：

    ```json
    "usingComponents": {
        "i-button": "../../dist/button/index"
    }
    ```

3. 在 wxml 中使用组件:

    ```html
    <i-button type="primary">这是一个按钮</i-button>
    ```

### 添加 Vant Weapp

1. 下载 [Vant Weapp](https://github.com/youzan/vant-weapp) 的代码，
将 `dist` 目录拷贝到 `miniprogram-template/miniprogram/` 下面。

2. 在页面的 json 中配置需要使用的组件：

    ```json
    "usingComponents": {
        "van-button": "../../dist/button/index"
    }
    ```

3. 在 wxml 中使用组件:

    ```html
    <van-button type="primary">这是一个按钮</van-button>
    ```

## 许可

[![](https://award.dovolopor.com?lt=License&rt=MIT&rbc=green)](./LICENSE)

## 参考

- [Flask document](https://dormousehole.readthedocs.io/en/latest/)
- [如何安装 Python 开发环境？](https://v2ai.cn/linux/2018/04/29/LX-2.html)
- [WeUI document](https://weui.io/)
- [iView Weapp document](https://weapp.iviewui.com/)
- [Vant Weapp document](https://youzan.github.io/vant-weapp/#/intro)
