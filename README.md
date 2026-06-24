# f1-dominance-analytics
A 75-season historical analytics pipeline and dark-mode interface tracking Formula 1 constructor eras and driver dominance metrics from 1950 to 2025.

# 🏎️ Formula 1 Racing Eras & Constructor Dominance (1950—2025)
### An End-to-End Historical Data Pipeline & Live Telemetry Interface
---

## 📌 Project Overview
This project processes **75 seasons and 1,142 unique Grand Prix race records** to analyze, segment, and track team dominance curves across the history of Formula 1. 

By handling legacy data anomalies and designing custom time-series cross-tabulations, this framework transitions from raw text-encoding cleaning to a beautiful, interactive frontend application designed from wireframes up.

### 🛠️ The Analytical Stack
* **Data Cleansing & Cross-Tabulation:** Microsoft Excel (Text Sanitization, Chronological Epoch Modeling)
* **Exploratory Data Pipeline:** Python / Jupyter Notebooks (Pandas Framework)
* **Frontend Web Application:** Vanilla HTML5, Advanced Flex/Grid Structuring, Embedded CSS Variables
* **UI/UX Ideation:** Figma Design Engine (High-Contrast Telemetry Theme)

---

## 🧼 1. Data Cleaning & Encoding Correction
Legacy athletic archives frequently suffer from text-encoding corruption. A massive profiling audit of the raw records flagged systemic character breakages across international driver names and historic constructors.

### Core Corrections:
* **Text Artifact Stripping:** Isolated and sanitized corrupt UTF-8 text anomalies—merging broken names like `NinoÂ Farina` $\rightarrow$ `Nino Farina`, `AlfaÂ Romeo` $\rightarrow$ `Alfa Romeo`, and cleaning trailing artifacts from classic teams (e.g., `FerrariÂ` $\rightarrow$ `Ferrari`). 
* **Dynamic Time-Series Anchors:** Transformed flat race dates into explicitly grouped `Decade` (e.g., `1950s`) and custom `Era` categorical labels inside the data layer. This structural step was critical to mapping continuous time data into clean horizontal timeline slicers on the web frontend.

---

## 📊 2. Historical Cross-Tabulation Matrix
To map out the shifting dominance index of constructor market share over 75 years, a multidimensional matrix sheet (`Constructor Wins by Decade`) was engineered. 

* **The Core Pattern:** The data highlights structural longevity versus sudden localized spikes. Ferrari anchors the sport's baseline across every single era cell (securing 17 landmark baseline wins across the spectrum), whereas teams like Brawn GP appear as localized anomalies, flashing with immense single-decade market concentration before shifting out of active tracking frames.

---

## 📽️ 3. Executive Storytelling & Historical Eras
Rather than presenting stakeholders with a list of 1,100 generic rows, the data was grouped into **three premium visual chapters** within the presentation layer (`F1_Racing_Eras_Presentation.pptx`):

1. **The Pioneer Years (1950s—1970s):** Shifting from the foundations of Alfa Romeo to the technical, ground-effect revolutions of Lotus.
2. **The Turbo & Glory Years (1980s—1990s):** Isolating the high-octane rivalry eras of Alain Prost (51 wins) and Ayrton Senna (41 wins).
3. **The Modern Dominance Era (2000s—2025):** Quantifying the systemic, ultra-optimized dynasties of Ferrari, Red Bull, and Mercedes.

---

## 🎛️ 4. Interface Engineering & UI Blueprint
The frontend app (`F1_Figma_Dashboard_Wireframe.html`) is structured with a custom telemetry system engine built around the core visual parameters defined in Figma.

```css
/* Core Application System Accent Variables */
:root {
  --bg:      #080810;
  --bg2:     #0d0d1a;
  --red:     #e50914;
  --white:   #f0f0f0;
  --mclaren: #ff8000;
  --redbull: #3671c6;
  --merc:    #00d2be;
}
