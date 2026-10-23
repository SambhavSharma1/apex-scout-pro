# ⚽ ApexScout Pro | Football Recruitment Intelligence & Arbitrage Analytics

> **Built for the Open-Source Sports Analytics Hackathon**  
> A high-density recruitment analytics dashboard designed for technical directors and scouts to identify statistically equivalent, undervalued alternatives to high-cost superstars.

---

## 📌 Problem Statement

In European football, elite clubs spend upwards of **€100M–€180M** on proven superstars (e.g., Erling Haaland, Jude Bellingham, Rodri). Mid-tier and budget-conscious clubs cannot compete financially under traditional, reputation-based scouting. 

Traditional recruitment often suffers from:
* **Subjective Evaluation Bias**: Over-weighting recent highlights or international tournament hype.
* **Superstar Inflation Premium**: Paying 3x–5x more for brand reputation rather than underlying statistical output.
* **Capital Misallocation**: High transfer fees leave clubs unable to balance squad depth.

**ApexScout Pro** addresses this with **multidimensional statistical vector matching**: comparing prospects across normalized per-90 metrics (Expected Goals, Expected Assists, Line-Breaking Progressive Passes, Duels Won %, and High-Press Recoveries) to identify high-fit surrogates at **60%–75% cost reduction**.

---

## 🚀 Core Features

* **Benchmark Role Selector**: Compare candidates against proven benchmarks across specific tactical profiles (Erling Haaland, Kevin De Bruyne, Bukayo Saka, Jude Bellingham, Rodri, Virgil van Dijk).
* **Multi-Vector Radar Analysis**: Interactive Chart.js radar overlay illustrating 6 normalized percentile metrics (0–99th percentile per 90 mins).
* **Capital Efficiency Arbitrage Calculator**: Quantifies transfer fee variance, cost reduction percentage, and capital multipliers in real time.
* **Scouted Candidate Data Table**: Sortable, filterable candidate database with instant breakdown by League, Age ceiling, and Maximum transfer fee.
* **Technical Scouting Verdicts**: Actionable qualitative summaries outlining tactical strengths, developmental considerations, and squad-building recommendations.

---

## 🧮 Statistical Methodology

Player similarity is calculated using a **Normalized Euclidean Distance Vector Model** against positional percentile metrics:

$$\text{Similarity \%} = \left( 1 - \frac{\sqrt{\sum_{i=1}^{n} (M_{\text{benchmark}, i} - M_{\text{candidate}, i})^2}}{\sqrt{n \times 100^2}} \right) \times 100$$

Where:
* $M_i \in [0, 99]$ represents the metric value normalized to the player's positional cohort per 90 minutes.
* Metrics are selected to reflect primary role demands (e.g., non-penalty xG and box touches for strikers; progressive passing and press resistance for defensive midfielders).
* The **Capital Multiplier** measures purchasing efficiency:
  $$\text{Capital Multiplier} = \frac{\text{Market Value}_{\text{Benchmark}}}{\text{Market Value}_{\text{Candidate}}}$$

---

## 🛠️ Tech Stack

* **Frontend**: HTML5, Vanilla JavaScript (ES6+)
* **Styling**: Tailwind CSS (Clean High-Density Dark Theme)
* **Data Visualization**: Chart.js (Radar & Percentile Progress Bars)
* **Typography**: Inter & JetBrains Mono (Tabular numerals)
* **Icons**: Lucide Icons
* **Deployment**: Static Web / GitHub Pages (Zero build dependencies)

---

## 💻 How to Run Locally

1. Clone or download this repository:
   ```bash
   git clone https://github.com/your-username/apex-scout-pro.git
   ```
2. Open `index.html` directly in any web browser (Chrome, Edge, Firefox, Safari).
   * No `npm install`, no backend servers, and no build configuration required.

---

## 📄 License

This project is open-source under the [MIT License](LICENSE).
