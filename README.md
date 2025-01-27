**DScanX** 是一个开源的命令行工具，旨在帮助网络安全专业人员进行子域名信息收集。以下是 DScanX 的主要功能和特点：

### 主要功能

1. **子域名扫描**：
   - 从 Fofa 等数据源中查询目标域名的子域名。
   - 通过指定的字典文件或默认字典文件进行子域名爆破。
2. **存活检测**：
   - 通过 HTTP 和 HTTPS 请求检查子域名是否存活，并获取其响应状态码。
3. **结果保存与处理**：
   - 将有效的子域名保存到指定文件中，并支持去重处理。
   - 提供了结果的加载效果和颜色化的控制台输出，便于用户实时查看扫描进度。
4. **多线程支持**：
   - 支持并发执行，以加快扫描速度。
   - 可以通过命令行参数设置并发线程数，控制扫描的并发量。
5. **自定义配置**：
   - 支持从文件中读取目标域名、字典文件等配置。
   - 可以自定义 Fofa API 的 email 和 key。

### 主要组件

- **命令行界面**：
  - 提供用户友好的命令行参数设置。
  - 支持多种配置选项，如目标域名、字典文件路径、并发线程数等。
- **子域名爆破与存活检测**：
  - 利用指定的字典进行子域名爆破。
  - 使用 HTTP 和 HTTPS 请求检测子域名的存活状态。
- **文件操作**：
  - 支持读取和写入子域名列表，确保数据的持久性和可用性。

### 使用方法

1. **安装与运行**：

   - 使用 Go 语言构建工具编译 DScanX。
   - 运行命令行工具，并使用参数指定配置文件、目标域名、字典文件等。

2. **示例命令**：

   ```
   DScanX.exe -domains domains.txt -dict dict.txt -thread 10
   ```

   这个命令会读取 `domains.txt` 文件中的目标域名，使用 `dict.txt` 字典文件进行子域名爆破，并设置并发线程数为 10。

   运行截图:
   ![image](https://github.com/user-attachments/assets/6b8a27c4-5c5b-4ef9-a3de-c3aa580dcd6f)

后续更新:多目标扫描
