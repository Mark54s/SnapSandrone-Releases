<p align="center">
  <img src="assets/banner.svg" alt="VibrationSnap — 离线振动分析与出图工作区" width="100%">
</p>

<h3 align="center">从测试通道，到测点、图表和报告。</h3>

<p align="center">
  为振动测试中的多通道、多工况分析准备的离线桌面工具箱。<br>
  整理接线、查看信号、标注峰值，把分析结果带进报告。
</p>

<p align="center">
  <strong>Windows x64</strong> &nbsp; · &nbsp; 解压即用 &nbsp; · &nbsp; 无需 Python &nbsp; · &nbsp; 默认离线
</p>

<p align="center">
  <a href="https://github.com/Mark54s/SnapSandrone-Releases/releases/download/v0.0.1-beta.4/VibrationSnap-v0.0.1-beta.4-windows-x64.zip"><strong>下载 Windows 便携版 ↓</strong></a>
  &nbsp;&nbsp; / &nbsp;&nbsp;
  <a href="https://github.com/Mark54s/SnapSandrone-Releases/releases/tag/v0.0.1-beta.4">本版更新</a>
  &nbsp;&nbsp; / &nbsp;&nbsp;
  <a href="#三步开始">使用方法</a>
  &nbsp;&nbsp; / &nbsp;&nbsp;
  <a href="https://github.com/Mark54s/SnapSandrone-Releases/issues">反馈问题</a>
</p>

<p align="center"><sub>v0.0.1-beta.4 · 约 107 MiB · 2026-10-21 · 早期测试版</sub></p>

---

## 一个工作区，看清一组信号

将通道拖成图卡，用时域、频域和时频视角观察同一段数据。每张卡保存自己的参数；切换左侧浏览的通道时，已有图表保持原来的来源。

<p align="center">
  <img src="assets/workspace-deepseek.png" alt="大肥鱼主题工作区：合成信号的时域、幅值谱、Welch PSD 与 STFT 四张图卡" width="100%">
</p>

<p align="center"><sub>大肥鱼（DeepSeek）主题 · 工作区预览使用合成信号</sub></p>

## beta.4，把重复操作连起来

### 01 &nbsp; 一次整理接线，多组工况沿用

把板卡通道映射为测点号和 X / Y / Z 方向，保存成**实验接线模板**。同一实验的各工况可以共用，不用逐份重填。

中途换线或通道故障时，可为某个工况单独设置、停用映射，之后再恢复继承。默认图卡标题与 Word 使用同一份生效映射，原始通道身份仍保留，方便追溯。

### 02 &nbsp; 连续点峰，集中整理测量结果

预先设置点击附近的搜索秒窗，单击吸附其中的最高峰，再结合峰附近若干周期估计局部平均频率。也可标记稳态区间，查看振幅、周期等测量结果。

测量模式可以跨图卡连续使用；标好后，将**全部或选中图卡的标记汇总为 CSV**，保留来源、通道和标记身份，便于后续整理。

### 03 &nbsp; 排好图卡，带着测点信息出报告

画布支持自动适应列数、固定多列和自由摆放。新工作区默认开启拖动统一图卡大小，也可关闭，适应不同的排版需求。

Word 报告可按板卡通道、测点号或 XYZ 正倒序整理实际出图顺序。**报告配置和接线模板都能从 Word 载入入口打开**；工况文字、题注与接线各自维护。

[查看完整更新记录 →](releases/v0.0.1-beta.4.md)

## 从导入到交付

| 整理数据 | 分析与查看 | 出图与交付 |
| :--- | :--- | :--- |
| TDMS / CSV / TXT 导入 | 时域、幅值谱、Welch PSD | PNG / PDF / SVG 图片 |
| 文件夹扫描、分组与通道浏览 | STFT、包络谱、倒谱、倍频程 | 通道数据、分析结果与测量 CSV |
| 裁剪、去均值、高通 / 低通滤波 | 互谱、相干与时域统计 | 批量图片、Word 图片报告 |
| 实验接线模板、工况映射例外 | 峰值 / 稳态标注、坐标与标题设置 | 来源、参数及视图配置保存 |

处理生成派生结果，**原始文件始终只读**。默认离线运行，无需账号，不上传测试数据。

## 三步开始

**1. 下载并完整解压**

获取 [beta.4 Windows 便携包](https://github.com/Mark54s/SnapSandrone-Releases/releases/download/v0.0.1-beta.4/VibrationSnap-v0.0.1-beta.4-windows-x64.zip)，解压到有写入权限的目录。进入 `VibrationSnap` 文件夹，运行 `VibrationSnap.exe`；保留旁边的 `_internal` 文件夹。

> 选择 Release 附件中的 **`VibrationSnap-…-windows-x64.zip`**。GitHub 自动生成的 **Source code** 压缩包是本下载仓库的文件，不是可运行程序。

**2. 导入数据，生成图卡**

点击「导入数据…」，将通道拖入中央工作区。选中图卡，设置分析类型和参数，再点「应用并更新」。需要同时查看时域和频域时，为同一通道建立不同类型的图卡即可。

**3. 标注、导出并保存工程**

如需测点名称，先在左侧「测点映射…」载入接线模板并应用。完成分析后，从导出菜单选择图片、数据或 Word 图片报告，再保存工程以便继续工作。

<details>
<summary><strong>第一次使用接线模板？展开查看</strong></summary>

1. 在左侧选择暂存记录，打开「测点映射…」。
2. 载入接线模板 JSON，也可从旧报告配置提取接线关系；检查测点号和方向后点击「应用」。
3. 其他工况默认沿用模板。需要例外时，选择「本工况单独设置」或「本工况停用映射」。
4. 已有独立映射不会被新模板覆盖。需要跟随模板时，多选后点击「所选恢复继承」。

Word 中的「载入配置 / 接线模板…」也能读取接线模板；点击「应用映射到工作区」或导出后才提交。取消未应用的草稿不会改工程，已经明确应用的映射会保留。

模板与工况例外随工程保存；停用映射不会删除原通道或信号。

</details>

## 两种外观，同一套分析

首次启动默认 **大肥鱼（DeepSeek）**，冷白与蓝色；也可选择暖白与棕色的 **素纸**。在「视图 → 外观主题… → 应用并保存」中切换，当前工作区保留，科学图表与报告不随界面主题改变。

<details>
<summary><strong>看看「素纸」工作区</strong></summary>

<p align="center">
  <img src="assets/workspace-paper.png" alt="素纸主题工作区：同一组合成信号的时域与频谱分析图卡" width="100%">
</p>

<p align="center"><sub>便携版提供大肥鱼与素纸两种内置主题，预览使用同一组合成数据。</sub></p>

</details>

## 下载、升级与常见问题

<details>
<summary><strong>需要安装 Python、MATLAB 或 Office 吗？</strong></summary>

无需安装 Python。普通分析、Python 图片导出和 Word 图片报告生成均不需要 MATLAB 或 Office；阅读编辑 `.docx` 文件需要 Word 或兼容软件。

可选的 MATLAB 原生绘图后端需自行安装并授权 MATLAB。目前该后端支持时域 PNG；频域图片及 PDF / SVG 请使用 Python 后端。下载包不包含 MATLAB 或其授权。

</details>

<details>
<summary><strong>升级时，怎样保留我的数据和工程？</strong></summary>

先退出旧程序，备份自己的工程、接线模板、导出结果和程序旁的 **`artifacts`** 目录。建议将新版解压到新目录，再迁移需要保留的文件；不要用空目录覆盖旧暂存数据。

工程保存来源引用、处理参数、接线映射和视图配置，不内嵌样本数据。重新打开工程时，仍需确保关联数据可访问，并点击「应用并更新」生成图表。含新功能的工程，旧版可能无法读取。

</details>

<details>
<summary><strong>如何核对下载文件？</strong></summary>

下载同一版本的 [SHA256SUMS.txt](https://github.com/Mark54s/SnapSandrone-Releases/releases/download/v0.0.1-beta.4/SHA256SUMS.txt)，在 ZIP 所在目录打开 PowerShell：

```powershell
Get-FileHash -LiteralPath 'VibrationSnap-v0.0.1-beta.4-windows-x64.zip' -Algorithm SHA256
```

将输出与校验文件中的 SHA-256 对比，应完全一致。程序尚未代码签名，Windows 可能提示发布者未知；如遇安全软件报警，请先核实下载来源和文件。

</details>

<details>
<summary><strong>这个仓库包含应用源码吗？</strong></summary>

这里提供软件下载、版本说明和问题反馈，**不包含应用源码或开发历史**。应用源码目前未以开源许可证发布；下载包内的第三方组件遵循各自许可证，相关声明随包保留。

</details>

---

## 把试用中的问题告诉我

VibrationSnap 仍处于早期测试阶段，不同电脑、显示缩放和数据组合尚未全面验证，重要分析结论请独立核对。

欢迎 [提交 Issue](https://github.com/Mark54s/SnapSandrone-Releases/issues/new)，附上 **软件版本、Windows 版本、复现步骤、预期与实际结果**。界面问题可补充显示缩放比例和脱敏截图；复现样例优先使用合成信号，请勿公开上传保密实验数据、账号凭据或未经脱敏的工程与日志。

<p align="center">
  <a href="https://github.com/Mark54s/SnapSandrone-Releases/releases/latest"><strong>下载最新版本</strong></a>
  &nbsp; · &nbsp;
  <a href="https://github.com/Mark54s/SnapSandrone-Releases/releases">历史版本</a>
  &nbsp; · &nbsp;
  <a href="https://github.com/Mark54s/SnapSandrone-Releases/issues/new">反馈与建议</a>
</p>
