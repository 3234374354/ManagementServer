# ClassIsland.ManagementServer

ClassIsland 集控服务器。

> **注意：本项目是ClassIsland集控服务器。如果您要查找ClassIsland软件本体，请前往仓库[HelloWRC/ClassIsland](https://github.com/HelloWRC/ClassIsland)**

## 功能

> [!TIP]
>
> 您可以点击下方链接或查看 [ClassIsland 文档](https://docs.classisland.tech) 了解更多。

### 管理后端

- [x] 实例注册与获取
- [x] 实例分组
- [x] 上传档案

### 数据分发

- [x] 按实例与分组拼接数据
- [x] 分发策略
- [x] 分发设置信息
- [x] 分发档案信息
- [x] 使用grpc向客户端发送命令
  - [ ] 向客户端发送提醒
  - [ ] 通知客户端更新数据

### API

- [x] API返回分页

### WebUI
- [x] 批量创建对象
- [x] 管理并分组实例
- [x] 管理并分组档案（课表、时间表、科目）信息
- [x] 上传档案信息
- [ ] 从表格导入课表
- [ ] 管理并分组策略
- [x] 管理并分组默认设置

### 用户
- [x] 用户创建与管理
- [ ] 用户鉴权
- [ ] 用户角色（管理员，教师，访客等）

## 开始使用（预览）

**请确保您的设备满足以下推荐需求：**

- Windows / Linux 系统  
- [Windows .NET 8.0 桌面运行时](https://dotnet.microsoft.com/zh-cn/download/dotnet/thank-you/runtime-desktop-8.0.7-windows-x64-installer)
- [Linux .NET 8.0 桌面运行时](https://learn.microsoft.com/zh-cn/dotnet/core/install/linux)

> [!IMPORTANT]
> 
> **本版本为预览版，仅用于测试和开发环境，请勿在生产环境中使用。**  
> 如您是普通用户，建议等待官方发布构建版本。

---

对于开发者或高级用户，您可以从以下渠道获取本软件的预览版本：

### 获取安装包

1. 访问 [GitHub Actions - ManagementServer](https://github.com/ClassIsland/ManagementServer/actions) 页面
2. 选择最新左侧带对勾的Action进入
3. 在 “Summayr” 底部下载适用于您平台的压缩包文件

### 安装步骤

1. 将压缩包解压到一个**独立的文件夹**（路径中请勿包含中文或特殊字符）
   > ⚠️ 请勿将程序解压至网盘同步目录、【下载】文件夹等可能存在访问限制的路径，否则可能导致**文件读写失败、配置丢失**等问题。
2. 将 `data/appsettings.example.json` 文件复制为 `appsettings.json`（位于程序主目录下）
3. 创建数据库，并记录数据库地址、用户名、密码及数据库名称
4. 编辑 `appsettings.json` 文件：
   - 修改 `ConnectionStrings.Production` 键值：
     1. 替换 `{Your Host}` 为数据库服务器地址（无需端口，如 `localhost`）
     2. 替换 `{User Id}` 为数据库用户名
     3. 替换 `{Your Password}` 为数据库密码
     4. 替换 `classisland_management` 为实际使用的数据库名
   - 添加/修改键 `DatabaseType` 为 `mysql`（目前仅支持 MySQL）
5. 如果您是 Windows 用户，可直接运行 `.ps1` 启动脚本启动服务
6. 如果您是 Linux 用户，并希望长期运行服务，可参考[此文档](https://blog.csdn.net/Pan_peter/article/details/128875714)进行配置

> [!NOTE]
> 如果您遇到任何问题，请前往 [ClassIsland.ManagementServer GitHub 仓库](https://github.com/ClassIsland/ManagementServer) 提交 issue 或查阅相关讨论内容。  


**🚧本项目还在开发中**

