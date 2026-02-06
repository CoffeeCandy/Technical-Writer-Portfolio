# 核心概念

## 一、文档源文件
* MkDocs中文档源文件是用Markdown格式编写的内容，通常存放在docs目录，构建时转换为静态网页。


## 二、主题
* MkDocs 主题控制文档网站的外观和布局，包括颜色、字体、导航样式，帮助打造统一且美观的用户界面体验。


## 三、构建
* 构建build的含义是将你的 Markdown 文档转换成静态的 HTML 网站。它会根据你项目中的 mkdocs.yml 配置文件和 docs/ 目录下的 Markdown 文件，生成完整的静态网页文件。生成的网站文件存放在 site/ 目录，你可以直接打开这些文件查看，也可以将它们上传到服务器或部署到 GitHub Pages 等平台。
  
## 四、Favicon图标
* MkDocs中的Favicon是网站浏览器标签页显示的小图标，用于品牌识别和提升用户体验，通常通过配置文件设置。

## 五、mkdocs.yml配置项说明
### 1. 概览

* MkDocs 使用 **mkdocs.yml** 作为全局配置文件，用于控制整个文档站点的行为和外观，包括：
    - 站点基本信息（名称、地址等）
    - 左侧导航结构
    - 主题与外观设置
    - 插件与扩展功能


### 2. 基本结构
* mkdocs.yml使用 **YAML** 格式进行编写，其基本形式为 **键值对（key: value）**。比如

```ymal
    site_name: My Docs
```


### 3. 核心配置项说明
* site_name（站点名称）:用于指定文档站点的名称，通常会显示在：**浏览器标签页标题** 和 **页面顶部导航栏**
```ymal
    site_name: MkDocs 用户指南
```
          
* site_url（站点地址，可选）: 用于指定站点的访问地址，在以下场景中非常有用：
    * 部署到 GitHub Pages
    * 启用 SEO 或站点地图插件
```ymal
    site_url: https://example.github.io/mkdocs-guide/
```   

* nav（导航配置）:用于定义文档站点左侧的导航结构，是配置中**最重要**、也**最容易出错**的部分。
    - 基本规则
        - 导航顺序与 `nav` 中的定义顺序一致
        - 文件路径必须真实存在
        - 支持多级导航

```ymal 
    nav:
    - 首页: index.md
    - 快速开始: getting-started.md
    - 使用指南:
        - 安装: guide/install.md
        - 配置文件说明: guide/configure
```

