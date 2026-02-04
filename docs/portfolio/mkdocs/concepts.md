# mkdocs用户指南

### 一、项目结构说明

- **docs/** ：存放所有文档内容，Markdown 文件集中管理。  
- **docs/index.md** ：网站首页，通常为项目简介或欢迎页。  
- **docs/concepts/** ：存放概念类文档，介绍项目核心理念和基础知识。  
- **docs/how-to-guides/** ：存放操作指南，帮助用户一步步完成任务。  
- **docs/assets/** ：存放图片、图标等静态资源，供文档引用。  
- **mkdocs.yml** ：MkDocs 的核心配置文件，定义网站结构、主题等。  
- **requirements.txt** ：Python 依赖列表，方便环境搭建。

通过该结构，项目文档逻辑清晰，便于新增文档和维护。

  

### 二、配置文件说明

#### 1. 概览

- MkDocs 使用 **mkdocs.yml** 作为全局配置文件，用于控制整个文档站点的行为和外观，包括：
    * 站点基本信息（名称、地址等）
    * 左侧导航结构
    * 主题与外观设置
    * 插件与扩展功能


#### 2. 基本结构
- mkdocs.yml使用 **YAML** 格式进行编写，其基本形式为 **键值对（key: value）**。

```ymal
    site_name: My Docs
```


#### 3. 常用核心配置项
- site_name（站点名称）:用于指定文档站点的名称，通常会显示在：**浏览器标签页标题** 和 **页面顶部导航栏**
```ymal
    site_name: MkDocs 用户指南
```
          
- site_url（站点地址，可选）: 用于指定站点的访问地址，在以下场景中非常有用：
    * 部署到 GitHub Pages
    * 启用 SEO 或站点地图插件
```ymal
site_url: https://example.github.io/mkdocs-guide/
```   

- nav（导航配置）:用于定义文档站点左侧的导航结构，是配置中**最重要**、也**最容易出错**的部分。
    - 基本规则
        * 导航顺序与 `nav` 中的定义顺序一致
        * 文件路径必须真实存在
        * 支持多级导航

```ymal 
    nav:
    - 首页: index.md
    - 快速开始: getting-started.md
    - 使用指南:
        - 安装: guide/install.md
        - 配置文件说明: guide/configure
```

