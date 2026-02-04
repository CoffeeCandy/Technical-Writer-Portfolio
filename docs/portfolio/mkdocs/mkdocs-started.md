# 快速上手

## 一、安装与环境准备
* 安装与环境准备
在使用 MkDocs 之前，请先完成以下环境准备和安装步骤。
* 环境要求
MkDocs 基于 Python 开发，请确保本地已安装 Python 环境。
	- Python 版本：3.8 及以上
	- 操作系统：Windows、macOS、Linux 均可

你可以通过以下命令确认 Python 是否已安装：
```bash
python --version
```
或：
```bash
python3 --version
```
如果未安装 Python，请先前往 Python 官方网站完成安装。

* 安装 MkDocs
MkDocs 可通过 Python 的包管理工具 pip 进行安装。
```bash
pip install mkdocs
```

安装完成后，可以通过以下命令验证是否安装成功：
```bash
mkdocs --version
```

如果终端输出 MkDocs 的版本号，说明安装成功。

* 常见问题说明
	- 命令不可用
		如果执行 mkdocs 命令提示未找到命令，请确认：
		- Python 和 pip 已正确安装
		- pip 的安装路径已加入系统环境变量
	- 使用 pip3
		在部分系统中，可能需要使用 pip3 代替 pip：

```bash
		pip3 install mkdocs
```
### 创建第一个项目
* 执行以下命令
```
mkdocs new my-project
cd my-project
mkdocs serve
```
* 在浏览器中打开http://127.0.0.1:8000/，你将看到显示的默认主页：

![first program](../pitcures/firstProgram.jpg)



 



 



 





