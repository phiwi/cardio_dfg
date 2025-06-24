---
theme: seriph
colorSchema: all
highlighter: shiki
lineNumbers: true
transition: slide-left
title: CARDIO:DE++ – Powering Next-Generation Cardiovascular AI
info: >
  A funding proposal summary for a multi-modal German clinical corpus project.
layout: cover
background: |
  linear-gradient(135deg, #0f2027 80%, #1976d2 100%),
  url('https://www.transparenttextures.com/patterns/cubes.png')
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');
.slidev-layout {
  background:
    radial-gradient(ellipse at 60% 20%, #00bcd455 0%, #0f202700 70%),
    linear-gradient(120deg, #0f2027 80%, #1976d2 100%),
    url('https://www.transparenttextures.com/patterns/cubes.png');
  color: #e3f0fa;
  font-family: 'Montserrat', Arial, sans-serif;
  /* Animate only the linear-gradient layer (second layer) */
  background-size: 100% 100%, 300% 300%, auto;
  background-position: 0 0, 0% 50%, 0 0;
  animation: gradientMove 24s ease-in-out infinite;
}
h1, h2, h3 {
  color: #00bcd4;
  font-family: 'Montserrat', Arial, sans-serif;
  letter-spacing: 0.02em;
}
a {
  color: #90caf9;
}
</style>

<div style="display: flex; flex-direction: column; align-items: center; justify-content: flex-start; min-height: 100vh; text-align: center; margin-top: 8vh;">

  <h1 style="font-size: 2.8em; color: #00bcd4; margin-bottom: 0.2em; text-shadow: 0 2px 12px #0f2027cc;">
    CARDIO:DE++
  </h1>
  <h3 style="color: #e3f0fa; margin-bottom: 0.7em; text-shadow: 0 2px 8px #1976d2cc;">
    Powering Next-Generation Cardiovascular AI<br>
    <span style="font-size: 0.7em; color: #90caf9;">with a Rich, Multi-Modal German Clinical Corpus</span>
  </h3>

  <!-- Animated, responsive ECG heartbeat line -->
  <div style="width: 100%; margin: 1.2em 0 1.2em 0; overflow: hidden; position: relative; height: 54px;">
    <svg
      v-motion="{
        initial: { x: 0, opacity: 0.18 },
        enter: { 
          x: [-800, 0], // animate from -800 to 0
          opacity: [0.18, 0.45, 0.18], 
          transition: { 
            duration: 3200, 
            times: [0, 0.5, 1], 
            repeat: Infinity, 
            repeatType: 'loop', 
            ease: 'linear' 
          }
        }
      }"
      width="200%" height="54" viewBox="0 0 3200 54" fill="none"
      style="display: block; position: absolute; left: 0; top: 0; min-width: 200%;">
      <path
        d="M0,40 
           L100,40 Q110,40 115,24 Q120,8 125,40 L200,40 Q210,40 213,36 Q216,32 219,40 L240,40
           Q243,40 246,25 Q249,10 252,40 L300,40 Q310,40 312,20 Q314,0 316,40 L318,40 Q319,45 320,10 Q321,5 322,40 L400,40
           L500,40 Q510,40 515,24 Q520,8 525,40 L600,40 Q610,40 613,36 Q616,32 619,40 L640,40
           Q643,40 646,25 Q649,10 652,40 L700,40 Q710,40 712,20 Q714,0 716,40 L718,40 Q719,45 720,10 Q721,5 722,40 L800,40
           L900,40 Q910,40 915,24 Q920,8 925,40 L1000,40 Q1010,40 1013,36 Q1016,32 1019,40 L1040,40
           Q1043,40 1046,25 Q1049,10 1052,40 L1100,40 Q1110,40 1112,20 Q1114,0 1116,40 L1118,40 Q1119,45 1120,10 Q1121,5 1122,40 L1200,40
           L1300,40 Q1310,40 1315,24 Q1320,8 1325,40 L1400,40 Q1410,40 1413,36 Q1416,32 1419,40 L1440,40
           Q1443,40 1446,25 Q1449,10 1452,40 L1500,40 Q1510,40 1512,20 Q1514,0 1516,40 L1518,40 Q1519,45 1520,10 Q1521,5 1522,40 L1600,40
           M1600,40 
           L1700,40 Q1710,40 1715,24 Q1720,8 1725,40 L1800,40 Q1810,40 1813,36 Q1816,32 1819,40 L1840,40
           Q1843,40 1846,25 Q1849,10 1852,40 L1900,40 Q1910,40 1912,20 Q1914,0 1916,40 L1918,40 Q1919,45 1920,10 Q1921,5 1922,40 L2000,40
           L2100,40 Q2110,40 2115,24 Q2120,8 2125,40 L2200,40 Q2210,40 2213,36 Q2216,32 2219,40 L2240,40
           Q2243,40 2246,25 Q2249,10 2252,40 L2300,40 Q2310,40 2312,20 Q2314,0 2316,40 L2318,40 Q2319,45 2320,10 Q2321,5 2322,40 L2400,40
           L2500,40 Q2510,40 2515,24 Q2520,8 2525,40 L2600,40 Q2610,40 2613,36 Q2616,32 2619,40 L2640,40
           Q2643,40 2646,25 Q2649,10 2652,40 L2700,40 Q2710,40 2712,20 Q2714,0 2716,40 L2718,40 Q2719,45 2720,10 Q2721,5 2722,40 L2800,40
           L2900,40 Q2910,40 2915,24 Q2920,8 2925,40 L3000,40 Q3010,40 3013,36 Q3016,32 3019,40 L3040,40
           Q3043,40 3046,25 Q3049,10 3052,40 L3100,40 Q3110,40 3112,20 Q3114,0 3116,40 L3118,40 Q3119,45 3120,10 Q3121,5 3122,40 L3200,40"
        stroke="#ff4081"
        stroke-width="4"
        fill="none"
      />
    </svg>
  </div>

  <div style="color: #e3f0fa; font-size: 1.1em; margin-bottom: 0.5em;">
    <b>Philipp Wiesenbach, Prof. Christoph Dieterich, Prof. Nicolas Geis (UKHD)</b><br>
    <b>Simone Britsch, <em>tbd.</em>, Prof. Daniel Dürschmied (UMM)</b><br>
  </div>
</div>

---

## <span class="section-title">Motivation</span>

<!-- Animated, left-aligned ECG line that scrolls and fades in/out -->

<div style="height: 1.5em;"></div>

<ul style="list-style: disc inside; padding-left: 0;">
  <li>
    <span style="display: inline-flex; align-items: center;">
      Scarcity of high-quality, freely accessible German clinical text corpora
      <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f4dd.png" alt="document" width="22" height="22" style="vertical-align: middle; margin-left: 0.6em;">
    </span>
  </li>
  <li>
    <span style="display: inline-flex; align-items: center;">
      Strict data protection (GDPR) limits data sharing
      <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f512.png" alt="lock" width="22" height="22" style="vertical-align: middle; margin-left: 0.6em;">
    </span>
  </li>
  <li>
    <span style="display: inline-flex; align-items: center;">
      Existing English corpora (e.g., MIMIC-III, i2b2) have driven clinical NLP
      <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f30e.png" alt="globe" width="22" height="22" style="vertical-align: middle; margin-left: 0.6em;">
    </span>
  </li>
  <li>
    <span style="display: inline-flex; align-items: center;">
      German resources are limited and lack multi-modal, parallel data
      <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f50d.png" alt="magnifier" width="22" height="22" style="vertical-align: middle; margin-left: 0.6em;">
    </span>
  </li>
</ul>

<div style="height: 5.5em;"></div>

```mermaid
flowchart TD
    A["Scarcity of German<br>  clinical corpora"]
    B["Strict GDPR/data<br>  protection"]
    C["English corpora <br> drive progress"]
    D["German resources lack<br>  multi-modality"]
    E["Need for CARDIO:DE++"]

    A --> E
    B --> E
    C --> E
    D --> E

    classDef default fill:#e3f0fa,stroke:#1976d2,stroke-width:2px,color:#1976d2;
    classDef E fill:#1976d2,stroke:#0f2027,stroke-width:3px,color:#fff;
```



---

## <span class="section-title">State of the Art</span>

<div style="height: 1.5em;"></div>

<div style="display: flex; flex-wrap: wrap; align-items: flex-start; justify-content: space-between; width: 100%;">
  <div style="flex: 1 1 320px; min-width: 260px; max-width: 480px; margin-right: 2vw;">
    <ul>
      <li><b>English corpora:</b> MIMIC-III, MIMIC-IV-Note, i2b2, CLEF, SemEval, THYME</li>
      <li><b>European corpora:</b> MERLOT (French), IULA (Spanish)</li>
      <li><b>German corpora:</b> GGPONC 2.0, 200 Oncological Discharge Summaries, GRASSCO, JSynCC</li>
      <li><b>Gap:</b> No large, multi-modal, parallel German cardiovascular corpus</li>
    </ul>
  </div>
  <div style="flex: 0 1 440px; min-width: 220px; max-width: 33vw; display: flex; flex-direction: column; align-items: flex-end;">
    <img src="https://media.springernature.com/full/springer-static/image/art%3A10.1038%2Fsdata.2016.35/MediaObjects/41597_2016_Article_BFsdata201635_Fig2_HTML.jpg"
         alt="MIMIC-III Database Logo"
         style="width: 100%; max-width: 440px; max-height: 38vh; border-radius: 12px; box-shadow: 0 4px 24px #1976d288; object-fit: contain; margin-left: 2vw;">
    <div style="color: #90caf9; font-size: 0.95em; margin-top: 0.5em; text-align: right;">
      <i>MIMIC-III: A leading English clinical corpus.<br>
      Source: <a href="https://physionet.org/content/mimiciii/1.4/" target="_blank" style="color:#90caf9;">PhysioNet</a></i>
    </div>
  </div>
</div>

---

## <span class="section-title">Preliminary Work</span>

<div style="height: 1.5em;"></div>

<div style="display: flex; flex-wrap: wrap; align-items: flex-start; justify-content: space-between; width: 100%;">
  <div style="flex: 1 1 320px; min-width: 260px; max-width: 480px; margin-right: 2vw;">
    <ul>
      <li>Developed de-identification and NER methods for German medical texts</li>
      <li>Achieved F2-scores up to 96% for de-identification</li>
      <li>Created and published the CARDIO:DE corpus:
        <ul>
          <li>500 cardiovascular doctor's letters</li>
          <li>993,143 tokens, 31,952 unique tokens</li>
          <li>High-quality medication and section annotations</li>
        </ul>
      </li>
      <li>CARDIO:DE is freely available for research</li>
    </ul>
  </div>
  <div style="flex: 0 1 440px; min-width: 220px; max-width: 33vw; display: flex; flex-direction: column; align-items: flex-end;">
    <img src="https://media.springernature.com/lw685/springer-static/image/art%3A10.1038%2Fs41597-023-02128-9/MediaObjects/41597_2023_2128_Fig3_HTML.png"
         alt="CARDIO:DE Figure 3: Annotation statistics and inter-annotator agreement"
         style="width: 100%; max-width: 440px; max-height: 38vh; border-radius: 12px; box-shadow: 0 4px 24px #1976d288; object-fit: contain; margin-left: 2vw;">
    <div style="color: #90caf9; font-size: 0.95em; margin-top: 0.5em; text-align: right;">
      <i>Figure 3: CARDIO:DE annotation statistics and inter-annotator agreement.<br>
      Source: <a href="https://www.nature.com/articles/s41597-023-02128-9" target="_blank" style="color:#90caf9;">Richter-Pechanski et al., Scientific Data 2023</a></i>
    </div>
  </div>
</div>

---

## <span class="section-title">Why CARDIO:DE++?</span>

<div style="height: 1.5em;"></div>

<ul style="list-style: disc inside; padding-left: 0;">
  <li>
    <span style="display: inline-flex; align-items: center;">
      Existing corpora lack:
      <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/26a0.png" alt="warning" width="22" height="22" style="vertical-align: middle; margin-left: 0.6em;">
    </span>
    <ul>
      <li>
        <span style="display: inline-flex; align-items: center;">
          Multi-site data (risk of site bias)
          <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f465.png" alt="people" width="18" height="18" style="vertical-align: middle; margin-left: 0.5em;">
        </span>
      </li>
      <li>
        <span style="display: inline-flex; align-items: center;">
          Explicitly parallel, structured tabular data
          <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f4c8.png" alt="chart" width="18" height="18" style="vertical-align: middle; margin-left: 0.5em;">
        </span>
      </li>
    </ul>
  </li>
  <li>
    <span style="display: inline-flex; align-items: center;">
      CARDIO:DE++ will:
      <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f680.png" alt="rocket" width="22" height="22" style="vertical-align: middle; margin-left: 0.6em;">
    </span>
    <ul>
      <li>
        <span style="display: inline-flex; align-items: center;">
          Add data from Universitätsklinikum Mannheim
          <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f3e5.png" alt="hospital" width="18" height="18" style="vertical-align: middle; margin-left: 0.5em;">
        </span>
      </li>
      <li>
        <span style="display: inline-flex; align-items: center;">
          Link free-text with structured clinical parameters
          <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f517.png" alt="link" width="18" height="18" style="vertical-align: middle; margin-left: 0.5em;">
        </span>
      </li>
      <li>
        <span style="display: inline-flex; align-items: center;">
          Enable advanced text-to-data and data-to-text AI models
          <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f916.png" alt="robot" width="18" height="18" style="vertical-align: middle; margin-left: 0.5em;">
        </span>
      </li>
    </ul>
  </li>
</ul>

---

## <span class="section-title">Project Objectives</span>

<div style="height: 1.5em;"></div>

<div class="vcenter">
<ul>
  <li><b>Expand corpus heterogeneity:</b><br> Add 500 new de-identified discharge letters from two sites</li>
  <li><b>Integrate structured tabular data:</b><br> Laboratory values, vital signs, ICD-10 codes, procedures, medications</li>
  <li><b>Enable advanced AI research:</b>
    <ul>
      <li>Synthetic data generation</li>
      <li>Data-to-text and text-to-data NLP</li>
      <li>Patient phenotyping and subgroup discovery</li>
    </ul>
  </li>
</ul>
</div>

---

## <span class="section-title">CARDIO:DE++ Enhancements</span>

<div style="height: 1.5em;"></div>

```mermaid
%%{init: {'themeVariables': { 'fontSize': '13px', 'nodePadding': '10', 'nodeSpacing': '20' }}}%%
flowchart LR
    subgraph CARDIO_DE["CARDIO:DE Corpus"]
      A1["500 Cardiovascular Discharge Letters<br/>(Heidelberg)"]
      A2["Manual Annotations:<br/>Medication, Sections"]
    end

    subgraph EXT["Enhancements"]
      B1["+500 Discharge Letters<br/>(Heidelberg & Mannheim)"]
      B2["Parallel Tabular Data:<br/>Labs, Vitals, ICD-10, Procedures, Meds"]
    end

    subgraph CARDIO_DEPP["CARDIO:DE++"]
      C1["1,000 Letters<br/>(2 Sites)"]
      C2["Multi-Modal:<br/>Text + Structured Data"]
      C3["Expanded Annotations"]
    end

    CARDIO_DE --> EXT
    EXT --> CARDIO_DEPP
``` 

<!-- 
```mermaid
%%{init: {'themeVariables': { 'fontSize': '13px', 'nodePadding': '10', 'nodeSpacing': '40' }}}%%
flowchart TD
    A1["CARDIO:DE Corpus<br><span style='font-size:0.8em'>500 Letters (Heidelberg)<br>Manual Annotations</span>"]
    B1["+500 Letters<br>(Heidelberg & Mannheim)"]
    B2["Parallel Tabular Data<br>(Labs, Vitals, ICD-10,<br> Procedures, Meds)"]
    C1["CARDIO:DE++<br><span style='font-size:0.8em'>1,000 Letters (2 Sites)<br>Multi-Modal: Text + Structured Data<br>Expanded Annotations</span>"]

    A1 --> B1
    A1 --> B2
    B1 --> C1
    B2 --> C1
```
-->


## <span class="section-title">CARDIO:DE++ Enablements</span>

<div style="height: 1.5em;"></div>

```mermaid
flowchart TD
    A["<b>🧬<br>CARDIO:DE++<br>Multi-Modal Corpus</b>"]:::main
    B1["🤖<br>Robust, Generalizable<br>AI Models"]:::ai
    B2["🧑‍⚕️<br>Improved Clinical<br>Decision Support"]:::clinical
    B3["🧪<br>Synthetic Data<br>Generation"]:::synth
    B4["🔄<br>Data-to-Text &<br>Text-to-Data"]:::datatext
    B5["🧬<br>Advanced Patient<br>Phenotyping"]:::pheno
    B6["🤝<br>Collaborative Research<br>& Shared Tasks"]:::collab

    A --> B1
    A --> B2
    A --> B3
    A --> B4
    A --> B5
    A --> B6

    classDef main fill:#1976d2,stroke:#0f2027,stroke-width:3px,color:#fff,stroke-dasharray: 0;
    classDef ai fill:#e3f2fd,stroke:#1976d2,stroke-width:2px,color:#1976d2,stroke-dasharray: 0;
    classDef clinical fill:#e1f5fe,stroke:#00bcd4,stroke-width:2px,color:#1976d2,stroke-dasharray: 0;
    classDef synth fill:#f3e5f5,stroke:#ab47bc,stroke-width:2px,color:#6a1b9a,stroke-dasharray: 0;
    classDef datatext fill:#fffde7,stroke:#ffd600,stroke-width:2px,color:#1976d2,stroke-dasharray: 0;
    classDef pheno fill:#e8f5e9,stroke:#388e3c,stroke-width:2px,color:#1976d2,stroke-dasharray: 0;
    classDef collab fill:#fce4ec,stroke:#d81b60,stroke-width:2px,color:#1976d2,stroke-dasharray: 0;
```

---

## <span class="section-title">Work Packages Overview</span>

<div style="height: 1.5em;"></div>

| WP  | Title                                   | Months      |
|-----|-----------------------------------------|-------------|
| WP1 | Ethics, Legal Framework & Onboarding    | 1–3         |
| WP2 | Data Acquisition                        | 1–12        |
| WP3 | De-identification                       | 2–12        |
| WP4 | Annotation                              | 6–24        |
| WP5 | Advanced AI Model Development           | 19–23       |
| WP6 | Dissemination & Sustainability          | 19–24       |

---

## <span class="section-title">WP1: Ethics, Legal Framework & Site Onboarding</span>

<div style="height: 1.5em;"></div>

<div class="vcenter">
<ul>
  <li><b>Months:</b> 1–3</li>
  <li><b>Objective:</b> Secure ethical/legal approvals and establish data sharing protocols</li>
  <li><b>Key Tasks:</b>
    <ul>
      <li>Ethics applications for both sites</li>
      <li>Standardized patient consent forms</li>
      <li>Data Use/Transfer Agreements (DUAs/DTAs)</li>
      <li>SOPs for data handling and training</li>
    </ul>
  </li>
  <li><b>Deliverables:</b> Approved ethics, signed DUAs/DTAs, consent forms, SOPs</li>
  <li><b>Lead:</b> Heidelberg (with UMM)</li>
</ul>
<div style="margin-top: 1.2em; font-size: 1em; background: linear-gradient(90deg, #1976d222 60%, #00bcd422 100%); border-left: 6px solid #1976d2; box-shadow: 0 2px 12px #1976d244; padding: 1em 1.2em; border-radius: 12px; display: flex; align-items: flex-start;">
  <span style="font-size: 1.6em; margin-right: 0.7em; margin-top: -0.1em;">📚</span>
  <span>
    <b style="font-weight: 600; color: #1976d2;">Further reading:</b>
    <ul style="margin: 0.3em 0 0 0.7em;">
      <li>
        <a href="https://gdpr.eu/" target="_blank">GDPR (General Data Protection Regulation)</a>
      </li>
    </ul>
  </span>
</div>
</div>

---

## <span class="section-title">WP2: Data Acquisition</span>

<div style="height: 1.5em;"></div>

<div class="vcenter">
<ul>
  <li><b>Months:</b> 1–12</li>
  <li><b>Objective:</b> Collect 500 new discharge letters and structured tabular data</li>
  <li><b>Key Tasks:</b>
    <ul>
      <li>Patient consent and data collection at both sites</li>
      <li>Finalize list of structured data points (labs, ICD-10, vitals, meds, procedures)</li>
      <li>Extract and link data for each letter</li>
    </ul>
  </li>
  <li><b>Deliverables:</b> 500 raw discharge letters + structured data</li>
  <li><b>Lead:</b> Heidelberg & UMM</li>
</ul>
<div style="margin-top: 1.2em; font-size: 1em; background: linear-gradient(90deg, #1976d222 60%, #00bcd422 100%); border-left: 6px solid #1976d2; box-shadow: 0 2px 12px #1976d244; padding: 1em 1.2em; border-radius: 12px; display: flex; align-items: flex-start;">
  <span style="font-size: 1.6em; margin-right: 0.7em; margin-top: -0.1em;">📝</span>
  <span>
    <b style="font-weight: 600; color: #1976d2;">Reference:</b>
    <a href="https://www.nature.com/articles/sdata201635" target="_blank">
      Johnson AEW et al., MIMIC-III Data Collection Protocol, Scientific Data (2016)
    </a>
  </span>
</div>
</div>

---

## <span class="section-title">WP3: De-identification</span>

<div style="height: 1.5em;"></div>

<div class="vcenter">
<ul>
  <li><b>Months:</b> 2–12</li>
  <li><b>Objective:</b> De-identify all textual and tabular data</li>
  <li><b>Key Tasks:</b>
    <ul>
      <li>Apply/refine CARDIO:DE de-identification models</li>
      <li>Manual review and correction</li>
      <li>Clean, standardize, and anonymize tabular data</li>
    </ul>
  </li>
  <li><b>Deliverables:</b> 500 de-identified letters, linked tabular data, quality report</li>
  <li><b>Lead:</b> Heidelberg</li>
</ul>
<div style="margin-top: 1.2em; font-size: 1em; background: linear-gradient(90deg, #1976d222 60%, #00bcd422 100%); border-left: 6px solid #1976d2; box-shadow: 0 2px 12px #1976d244; padding: 1em 1.2em; border-radius: 12px; display: flex; align-items: flex-start;">
  <span style="font-size: 1.6em; margin-right: 0.7em; margin-top: -0.1em;">🔒</span>
  <span>
    <b style="font-weight: 600; color: #1976d2;">Key resource:</b>
    <a href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2995716/" target="_blank">
      Meystre et al., Review of De-identification Techniques for Clinical Text, JAMIA (2010)
    </a>
  </span>
</div>
</div>

---

## <span class="section-title">WP4: Annotation</span>

<div style="height: 1.5em;"></div>

<div class="vcenter">
<ul>
  <li><b>Months:</b> 6–24</li>
  <li><b>Objective:</b> Annotate new data using established schemes</li>
  <li><b>Key Tasks:</b>
    <ul>
      <li>Apply CARDIO:DE annotation schemes (medication, section classes)</li>
      <li>Inter-annotator agreement studies</li>
      <li>Link text to tabular data via anonymized IDs</li>
      <li>(Optional) Explore explicit text-to-table linking</li>
    </ul>
  </li>
  <li><b>Deliverables:</b> Annotated CARDIO:DE++ corpus, guidelines, reports, splits</li>
  <li><b>Lead:</b> Heidelberg</li>
</ul>
<div style="margin-top: 1.2em; font-size: 1em; background: linear-gradient(90deg, #1976d222 60%, #00bcd422 100%); border-left: 6px solid #1976d2; box-shadow: 0 2px 12px #1976d244; padding: 1em 1.2em; border-radius: 12px; display: flex; align-items: flex-start;">
  <span style="font-size: 1.6em; margin-right: 0.7em; margin-top: -0.1em;">🖊️</span>
  <span>
    <b style="font-weight: 600; color: #1976d2;">See also:</b>
    <a href="https://www.nature.com/articles/s41597-023-02128-9" target="_blank">
      CARDIO:DE Corpus Publication (Richter-Pechanski et al., 2023)
    </a>
  </span>
</div>
</div>

---

## <span class="section-title">WP5: Advanced AI Model Development</span>

<div style="height: 1.5em;"></div>

<div class="vcenter">
<ul>
  <li><b>Months:</b> 19–23</li>
  <li><b>Objective:</b> Develop and evaluate advanced AI models</li>
  <li><b>Key Tasks:</b>
    <ul>
      <li>Fine-tune LLMs for synthetic data</li>
      <li>Develop data-to-text & text-to-data models</li>
      <li>Patient phenotyping with multi-modal data</li>
    </ul>
  </li>
  <li><b>Deliverables:</b> Synthetic letters, evaluated models, phenotyping reports</li>
  <li><b>Lead:</b> Heidelberg</li>
</ul>
<div style="margin-top: 1.2em; font-size: 1em; background: linear-gradient(90deg, #1976d222 60%, #00bcd422 100%); border-left: 6px solid #1976d2; box-shadow: 0 2px 12px #1976d244; padding: 1em 1.2em; border-radius: 12px; display: flex; align-items: flex-start;">
  <span style="font-size: 1.6em; margin-right: 0.7em; margin-top: -0.1em;">🤖</span>
  <span>
    <b style="font-weight: 600; color: #1976d2;">Further reading:</b>
    <a href="https://arxiv.org/abs/2305.09617" target="_blank">
      Med-PaLM: Towards Expert-Level Medical Question Answering with Large Language Models
    </a>
  </span>
</div>
</div>

---

## <span class="section-title">WP6: Dissemination, Publication & Sustainability</span>

<div style="height: 1.5em;"></div>

<div class="vcenter">
<ul>
  <li><b>Months:</b> 19–24</li>
  <li><b>Objective:</b> Maximize impact and ensure sustainability</li>
  <li><b>Key Tasks:</b>
    <ul>
      <li>Public release of CARDIO:DE++ corpus</li>
      <li>Documentation and usage examples</li>
      <li>Peer-reviewed publications and workshops</li>
      <li>Long-term maintenance plan</li>
    </ul>
  </li>
  <li><b>Deliverables:</b> Released corpus, documentation, publications, sustainability plan</li>
  <li><b>Lead:</b> Heidelberg</li>
</ul>
<div style="margin-top: 1.2em; font-size: 1em; background: linear-gradient(90deg, #1976d222 60%, #00bcd422 100%); border-left: 6px solid #1976d2; box-shadow: 0 2px 12px #1976d244; padding: 1em 1.2em; border-radius: 12px; display: flex; align-items: flex-start;">
  <span style="font-size: 1.6em; margin-right: 0.7em; margin-top: -0.1em;">🌐</span>
  <span>
    <b style="font-weight: 600; color: #1976d2;">Open Science & FAIR Data:</b>
    <a href="https://www.go-fair.org/fair-principles/" target="_blank">
      FAIR Data Principles
    </a>
  </span>
</div>
</div>

---

## <span class="section-title">Timeline working packages</span>

<div style="height: 1.5em;"></div>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');
.vcenter {
  display: flex;
  flex-direction: column;
  justify-content: center;
  min-height: 70vh;
}
.centered-list ul, .vcenter ul {
  margin: 0 auto;
  padding: 1.5em 2.5em;
  background: rgba(15,32,39,0.10);
  border-radius: 18px;
  box-shadow: 0 2px 16px 0 rgba(25,118,210,0.07);
  font-size: 1.18em;
  color: #e3f0fa;
  max-width: 700px;
}
.timeline-table {
  border-collapse: collapse;
  font-size: 12px;
  margin: 0 auto;
  font-family: 'Montserrat', Arial, sans-serif;
}
.timeline-table th, .timeline-table td {
  border: 1px solid #1e293b;
  padding: 2px 4px;
  text-align: center;
  min-width: 16px;
  height: 18px;
}
.timeline-table th {
  background: #0d1b2a;
  font-weight: bold;
  color: #90caf9;
}
.timeline-bar {
  background: linear-gradient(90deg, #1976d2 0%, #00bcd4 100%);
  border-radius: 4px;
}
.timeline-empty {
  background: #0a192f;
}
.timeline-label {
  font-weight: bold;
  background: #112d4e;
  color: #90caf9;
}
.timeline-legend {
  margin: 18px auto 0 auto;
  max-width: 600px;
  font-size: 13px;
  text-align: left;
  font-family: 'Montserrat', Arial, sans-serif;
}
.timeline-legend-table {
  border-collapse: collapse;
  width: 100%;
  margin-top: 8px;
}
.timeline-legend-table td {
  padding: 2px 8px;
  border: none;
  vertical-align: top;
}
.timeline-legend-wp {
  font-weight: bold;
  color: #00bcd4;
  min-width: 36px;
  display: inline-block;
}
</style>

<table class="timeline-table">
  <tr>
    <th></th>
    <th>1</th><th>2</th><th>3</th><th>4</th><th>5</th><th>6</th><th>7</th><th>8</th><th>9</th><th>10</th><th>11</th><th>12</th>
    <th>13</th><th>14</th><th>15</th><th>16</th><th>17</th><th>18</th><th>19</th><th>20</th><th>21</th><th>22</th><th>23</th><th>24</th>
  </tr>
  <tr>
    <td class="timeline-label">WP1</td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-bar"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
  </tr>
  <tr>
    <td class="timeline-label">WP2</td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-bar"></td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-bar"></td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-bar"></td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-bar"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
  </tr>
  <tr>
    <td class="timeline-label">WP3</td>
    <td class="timeline-empty"></td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-bar"></td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-bar"></td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-bar"></td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
  </tr>
  <tr>
    <td class="timeline-label">WP4</td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-bar"></td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-bar"></td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-bar"></td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-bar"></td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-bar"></td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-bar"></td>
    <td class="timeline-bar"></td>
  </tr>
  <tr>
    <td class="timeline-label">WP5</td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-bar"></td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-empty"></td>
  </tr>
  <tr>
    <td class="timeline-label">WP6</td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-bar"></td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-bar"></td>
  </tr>
</table>

<div class="timeline-legend">
  <b>Legend:</b>
  <table class="timeline-legend-table">
    <tr>
      <td class="timeline-legend-wp">WP1</td>
      <td>Ethics, Legal Framework & Site Onboarding</td>
    </tr>
    <tr>
      <td class="timeline-legend-wp">WP2</td>
      <td>Data Acquisition</td>
    </tr>
    <tr>
      <td class="timeline-legend-wp">WP3</td>
      <td>De-identification</td>
    </tr>
    <tr>
      <td class="timeline-legend-wp">WP4</td>
      <td>Annotation</td>
    </tr>
    <tr>
      <td class="timeline-legend-wp">WP5</td>
      <td>Advanced AI Model Development</td>
    </tr>
    <tr>
      <td class="timeline-legend-wp">WP6</td>
      <td>Dissemination, Publication & Sustainability</td>
    </tr>
  </table>
</div>



---

## <span class="section-title">Summary: Expected Impact</span>

<div style="height: 1.5em;"></div>

<div style="position: relative; min-height: 55vh;">

  <ul style="list-style: disc inside; padding-left: 0; position: relative; z-index: 1;">
    <li v-motion="{
          initial: { opacity: 0, x: -40 },
          enter: { opacity: 1, x: 0, transition: { delay: 200, duration: 1200 } }
        }"
        style="margin-bottom: 1.2em; display: flex; align-items: center;">
      <span style="display: inline-flex; align-items: center;">
        First large, multi-modal, parallel German cardiovascular corpus
        <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f4c8.png" alt="chart" width="28" height="28" style="vertical-align: middle; margin-left: 0.7em;">
      </span>
    </li>
    <li v-motion="{
          initial: { opacity: 0, x: -40 },
          enter: { opacity: 1, x: 0, transition: { delay: 900, duration: 1200 } }
        }"
        style="margin-bottom: 1.2em; display: flex; align-items: center;">
      <span style="display: inline-flex; align-items: center;">
        Enables robust, generalizable AI models for clinical NLP
        <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f916.png" alt="robot" width="28" height="28" style="vertical-align: middle; margin-left: 0.7em;">
      </span>
    </li>
    <li v-motion="{
          initial: { opacity: 0, x: -40 },
          enter: { opacity: 1, x: 0, transition: { delay: 1600, duration: 1200 } }
        }"
        style="margin-bottom: 1.2em; display: flex; align-items: center;">
      <span style="display: inline-flex; align-items: center;">
        Supports synthetic data generation and advanced patient phenotyping
        <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f9ec.png" alt="dna" width="28" height="28" style="vertical-align: middle; margin-left: 0.7em;">
      </span>
    </li>
    <li v-motion="{
          initial: { opacity: 0, x: -40 },
          enter: { opacity: 1, x: 0, transition: { delay: 2300, duration: 1200 } }
        }"
        style="margin-bottom: 1.2em; display: flex; align-items: center;">
      <span style="display: inline-flex; align-items: center;">
        Fosters collaboration and innovation in German-speaking clinical NLP
        <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f91d.png" alt="handshake" width="28" height="28" style="vertical-align: middle; margin-left: 0.7em;">
      </span>
    </li>
  </ul>
</div>
---

<div style="display: flex; flex-direction: column; align-items: center; min-height: 100vh;">

  <!-- Animated "Thank you!" slogan near the top -->
  <div
    v-motion="{
      initial: { opacity: 0, y: -60, scale: 0.93 },
      enter: { opacity: 1, y: 0, scale: 1.08, transition: { delay: 200, duration: 1200, ease: 'easeOut' } }
    }"
    style="font-size: 3.2em; font-weight: 800; color: #00bcd4; text-shadow: 0 4px 28px #1976d2cc, 0 2px 0 #fff; letter-spacing: 0.05em; margin-top: 7vh; margin-bottom: 2.2em; text-align: center;">
    Thank you!
  </div>

  <!-- Animated pulsing heart SVG, centered below the slogan -->
  <svg
    v-motion="{
      initial: { scale: 1, opacity: 0.10 },
      enter: { scale: 1.18, opacity: 0.18, transition: { repeat: Infinity, repeatType: 'reverse', duration: 1800, ease: 'easeInOut' } }
    }"
    width="180" height="180" viewBox="0 0 24 24" fill="none"
    style="margin-bottom: 0;">
    <path
      fill="#ff4081"
      stroke="#1976d2"
      stroke-width="2.2"
      stroke-linecap="round"
      stroke-linejoin="round"
      d="M12 21s-6.5-5.05-9.14-8.13C1.09 10.2 1 7.36 3.05 5.32a6.23 6.23 0 0 1 8.82 0l.13.13.13-.13a6.23 6.23 0 0 1 8.82 0c2.05 2.04 1.96 4.88.19 7.55C18.5 15.95 12 21 12 21z"
    />
  </svg>

</div>