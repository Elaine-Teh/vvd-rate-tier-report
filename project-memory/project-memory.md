# 项目长期记忆

## 用户偏好
- 用户希望被称为 Elaine。
- 用户希望助手是 master、clever，擅长 analysis、跳出框架思考，并主动给 suggestion。

## 常用入口
- FineBI：`https://bi.culines.com/`
- 主报告本地文件：`C:\Users\elaineteh\WorkBuddy\20260413100944\CNSHA_CNSHK_CNNAS_Rate_Tier_Report.html`
- 主报告 file URL：`file:///C:/Users/elaineteh/WorkBuddy/20260413100944/CNSHA_CNSHK_CNNAS_Rate_Tier_Report.html`
- GitHub 仓库：`https://github.com/Elaine-Teh/vvd-rate-tier-report`
- GitHub Pages：`https://Elaine-Teh.github.io/vvd-rate-tier-report/CNSHA_CNSHK_CNNAS_Rate_Tier_Report.html`

## 常用操作路径
- Income Data Base-Marketing → VVD → 输入 TGLK2610W → Query → 导出 Excel

## 导出数据方法
1. 页面工具栏找下载/Export 按钮（⬇️ 图标）
2. 选择“导出 Excel”
3. 保存文件

## 运费计算公式 (TGLK2610)
- 费用包含：OFT + LSS + WRS + BAF
- 计算公式：(OFT + BAF + LSS + WRS) Charge Amount 总和 ÷ OFT TEUs
- 箱型区分：
  - 20' = 20GP, FE20
  - 40' = 40HC, FE40, 40RH
- SEA 分组：TW=Taiwan, VN=Vietnam, TH=Thailand, MY=Malaysia, 其他=China
- 空值显示：- 

## CNSHA Rate Tier 分类 (按 POD, 最新 2026-04-14)
| POD | 20' FAK | 20' T2 | 20' T1 | 20' Spot | 40' FAK | 40' T2 | 40' T1 | 40' Spot |
|-----|---------|---------|--------|----------|---------|---------|--------|----------|
| SAJED/EGSOK | >$3,000 | $2,601-$2,999 | $2,600 | <$2,600 | >$4,000 | $3,601-$3,999 | $3,600 | <$3,600 |
| DJIJB | >$3,100 | $2,701-$3,099 | $2,700 | <$2,700 | >$4,200 | $3,801-$4,199 | $3,800 | <$3,800 |
| JOAQJ | >$3,200 | $2,801-$3,199 | $2,800 | <$2,800 | >$4,400 | $4,001-$4,399 | $4,000 | <$4,000 |
| YEADE/SDPZU | >$4,000 | $3,601-$3,999 | $3,600 | <$3,600 | >$5,200 | $4,801-$4,999 | $4,800 | <$4,800 |

## CNSHK Rate Tier 分类 (按 POD)
| POD | 20' FAK | 20' T2 | 20' T1 | 20' Spot | 40' FAK | 40' T2 | 40' T1 | 40' Spot |
|-----|---------|---------|--------|----------|---------|---------|--------|----------|
| JED | >$3,000 | $2,851-$2,999 | $2,850 | <$2,850 | >$4,200 | $3,901-$4,199 | $3,900 | <$3,900 |
| SOK | >$3,050 | $2,901-$3,049 | $2,900 | <$2,900 | >$4,300 | $4,001-$4,299 | $4,000 | <$4,000 |
| ADE | >$4,050 | $3,901-$4,049 | $3,900 | <$3,900 | >$5,700 | $5,651-$5,699 | $5,650 | <$5,650 |
| PZU | >$3,900 | $3,751-$3,899 | $3,750 | <$3,750 | >$5,400 | $5,351-$5,399 | $5,350 | <$5,350 |
| DMN | >$5,500 | $5,351-$5,499 | $5,350 | <$5,350 | >$6,700 | $6,641-$6,699 | $6,640 | <$6,640 |
| RUH | >$5,500 | $5,399-$5,499 | $5,400 | <$5,400 | >$6,800 | $6,501-$6,799 | $6,500 | <$6,500 |

## HTML 报告格式要求
- Spot Bookings 表格格式：简洁表格，按 POL (CNSHA/CNSHK/CNNAS) 分组
- 列：B/L No. | Size (20'/40') | POD | Rate ($)
- Spot 分类行：红色背景 (#FFC7CE) + 红色字体 (#9C0006)
- 新增/修正记录：深红色背景 (#FF0000) + 白色字体高亮显示
- 表格样式：w-full text-sm，thead 用浅色背景 bg-xxx-100
- 修正记录需高亮：用户手动修正某个记录的分类时，用 highlight-spot class 高亮

## Overview 页面格式 (Rate Tier Report)
### China Ports 表格 (含 Tier Distribution)
| Port | B/Ls | Bookings | TEU |
|------|------|----------|-----|
| CNSHA | 126 | 20 | 393 |
| CNSHK | 99 | 31 | 245 |
| CNNAS | 106 | 24 | 350 |
| CNSWA | 2 | 2 | 22 |

### SEA Ports 表格 (FAK only, 无 tier distribution)
| Region | B/Ls | Bookings | TEU |
|--------|------|----------|-----|
| Taiwan | 51 | 4 | 77 |
| Thailand | 94 | 4 | 139 |
| Vietnam | 79 | 4 | 79 |

### 汇总卡片
- Total B/Ls: 333 (含 CNSWA)
- Total Bookings: 77
- Total TEU: 1,305 (China 1,010 + SEA 295)
- Tier Distribution 仅显示 China Ports
