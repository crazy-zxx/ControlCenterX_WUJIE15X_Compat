# ControlCenterX_WUJIE15X_Compat 
# 机械革命无界15X控制台官方修改兼容安装包

## 当前最新版本 ControlCenterX `5.56.60.46`

## 理论支持 无界 14X / 15X ，AMD Ryzen 7 版本

## 官方网站给的控制台安装包会显示不支持的机型，那就用AI解决！

## Codex 万岁！！！

ControlCenterX 5.56.60.46 — 无界15X兼容安装包（全部由Codex自动完成）
制作日期：2026-11-20

**安装入口：双击 Install-WUJIE15X.cmd，随后按原厂安装向导操作。**

请保留整个目录；setup.ini、logo、PreinstallKit、UserFanTables 等配套内容应与 EXE 放在一起。
入口先核对目标机型、CPU 和安装器 SHA256，再请求管理员权限启动原厂安装流程。
仅检查、不安装：powershell.exe -NoProfile -ExecutionPolicy Bypass -File .\Install-WUJIE15X.ps1 -CheckOnly

目标设备：
MECHREVO WUJIE15XA / WUJIE15-GX5HRXG / AMD Ryzen 7 8845HS。
旧包记录的 BIOS 为 N.1.14MRO20，固件 APVersionCheck=23。
本次未重新检测固件；以上数值来自旧包，不代表本次实测。

本次适配：
以原始 ControlCenterX_5.56.60.46_Mechrevo 为基础，参考 5.56.60.45_WUJIE15X_Compat。
已确认两版的安装脚本编译代码相同，迁移同一项 CHECKAPVERSION 最低值修改：24 -> 23。
解压后的安装元数据恰好只有一个字节变化；没有伪造或修改固件返回值。
新版的程序载荷、驱动、服务、MSIX、语言资源、风扇参数及 179 个配套文件均保留原样。
未将旧版的程序文件或依赖覆盖到新版中。

验证结果：
已重新解压并核对补丁位置、LZMA 数据块 CRC、Inno 引导信息 CRC、偏移和 PE 校验和。
内嵌程序载荷及其余安装元数据与原版逐字节一致；配套文件已核对 SHA256。
完整补丁位置、哈希和配套文件清单见 patch-details.json。
原厂外层签名因修改失效，已移除；此 EXE 为未签名的个人修改版，内嵌程序未修改。
原始目录和旧兼容包均未改动。

验证范围：
本包是与旧包相同范围的安装兼容补丁；未实际安装或验证硬件运行功能。
风扇、性能模式、快捷键、充电限制等功能仍需在目标机器安装后验证。
如运行时不识别硬件或控制异常，请通过 Windows“已安装的应用”卸载。
安装日志保存为本目录 compat-install.log。
