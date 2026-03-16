# WorkTime Tracker · 工时记录

> **一个文件，零依赖，专为在加拿大安大略省打工的你而生。**
> *One file. Zero dependencies. Built for workers in Ontario, Canada.*

---

## 截图 · Screenshots

![image-20260317010001447](C:\Users\TIANY\AppData\Roaming\Typora\typora-user-images\image-20260317010001447.png)

| 日历视图 Calendar | 薪酬预估 Payroll | 工资单对比 Payslip |
|:-:|:-:|:-:|
| 粉色渐变日历，高亮发薪周期 | 双周薪酬拆分，实时税费估算 | 实收 vs 预估，一目了然 |

---

## 这是什么 · What is this?

一个**单 HTML 文件**的工时 + 薪酬追踪工具，无需安装，无需服务器，无需账号。
打开即用，数据存在你自己浏览器里，永远不会上传到任何地方。

A **single HTML file** work-hours and pay tracker. No install. No server. No account.
Just open it in any browser — your data stays in your browser, forever private.

---

## 功能一览 · Features

### 📅 智能日历
- 月份视图，支持**月份 / 年份快速跳转**选择器
- 键盘方向键导航日期（← → ↑ ↓）
- 点击任意日期自动跳转到当日工时录入
- 发薪日 🟡 金色高亮，选中工资单后显示 🟢 绿色薪酬周期
- 自动标记安大略省法定节假日（2024–2027）

### ⏱ 工时录入
- 录入上下班时间（精确到分钟）
- **跨午夜班次**自动识别，无需手动换算
- **快速填写按钮**：一键填入 8h / 7.5h / 7h / 6h / 4h 班次（默认 9:00 开始）
- **编辑已有记录**：点击 ✏️ 修改任意班次，无需删除重填
- 每条记录支持自定义备注（班次名、备注等）
- 一天内可添加多段工时

### 💰 薪酬计算
- 基于加拿大安大略省 **2025 年税率**估算
  - 联邦所得税（Federal Income Tax）
  - 安大略省税（Ontario Provincial Tax）
  - CPP 养老金（5.95%，上限 $4,034.10）
  - EI 就业保险（1.66%，上限 $1,049.12）
- **每周 44 小时加班门槛**（ESA 标准，可自定义）
- 法定节假日 1.5× 薪酬（倍率可调）
- 以双周年化模型计算，接近实际 CRA 扣税方式

### 📋 发薪记录 & 对比
- 记录每次发薪日的**实收工资 + 小费**
- 自动计算该发薪日对应的双周薪酬周期（周一到周日）
- **实收 vs 预估** 对比面板，清晰显示差额
- 可滚动浏览历史工资单列表

### 🔮 未来两期预估
- 自动从最近已覆盖周期结束后的下一个周一开始
- 显示**两个完整双周周期**的预估税前 / 税后收入
- 若当日在某周期内，显示**周期进度条**（已过天数 / 剩余天数）

### 📊 本年度汇总
- 薪酬页顶部实时展示当年：总工时、预估总税前、实收总金额

### 🗓 月度概览横幅
- 仅统计**未发薪**的工时（已被工资单覆盖的日期自动排除）
- 显示待发工作天数、工时数、假期天数、预估收入

### ⚙️ 灵活设置
- 基础时薪（安大略省 2025 年最低工资 $17.20/h）
- 每周加班门槛（默认 44h，可自定义）
- 工作周起始日（周一 / 周日）
- 假期薪酬倍率（默认 1.5×）
- 一键开关法定节假日自动标记

### 🌐 中英文切换
- 全界面双语支持，随时一键切换
- 语言偏好自动保存

### 💾 数据导出 / 导入
- 一键导出为 JSON 文件（含工时、设置、全部工资单记录）
- 支持跨设备导入，数据完整迁移

---

## 快速开始 · Quick Start

```bash
# 克隆或直接下载
git clone https://github.com/your-username/worktime-tracker.git

# 用浏览器打开（无需任何构建步骤）
open index.html
```

或者直接 **[点击 index.html → 在浏览器中打开](index.html)**，完事。

---

## 技术栈 · Tech Stack

| 项目 | 说明 |
|------|------|
| 语言 | 原生 HTML + CSS + JavaScript |
| 依赖 | **零** |
| 数据存储 | `localStorage`（纯本地，不联网） |
| 兼容性 | 所有现代浏览器 + 手机浏览器（响应式） |
| 文件数量 | **1 个** |

---

## 税务说明 · Tax Disclaimer

> ⚠️ 本工具的税费估算**仅供参考**，基于安大略省 2025 年联邦及省级税率，采用双周年化模型。
> 实际税额因个人情况（RRSP、额外扣除、多份工作等）可能有所不同。
> 请以实际工资单和 CRA 官方文件为准。

> ⚠️ Tax estimates are **for reference only**, using Ontario 2025 federal and provincial rates with a bi-weekly annualized model.
> Actual deductions vary based on personal circumstances. Always refer to your official payslip and CRA guidelines.

---

## 数据安全 · Privacy

所有数据**仅存储在你的本地浏览器**（`localStorage`），从不发送到任何服务器。
清除浏览器数据前请先导出 JSON 备份。

All data is stored **exclusively in your local browser** (`localStorage`) and never sent anywhere.
Export a JSON backup before clearing browser data.

---

## 适用人群 · Who is this for?

- 在安大略省按小时计薪的员工
- 服务行业、零售、餐饮从业者（有小费记录）
- 想核对每次发薪是否准确的打工人
- 需要一个轻量、离线、无账号工具的所有人

---

## License

MIT — 随便用，随便改，记得留个 ⭐ 就好。
MIT — Use it, fork it, just leave a ⭐ if it helped you.
