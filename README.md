# RelVectors —— AI 工程师

RelVectors 常驻在你的电脑上，像一位随叫随到的工程师：持续读取这台机器的真实读数，和它自己的历史比较，
发现问题先复测确认，只在需要你时才打扰你。改动电脑的每一步都经过授权：只读的直接做，可撤销的按规则做，
不可撤销的一定先问你。

## 六大功能

| 功能 | 做什么 |
|---|---|
| 返老还童 | 找出拖慢和占地方的东西，清理（可撤销）、更新软件，再测速，和这台机器最早的结果比较 |
| 延年益寿 | 跟踪硬盘健康与寿命、电池、热压力和备份，趋势变差时提前提醒 |
| 潜力爆涨 | 测硬盘和处理器的真实能力，找出瓶颈，内存够时部署本地模型 |
| 挖掘宝藏 | 找出可回收的空间、可更新的软件、闲置的处理器和内存 |
| 远程出差 | 到别的机器上替你办事：与其他 RelVectors 配对协作、SSH 远程检查、把事情交给其他 agent |
| 保驾护航 | 探测正在运行的进程，找出不安全因素：可疑位置启动的程序、对外开放的端口、占满处理器的未知程序，再查防火墙、加密和安全更新 |

另有：网页客户端（仪表、任务对话、设置）、端云混合模型（本地优先，云端有预算，个人内容默认不出机器）、
常驻低功耗巡检、硬盘 SMART 健康（安装包已内置 smartctl）。

## 下载

在右侧 **Releases** 下载对应系统的安装包：

| 系统 | 文件 |
|---|---|
| macOS（Apple 芯片） | `RelVectors-<版本>-mac-arm64.tar.gz` |
| macOS（Intel） | `RelVectors-<版本>-mac-x64.tar.gz` |
| Windows 10 / 11（x64） | `RelVectors-<版本>-windows-x64.zip` |
| Windows（ARM） | `RelVectors-<版本>-windows-arm64.zip` |
| Linux（x86_64） | `RelVectors-<版本>-linux-x64.tar.gz` |
| Linux（ARM64） | `RelVectors-<版本>-linux-arm64.tar.gz` |

安装包自带运行环境，**不需要另装 Python 或其他依赖**，安装过程不联网。
Linux 需要 glibc 2.28 及以上（Ubuntu 20.04+、Debian 10+、RHEL / Rocky 8+ 等）。
每个版本附 `SHA256SUMS.txt`，可以核对下载是否完整。

## 安装

- **macOS**：解压后右键点“安装.command”→ 打开（安装包尚未经 Apple 公证，首次需要右键）；
  或在终端进入解压后的文件夹运行 `sh install.sh`。
- **Windows**：解压后双击 `install.cmd`。如果出现“Windows 已保护你的电脑”，点“更多信息 → 仍要运行”。
- **Linux**：解压后在终端运行 `sh install.sh`。

装好后会自动打开浏览器里的客户端，之后也可以随时运行 `rv console`。登录后自动在后台运行，普通用户权限。
需要读取硬盘 SMART 等管理员数据时，按提示运行一次 `sudo rv exec install`（Windows 在“以管理员身份运行”的终端里运行 `rv exec install`）。

卸载：运行安装文件夹里的 `uninstall.sh` / `uninstall.cmd`（保留数据）。

## 试用与激活

- 免费试用 **7 天**，第一次运行时开始计时。
- 到期后在客户端“设置 → 授权”点“复制申请信息”（或在终端运行 `rv license`），
  作为邮件正文发到 **155570@qq.com**，主题随意。系统会自动回信发激活码。
- 把激活码粘贴到同一页面（或运行 `rv license activate <激活码>`）即可。激活不需要联网，有效期从首次激活时开始算。

## 常用命令

```
rv status            本机状态
rv console           打开客户端
rv license           试用与激活
rv service status    后台服务状态
```

## 隐私

RelVectors 只读取机器状态（读数、容量、温度、版本、硬件型号）。文档、文件名、对话、邮件等个人内容，
只在你交办的任务里、经你授权时才读取，默认不发往云端模型。

---

RelVectors 为专有软件。本仓库只提供安装包下载。安装包内置的 smartctl 来自 smartmontools（GPL），其许可证随包附带。
问题与授权：155570@qq.com
