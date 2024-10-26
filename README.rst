# 中国视频下载器 (China Video Downloader)

## 项目简介

中国视频下载器是一个基于 Python 3 的工具，旨在帮助用户从中国媒体站点下载视频文件。该项目支持多种视频格式，并提供简单易用的命令行界面。
本项目是基于[ykdl](https://github.com/LifeActor/ykdl/tree/master)的重构版本，分支代号 2.0。

## 特性

- 支持从多个中国媒体站点下载视频
- 支持多种视频格式（如 MP4、AVI 等）
- 简单易用的命令行界面
- 支持批量下载(当传入的URL参数为播放列表时)
- 自动处理视频链接的解析

## 安装

### 先决条件

确保你的系统上已安装 Python 3.x。你可以通过以下命令检查：

```bash
python3 --version


### 创建虚拟环境

在项目根目录下创建一个虚拟环境：

```bash
python3 -m venv venv
```

### 激活虚拟环境

- **在 macOS/Linux 上**：

  ```bash
  source venv/bin/activate
  ```

- **在 Windows 上**：

  ```bash
  venv\Scripts\activate
  ```

激活后，你会看到命令行提示符前面出现 `(venv)`，表示你已进入虚拟环境。

### 安装依赖

使用 `requirements.txt` 文件安装所需的 Python 模块：

```bash
pip install -r requirements.txt
```

### 依赖模块

以下是项目中可能用到的 Python 模块：

- `requests`：用于发送 HTTP 请求，下载视频文件。
- `beautifulsoup4`：用于解析 HTML 页面，提取视频链接。
- `lxml`：用于加速 HTML 解析。
- `pytube`：用于处理 YouTube 视频下载（如果需要）。
- `argparse`：用于处理命令行参数。

## 使用方法

### 基本用法

在命令行中运行以下命令以下载视频：

```bash
python3 CVD.py <视频链接>
```

### 示例

```bash
python3 CVD.py https://example.com/video123
```

### 批量下载

你可以传入一个播放列表的URL,本脚本会自动解析分集进行批量下载：

```bash
python3 CVD.py https://example.com/videoList
```

## 配置

在项目根目录下，你可以找到一个名为 `config.py` 的文件。在这里，你可以配置一些选项，例如下载目录、默认视频格式等。

```python
DOWNLOAD_DIR = "downloads"
DEFAULT_FORMAT = "mp4"
```

## 贡献

欢迎任何形式的贡献！请遵循以下步骤：

1. Fork 本项目
2. 创建你的特性分支 (`git checkout -b feature/YourFeature`)
3. 提交你的更改 (`git commit -m 'Add some feature'`)
4. 推送到分支 (`git push origin feature/YourFeature`)
5. 创建一个 Pull Request

## 许可证

本项目采用 MIT 许可证，详细信息请查看 [LICENSE](LICENSE) 文件。

## 联系

如有任何问题或建议，请通过以下方式联系我：

- 邮箱: we7soft@gmail.com
- GitHub: [LifeActor](https://github.com/LifeActor)

### 特殊说明

- **我们不主动支持VIP资源解析和下载**：项目仅供研学，进行二次开发扩展所造成的法律问题本项目不负连带责任。
