<p align="center">
  <img src="assets/banner.svg" alt="VibrationSnap — offline vibration analysis" width="100%">
</p>

<p align="center">
  <strong>导入 · 分析 · 对比 · 出图</strong><br>
  面向振动测试与分析的离线桌面工具箱
</p>

<p align="center">
  <a href="https://github.com/Mark54s/SnapSandrone-Releases/releases/latest"><strong>下载 Windows 便携版</strong></a>
  &nbsp; · &nbsp;
  <a href="https://github.com/Mark54s/SnapSandrone-Releases/releases">版本记录</a>
  &nbsp; · &nbsp;
  <a href="https://github.com/Mark54s/SnapSandrone-Releases/issues">问题反馈</a>
</p>

---

## 下载与启动

**当前版本：v0.0.1-beta.3 · Windows x64 · 便携测试版**

1. [下载 VibrationSnap Windows x64 ZIP](https://github.com/Mark54s/SnapSandrone-Releases/releases/download/v0.0.1-beta.3/VibrationSnap-v0.0.1-beta.3-windows-x64.zip)。
2. 完整解压到有写入权限的文件夹，不要直接在压缩包里运行。
3. 进入 `VibrationSnap` 文件夹，双击 **`VibrationSnap.exe`**。

无需安装 Python。必须保留 EXE 旁的 **`_internal` 文件夹**，不能只复制 EXE。
GitHub 自动生成的 **Source code (zip / tar.gz)** 只有本下载仓库的说明文件，**不是软件安装包**。

## 可以做什么

| 数据 | 分析 | 工作区与导出 |
| :--- | :--- | :--- |
| TDMS / CSV / TXT 导入 | 时域、幅值谱、Welch PSD | 一卡一图、专注查看、拖动排序 |
| 文件夹导入、分组与通道浏览 | STFT、包络谱、倒谱、倍频程 | 多卡批量参数与坐标范围 |
| 裁剪、去均值、高/低通滤波 | 互谱、相干及统计质检 | 工作区保存、图片/数据导出、**Word 图片报告** |

### 第一次使用

**导入数据 → 选择通道并拖入中央工作区 → 选中图卡设置参数 → 应用并更新 → 导出。**

- 每张图卡显示一张图；同时比较时域和频域时，建立两张图卡即可。
- 原始文件只读，处理结果与原始数据分开。
- 工作区保存来源引用、参数和视图配置；重新打开后点击“应用并更新”生成图表。
- 默认离线处理，不需要登录，也不上传实验数据。

## 本版更新

- 提供 **大肥鱼（DeepSeek）** 与 **素纸** 两种内置外观；在“视图 → 外观主题…”中应用并保存，立即切换。
- 便携版不载入其他自定义皮肤；本机已有主题文件保持原样。首次默认大肥鱼。
- 分析工作区与滤波调试使用页签导航，改进空闲暂离时的会话保留、只读保护及诊断中文显示。
- 保留 Word 图片报告及既有分析、图片/数据导出功能。

## MATLAB 是否必需？

**不必需。** 普通分析与 Python 图片导出无需 MATLAB。

MATLAB 原生绘图是可选后端，需要自行安装并授权 MATLAB，再在软件中配置其可执行文件。
当前 MATLAB 后端仅支持**时域 PNG**；频域图片、PDF/SVG 请使用 Python 后端。
本下载不包含 MATLAB 或 MATLAB 授权。

## 使用前请知道

- **这是早期测试版**，尚未全面验证不同电脑、DPI 与所有数据组合；重要分析结论请独立核对。
- 程序尚未代码签名，Windows 可能提示发布者未知。请核对本仓库下载来源与 Release 中的 `SHA256SUMS.txt`；若安全软件报警，请先核实，不要直接关闭防护。
- 导入副本、设置及工程可能保存在程序旁的 `artifacts` 目录。**升级或删除旧版本前，请备份 `artifacts`、工程文件及导出结果**；不要盲目覆盖用户数据。
- MATLAB 原生图片文字与不同电脑上的实际输出仍需用户验收。

<details>
<summary>如何校验下载文件（可选）</summary>

在 PowerShell 中运行（将路径换成你的 ZIP 路径）：

```powershell
Get-FileHash -LiteralPath 'VibrationSnap-v0.0.1-beta.3-windows-x64.zip' -Algorithm SHA256
```

将结果与同一 Release 的 `SHA256SUMS.txt` 对比，应完全一致。

</details>

## 问题反馈

请在 [Issues](https://github.com/Mark54s/SnapSandrone-Releases/issues/new) 描述：软件版本、Windows 版本、操作步骤、预期结果与实际结果。
截图请先遮盖个人信息。**不要公开上传保密实验数据、账号凭据或包含私人路径的工程/日志**；需要样例时优先使用合成信号。

## 关于本仓库

这里只提供 VibrationSnap 的软件下载、版本说明与问题反馈，**不包含应用源码或开发历史**。
目前未以开源许可证发布应用源码。下载包中的第三方组件遵循各自许可证，相关声明保留在包内。
