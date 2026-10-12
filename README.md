# India-Stocks-541-570-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 541 to 570)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-541-570-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (541 to 570)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 541 | `ADDIND` | Addi Industries Limited | `ADDIND.NS` |
| 542 | `ADFFOODS` | ADF Foods Limited | `ADFFOODS.NS` |
| 543 | `ADL` | Archidply Decor Limited | `ADL.NS` |
| 544 | `ADOR` | Ador Welding Limited | `ADOR.NS` |
| 545 | `ADROITIND` | Adroit Industries (India) Limited | `ADROITIND.NS` |
| 546 | `ADROITINFO` | Adroit Infotech Limited | `ADROITINFO.NS` |
| 547 | `ADSL` | Allied Digital Services Limited | `ADSL.NS` |
| 548 | `ADVAIT` | Advait Energy Transitions Limited | `ADVAIT.NS` |
| 549 | `ADVANCE` | Advance Agrolife Limited | `ADVANCE.NS` |
| 550 | `ADVANIHOTR` | Advani Hotels & Resorts (India) Limited | `ADVANIHOTR.NS` |
| 551 | `ADVENTHTL` | Advent Hotels International Limited | `ADVENTHTL.NS` |
| 552 | `ADVENZYMES` | Advanced Enzyme Technologies Limited | `ADVENZYMES.NS` |
| 553 | `ADVIKCA` | Advik Capital Limited | `ADVIKCA.NS` |
| 554 | `AEPL` | Artemis Electricals and Projects Limited | `AEPL.NS` |
| 555 | `AEQUS` | Aequs Limited | `AEQUS.NS` |
| 556 | `AEROENTER` | Aeroflex Enterprises Limited | `AEROENTER.NS` |
| 557 | `AEROFLEX` | Aeroflex Industries Limited | `AEROFLEX.NS` |
| 558 | `AERONEU` | Aeroflex Neu Limited | `AERONEU.NS` |
| 559 | `AEROPLANE` | Amir Chand Jagdish Kumar (Exports) Limited | `AEROPLANE.NS` |
| 560 | `AFFORDABLE` | Affordable Robotic & Automation Limited | `AFFORDABLE.NS` |
| 561 | `AFIL` | Akme Fintrade (India) Limited | `AFIL.NS` |
| 562 | `AFSL` | Abans Financial Services Limited | `AFSL.NS` |
| 563 | `AGARIND` | Agarwal Industrial Corporation Limited | `AGARIND.NS` |
| 564 | `AGARWALEYE` | Dr. Agarwal's Health Care Limited | `AGARWALEYE.NS` |
| 565 | `AGASTYAEN` | Agastya Energy and Infrastructure Limited | `AGASTYAEN.NS` |
| 566 | `AGI` | AGI Greenpac Limited | `AGI.NS` |
| 567 | `AGIIL` | Agi Infra Limited | `AGIIL.NS` |
| 568 | `AGL` | Allcargo Global Limited | `AGL.NS` |
| 569 | `AGOL` | Ashapuri Gold Ornament Limited | `AGOL.NS` |
| 570 | `AGRITECH` | Agri-Tech (India) Limited | `AGRITECH.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream ADDIND 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-541-570-Historical-Data/main/ADDIND/1m/2026/10/ADDIND_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
