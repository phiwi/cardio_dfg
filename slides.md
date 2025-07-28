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

/* --- ECG Monitor Animation Styles --- */

@keyframes draw-and-fade {
  from { mask-position: 100% 0; -webkit-mask-position: 100% 0; }
  to { mask-position: 0% 0; -webkit-mask-position: 0% 0; }
}

.ecg-monitor-container {
  width: 100%;
  margin: 1.2em 0;
  overflow: hidden;
  position: relative;
  height: 60px;
}

.ecg-monitor-svg {
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  
  /* The animated mask that creates the drawing effect */
  mask-size: 200% 100%;
  mask-image: linear-gradient(to right,
    transparent 35%,
    rgba(0,0,0,0.8) 45%,
    black 49%,
    transparent 50%
  );
  
  -webkit-mask-size: 200% 100%;
  -webkit-mask-image: linear-gradient(to right,
    transparent 35%,
    rgba(0,0,0,0.8) 45%,
    black 49%,
    transparent 50%
  );

  animation: draw-and-fade 5s linear infinite;
}
.themed-icon {
  color: #ff4081;
  font-size: 1.4em;
  margin-left: 0.6em;
  vertical-align: -0.2em;
}
.diagram-layer {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  transition: opacity 0.5s ease-in-out;
}
.unroll-container .mermaid {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
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

  <!-- ECG Monitor Container -->
  <div class="ecg-monitor-container">
    <svg class="ecg-monitor-svg" viewBox="0 0 800 60" fill="none">
      <!-- The static ECG path that is revealed by the mask -->
      <path
        d="M-100,30 L0,30 C5,30 8,26 12,30 L20,30 L25,33 L35,5 L42,58 L50,30 L70,30 C80,30 90,18 105,30 L200,30 C205,30 208,26 212,30 L220,30 L225,33 L235,5 L242,58 L250,30 L270,30 C280,30 290,18 305,30 L400,30 C405,30 408,26 412,30 L420,30 L425,33 L435,5 L442,58 L450,30 L470,30 C480,30 490,18 505,30 L600,30 C605,30 608,26 612,30 L620,30 L625,33 L635,5 L642,58 L650,30 L670,30 C680,30 690,18 705,30 L800,30 L900,30"
        stroke="#ff4081"
        stroke-width="2.5"
        stroke-linecap="round"
        fill="none"
        opacity="0.6"
      />
      <!-- The <circle> element has been removed -->
    </svg>
  </div>

  <div style="color: #e3f0fa; font-size: 1.1em; margin-bottom: 0.5em;">
    <b>Philipp Wiesenbach, Prof. Christoph Dieterich, Prof. Nicolas Geis (UKHD)</b><br>
    <b>Simone Britsch (UMM)<em>tbd.</em></b><br>
  </div>
</div>

---

<div class="section-title">Motivation</div>

<div style="height: 1.5em;"></div>

<ul class="themed-list">
  <li>
    <span style="display: inline-flex; align-items: center;">
      Scarcity of high-quality, freely accessible German clinical text corpora
      <div class="i-carbon-document themed-icon" />
    </span>
  </li>
  <li>
    <span style="display: inline-flex; align-items: center;">
      Strict data protection (GDPR) limits data sharing
      <div class="i-carbon-locked themed-icon" />
    </span>
  </li>
  <li>
    <span style="display: inline-flex; align-items: center;">
      Existing English corpora (e.g., MIMIC-III, i2b2) have driven clinical NLP
      <div class="i-carbon-language themed-icon" />
    </span>
  </li>
  <li>
    <span style="display: inline-flex; align-items: center;">
      German resources are limited and lack multi-modal, parallel data
      <div class="i-carbon-search themed-icon" />
    </span>
  </li>
</ul>

<div style="height: 5.5em;"></div>


```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 
    'primaryColor': 'transparent', 
    'primaryTextColor': '#e3f0fa', 
    'lineColor': '#ff4081', 
    'textColor': '#e3f0fa', 
    'mainBkg': 'transparent', 
    'nodeBorder': '#ff4081' 
}}}%%
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

    style A,B,C,D stroke-width:2px
    style E stroke-width:3px,font-weight:bold
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

<!-- What is missing in existing corpora -->
<div v-click
  v-motion="{
    initial: { opacity: 0, y: 30 },
    enter: { opacity: 1, y: 0, transition: { duration: 1200 } }
  }"
  style="background: linear-gradient(90deg, #ff980022 60%, #ffeb3b22 100%); border-left: 6px solid #ff9800; border-radius: 10px; margin-bottom: 1.5em; padding: 1em 1.2em;"
>
  <b style="color: #ff9800; font-size: 1.1em;">Existing corpora lack:</b>
  <ul style="list-style: disc inside; padding-left: 0; margin-top: 0.6em;">
    <li>
      <span style="display: inline-flex; align-items: center;">
        Multi-site data (risk of site bias)
        <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f465.png" alt="people" width="18" height="18" style="vertical-align: middle; margin-left: 0.5em;">
      </span>
    </li>
    <li>
      <span style="display: inline-flex; align-items: center;">
        Explicitly parallel, multi-modal patient data
        <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f4c8.png" alt="chart" width="18" height="18" style="vertical-align: middle; margin-left: 0.5em;">
      </span>
    </li>
  </ul>
</div>

<!-- What CARDIO:DE++ will contribute -->
<div v-click
  v-motion="{
    initial: { opacity: 0, y: 30 },
    enter: { opacity: 1, y: 0, transition: { duration: 1200 } }
  }"
  style="background: linear-gradient(90deg, #1976d222 60%, #00bcd422 100%); border-left: 6px solid #1976d2; border-radius: 10px; padding: 1em 1.2em;"
>
  <b style="color: #1976d2; font-size: 1.1em;">CARDIO:DE++ will:</b>
  <ul style="list-style: disc inside; padding-left: 0; margin-top: 0.6em;">
    <li>
      <span style="display: inline-flex; align-items: center;">
        Collect 1,000 discharge letters collected from two sites (UKHD & UMM)
        <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f3e5.png" alt="hospital" width="18" height="18" style="vertical-align: middle; margin-left: 0.5em;">
      </span>
    </li>
    <li>
      <span style="display: inline-flex; align-items: center;">
        Collect data from differnt stays per patient enabling longitudinal analyes
        <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f3e5.png" alt="hospital" width="18" height="18" style="vertical-align: middle; margin-left: 0.5em;">
      </span>
    </li>
    <li>
      <span style="display: inline-flex; align-items: center;">
        Add a multitude of medical examination data per patient 
        <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f517.png" alt="link" width="18" height="18" style="vertical-align: middle; margin-left: 0.5em;">
      </span>
    </li>
    <li>
      <span style="display: inline-flex; align-items: center;">
        Actively steer the corpus design towards least exhibited bias
        <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f916.png" alt="robot" width="18" height="18" style="vertical-align: middle; margin-left: 0.5em;">
      </span>
    </li>
  </ul>
</div>

---

## <span class="section-title">Project Objectives</span>

<div style="height: 2.5em;"></div>

<!-- 
  This container uses flexbox to create a responsive 2x2 grid.
  - flex-grow: 1 allows it to fill the available vertical space.
  - The gap and padding on the items have been reduced to prevent overflow.
-->
<div style="flex-grow: 1; display: flex; gap: 1.5em; flex-wrap: wrap; justify-content: center; align-content: center;">

  <!-- O1: Enhance Corpus Heterogeneity -->
  <div v-click
    v-motion="{ initial: { opacity: 0, y: 40 }, enter: { opacity: 1, y: 0, transition: { duration: 800 } } }"
    style="background: linear-gradient(120deg, #1976d2 80%, #00bcd4 100%); color: #fff; border-radius: 14px; box-shadow: 0 2px 16px #1976d288; padding: 1em 1.2em; flex: 1 1 40%; max-width: 45%;">
    <span style="font-size: 1.8em; vertical-align: middle;">🧬</span>
    <b>Enhance Corpus Heterogeneity</b>
    <div style="font-size: 0.9em; margin-top: 0.5em;">Expand to 1,000 letters from two sites to build generalizable AI models and mitigate site-specific bias.</div>
  </div>

  <!-- O2: Enable Longitudinal Assessment -->
  <div v-click
    v-motion="{ initial: { opacity: 0, y: 40 }, enter: { opacity: 1, y: 0, transition: { duration: 800 } } }"
    style="background: linear-gradient(120deg, #1976d2 80%, #00bcd4 100%); color: #fff; border-radius: 14px; box-shadow: 0 2px 16px #1976d288; padding: 1em 1.2em; flex: 1 1 40%; max-width: 45%;">
    <span style="font-size: 1.8em; vertical-align: middle;">📈</span>
    <b>Enable Longitudinal Assessment</b>
    <div style="font-size: 0.9em; margin-top: 0.5em;">Collect multiple letters per patient to enable the study of disease progression and treatment response over time.</div>
  </div>

  <!-- O3: Create a Rich Multi-Modal Resource -->
  <div v-click
    v-motion="{ initial: { opacity: 0, y: 40 }, enter: { opacity: 1, y: 0, transition: { duration: 800 } } }"
    style="background: linear-gradient(120deg, #00bcd4 80%, #1976d2 100%); color: #fff; border-radius: 14px; box-shadow: 0 2px 16px #1976d288; padding: 1em 1.2em; flex: 1 1 40%; max-width: 45%;">
    <span style="font-size: 1.8em; vertical-align: middle;">📊</span>
    <b>Create a Rich Multi-Modal Resource</b>
    <div style="font-size: 0.9em; margin-top: 0.5em;">Link clinical text with structured data, ECGs, and echocardiogram videos for advanced, integrated AI models.</div>
  </div>

  <!-- O4: Proactively Mitigate Data Bias -->
  <div v-click
    v-motion="{ initial: { opacity: 0, y: 40 }, enter: { opacity: 1, y: 0, transition: { duration: 800 } } }"
    style="background: linear-gradient(120deg, #00bcd4 80%, #1976d2 100%); color: #fff; border-radius: 14px; box-shadow: 0 2px 16px #1976d288; padding: 1em 1.2em; flex: 1 1 40%; max-width: 45%;">
    <span style="font-size: 1.8em; vertical-align: middle;">🛡️</span>
    <b>Proactively Mitigate Data Bias</b>
    <div style="font-size: 0.9em; margin-top: 0.5em;">Ensure data quality and adhere to FAIR/CARE principles to foster the development of fairer and more robust AI systems.</div>
  </div>

</div>

---


## <span class="section-title">CARDIO:DE++ Enhancements & Enablements</span>

<!-- This flex container manages the vertical layout of the two diagrams -->
<div style="display: flex; flex-direction: column; justify-content: space-around; height: 85%;">

<!-- 
  This container uses v-clicks to overlay three diagrams.
  Each diagram contains the *full* layout, but styles future elements
  to be invisible, preventing any resizing or repositioning on click.
-->
<div class="unroll-container" style="position: relative; min-height: 200px;">
<v-clicks>

<!-- Step 1: Only CARDIO:DE is visible -->
```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'mainBkg': 'transparent' }}}%%
flowchart LR
    subgraph CARDIO_DE["CARDIO:DE Corpus"]
      A1["500 Cardiovascular Discharge Letters<br/>(Heidelberg)"]
      A2["Manual Annotations:<br/>Medication, Sections"]
    end
    subgraph EXT["Enhancements"]
      B1["2 letters+ per patient"]
      B2["Add:<br> Labs, ECGs, Echos, Angios"]
    end
    subgraph CARDIO_DEPP["CARDIO:DE++"]
      C1["1,000 discharge Letters<br/>(2 Sites)"]
      C2["Multi-Modal:<br/>Text + Structured Data"]
    end
    CARDIO_DE --> EXT
    EXT --> CARDIO_DEPP
    style CARDIO_DE fill:transparent,stroke:#ff4081,stroke-width:2px, primaryTextColor:'#e3f0fa', 
    style EXT fill:transparent,stroke:transparent,color:transparent
    style CARDIO_DEPP fill:transparent,stroke:transparent,color:transparent
    style B1 color:transparent,fill:transparent,stroke:transparent
    style B2 color:transparent,fill:transparent,stroke:transparent
    style C1 color:transparent,fill:transparent,stroke:transparent
    style C2 color:transparent,fill:transparent,stroke:transparent
    linkStyle 0,1 stroke:transparent

    classDef leaf fill:transparent,stroke:#ff4081,stroke-width:2px,color:#e3f0fa;
```

<!-- Step 2: CARDIO:DE and Enhancements are visible -->
```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'mainBkg': 'transparent' }}}%%
flowchart LR
    subgraph CARDIO_DE["CARDIO:DE Corpus"]
      A1["500 Cardiovascular Discharge Letters<br/>(Heidelberg)"]
      A2["Manual Annotations:<br/>Medication, Sections"]
    end
    subgraph EXT["Enhancements"]
      B1["2 letters+ per patient"]
      B2["Add:<br> Labs, ECGs, Echos, Angios"]
    end
    subgraph CARDIO_DEPP["CARDIO:DE++"]
      C1["1,000 discharge Letters<br/>(2 Sites)"]
      C2["Multi-Modal:<br/>Text + Structured Data"]
    end
    CARDIO_DE --> EXT
    EXT --> CARDIO_DEPP
    style CARDIO_DE fill:#00bcd422,stroke:#ff4081,stroke-width:2px
    style EXT fill:#00bcd422,stroke:#ff4081,stroke-width:2px
    style CARDIO_DEPP fill:transparent,stroke:transparent,color:transparent
    style C1 color:transparent,fill:transparent,stroke:transparent
    style C2 color:transparent,fill:transparent,stroke:transparent
    linkStyle 0 stroke:#ff4081
    linkStyle 1 stroke:transparent
```

<!-- Step 3: Full diagram is visible -->
```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'mainBkg': 'transparent' }}}%%
flowchart LR
    subgraph CARDIO_DE["CARDIO:DE Corpus"]
      A1["500 Cardiovascular Discharge Letters<br/>(Heidelberg)"]
      A2["Manual Annotations:<br/>Medication, Sections"]
    end
    subgraph EXT["Enhancements"]
      B1["2 letters+ per patient"]
      B2["Add:<br> Labs, ECGs, Echos, Angios"]
    end
    subgraph CARDIO_DEPP["CARDIO:DE++"]
      C1["1,000 discharge Letters<br/>(2 Sites)"]
      C2["Multi-Modal:<br/>Text + Structured Data"]
    end
    CARDIO_DE --> EXT
    EXT --> CARDIO_DEPP
    style CARDIO_DE fill:#00bcd422,stroke:#ff4081,stroke-width:2px
    style EXT fill:#00bcd422,stroke:#ff4081,stroke-width:2px
    style CARDIO_DEPP fill:#00bcd433,stroke:#ff4081,stroke-width:3px,font-weight:bold
    linkStyle 0,1 stroke:#ff4081
```

</v-clicks>
</div>

<div v-click>
```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 
    'primaryColor': 'transparent', 
    'primaryTextColor': '#e3f0fa', 
    'lineColor': '#ff4081', 
    'textColor': '#e3f0fa', 
    'mainBkg': 'transparent', 
    'nodeBorder': '#ff4081' 
}}}%%
flowchart TD
    A["<b>🧬<br>CARDIO:DE++<br>Multi-Modal Corpus</b>"]:::main
    B1["🤖<br>Robust, Generalizable<br>AI Models"]:::leaf
    B2["🧑‍⚕️<br>Improved Clinical<br>Decision Support"]:::leaf
    B3["🧪<br>Synthetic Data<br>Generation"]:::leaf
    B4["🔄<br>Data-to-Text &<br>Text-to-Data"]:::leaf
    B5["🧬<br>Advanced Patient<br>Phenotyping"]:::leaf
    B6["🤝<br>Collaborative Research<br>& Shared Tasks"]:::leaf

    A --> B1
    A --> B2
    A --> B3
    A --> B4
    A --> B5
    A --> B6

    classDef main fill:#00bcd433,stroke:#ff4081,stroke-width:3px,color:#e3f0fa,font-weight:bold;
    classDef leaf fill:transparent,stroke:#ff4081,stroke-width:2px,color:#e3f0fa;
```
</div>

</div>

---

## <span class="section-title">Graphical Abstract</span>

<div style="height: 1.5em;"></div>

<!-- This container uses flexbox to fill the remaining vertical space and create two columns -->
<div style="flex-grow: 1; display: flex; justify-content: space-around; align-items: start; min-height: 0; gap: 2em;">

  <!-- Left Column: Previous Work -->
  <div style="flex: 1; text-align: center;">
    <h3 style="color: #90caf9; margin-bottom: 1em; font-size: 1.2em;">Previous Work</h3>
    <img 
      src="/previous.png" 
      alt="Previous Work" 
      style="display: block; margin: 0 auto; max-width: 50%; max-height: 65vh; object-fit: contain; border-radius: 12px; box-shadow: 0 4px 24px #1976d288;"
    >
  </div>

  <!-- Right Column: This Proposal -->
  <div style="flex: 1; text-align: center;">
    <h3 style="color: #90caf9; margin-bottom: 1em; font-size: 1.2em;">Proposed Project</h3>
    <img 
      src="/graph_abstract.png" 
      alt="Proposed Project" 
      style="display: block; margin: 0 auto; max-width: 75%; max-height: 65vh; object-fit: contain; border-radius: 12px; box-shadow: 0 4px 24px #1976d288;"
    >
  </div>

</div>
---

## <span class="section-title">Work Packages Overview</span>

<div style="height: 1.5em;"></div>

| WP  | Title                                   | Months      |
|-----|-----------------------------------------|-------------|
| WP1 | Ethics, Legal Framework & Onboarding    | 1–5         |
| WP2 | Data Acquisition                        | 1–6        |
| WP3 | De-identification                       | 2–12        |
| WP4 | Annotation                              | 6–18        |
| WP5 | Advanced AI Model Development           | 13–21       |
| WP6 | Dissemination & Sustainability          | 19–24       |

---

## <span class="section-title">WP1: Ethics, Legal Framework & Site Onboarding</span>

<div style="height: 1.5em;"></div>

<div class="vcenter">
<ul>
  <li><b>Months:</b> 1–5</li>
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
  <li><b>Months:</b> 2–6</li>
  <li><b>Objective:</b> Collect 1,000 new discharge letters and structured tabular data</li>
  <li><b>Key Tasks:</b>
    <ul>
      <li>Patient consent and data collection at both sites</li>
      <li>extract structured numerical/categorical data and link to SNOMED CT</li>
      <li>Collect textual reports of findings from echocardiograms and coronary angiography</li>
      <li>Acquire echocardiogram videos in suitable digital formats, preserving resolution for analysis.</li>
      <li>Acquire contemporaneous 12-lead ECGs as raw digital time series data.</li>
    </ul>
  </li>
  <li><b>Deliverables:</b> 1,000 raw discharge letters + structured data</li>
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
  <li><b>Deliverables:</b> 1,000 de-identified discharge letters, the corresponding de-identified and linked structured tabular data, along with a comprehensive de-identification quality report, and a DFG 12-month status report </li>
  <li><b>Lead:</b> Heidelberg</li>
</ul>
<div style="margin-top: 1.2em; font-size: 1em; background: linear-gradient(90deg, #1976d222 60%, #00bcd422 100%); border-left: 6px solid #1976d2; box-shadow: 0 2px 12px #1976d244; padding: 1em 1.2em; border-radius: 12px; display: flex; align-items: flex-start;">
  <span style="font-size: 1.6em; margin-right: 0.7em; margin-top: -0.1em;">🔒</span>
  <span>
    <b style="font-weight: 600; color: #1976d2;">Key resource:</b>
    <a href="https://iapp.org/news/a/does-anonymization-or-de-identification-require-consent-under-the-gdpr" target="_blank">
      Does anonymization or de-identification require consent under the GDPR?
    </a>
  </span>
</div>
</div>

---

## <span class="section-title">Joint Annotation Process</span>

<div style="height: 2.5em;"></div>

<div style="flex-grow: 1; display: flex; justify-content: center; align-items: center; min-height: 0;">
  <img 
    src="/joint_anno2.png" 
    alt="Joint Annotation Process between UKHD and UMM" 
    style="max-width: 75%; max-height: 75vh; object-fit: contain; border-radius: 12px; box-shadow: 0 4px 24px #1976d288;"
  >
</div>

---

## <span class="section-title">WP4: Annotation</span>

<div style="height: 1.5em;"></div>

<div class="vcenter">
<ul>
  <li><b>Months:</b> 6–18</li>
  <li><b>Objective:</b> Annotate new data using established schemes</li>
  <li><b>Key Tasks:</b>
    <ul>
      <li>Apply CARDIO:DE annotation schemes (medication, section classes)</li>
      <li>Inter-annotator agreement studies</li>
      <li>Link text to tabular data via anonymized IDs</li>
    </ul>
  </li>
  <li><b>Deliverables:</b> Fully annotated CARDIO:DE++ corpus (including medication/section classes for new letters/reports); linked 12-lead ECGs, structured numerical/categorical data, and echocardiogram videos; new annotation layers; updated guidelines; comprehensive IAA reports</li>
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
  <li><b>Months:</b> 13–23</li>
  <li><b>Objective:</b> Develop and evaluate advanced AI models</li>
  <li><b>Key Tasks:</b>
    <ul>
      <li>Fine-tune LLMs for synthetic data</li>
      <li>Develop data-to-text & text-to-data models</li>
      <li>Develop/evaluate multimodal models integrating text, structured , ECG, and Echo video data</li>
    </ul>
  </li>
  <li><b>Deliverables:</b> Fine-tuned generative LLMs; evaluated corpus of synthetic discharge letters/reports; developed/evaluated data-to-text and text-to-data NLP models; report on advanced patient phenotyping; baseline performance metrics on CARDIO:DE++.</li>
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
  <li><b>Months:</b> 18–24</li>
  <li><b>Objective:</b> Maximize impact and ensure sustainability</li>
  <li><b>Key Tasks:</b>
    <ul>
      <li>Public release of CARDIO:DE++ corpus</li>
      <li>Documentation and usage examples</li>
      <li>Long-term maintenance plan</li>
      <li>Shared Tasks?</li>
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
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-empty"></td>
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
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
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
    <td class="timeline-bar"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td>
  </tr>
  <tr>
    <td class="timeline-label">WP5</td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-bar"></td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-bar"></td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-bar"></td>
    <td class="timeline-bar"></td><td class="timeline-bar"></td><td class="timeline-bar"></td>
    <td class="timeline-empty"></td><td class="timeline-empty"></td><td class="timeline-empty"></td>
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
    <li v-click style="margin-bottom: 1.2em; display: flex; align-items: center;">
      <span style="display: inline-flex; align-items: center;">
        First large, multi-modal, parallel German cardiovascular corpus
        <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f4c8.png" alt="chart" width="28" height="28" style="vertical-align: middle; margin-left: 0.7em;">
      </span>
    </li>
    <li v-click style="margin-bottom: 1.2em; display: flex; align-items: center;">
      <span style="display: inline-flex; align-items: center;">
        Enables robust, generalizable AI models for clinical NLP
        <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f916.png" alt="robot" width="28" height="28" style="vertical-align: middle; margin-left: 0.7em;">
      </span>
    </li>
    <li v-click style="margin-bottom: 1.2em; display: flex; align-items: center;">
      <span style="display: inline-flex; align-items: center;">
        Supports synthetic data generation and advanced patient phenotyping
        <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f9ec.png" alt="dna" width="28" height="28" style="vertical-align: middle; margin-left: 0.7em;">
      </span>
    </li>
    <li v-click style="margin-bottom: 1.2em; display: flex; align-items: center;">
      <span style="display: inline-flex; align-items: center;">
        Fosters collaboration and innovation in German-speaking clinical NLP
        <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/72x72/1f91d.png" alt="handshake" width="28" height="28" style="vertical-align: middle; margin-left: 0.7em;">
      </span>
    </li>
  </ul>
</div>

---
layout: center
slidenumbers: false
---

<style>
/* Keyframes for the subtle pulsating animation */
@keyframes pulse-line {
  from {
    opacity: 0.3;
  }
  to {
    opacity: 1.0;
  }
}

/* Scoped styles for this specific slide layout */
.slidev-layout.center h1 {
  font-size: 3.5em;
  color: #00bcd4;
  font-weight: 800;
  margin-bottom: 0.5em;
  text-shadow: 0 3px 20px #1976d299;
}

.ecg-divider {
  /* The width is kept the same for perfect alignment */
  width: 340px;
  margin: 1em 0;
  animation: pulse-line 2200ms ease-in-out infinite alternate;
}

.contact-info {
  margin-top: 1.5em;
  font-size: 0.9em;
  color: #e3f0fa;
  line-height: 1.6;
}

.contact-info a {
  color: #90caf9;
  text-decoration: none;
  border-bottom: 1px dotted #90caf988;
}
</style>

<!-- The entire content is automatically centered by the layout -->

<h1>
  Thank you!
</h1>

<!-- 
  The SVG now contains a completely new path with 4 smaller, compressed peaks.
  The stroke-width is reduced for a finer look.
-->
<svg class="ecg-divider" viewBox="0 0 520 60" fill="none" xmlns="http://www.w3.org/2000/svg">
  <path
    d="M0,30 L20,30 C23,30 25,28 28,30 L35,30 L40,32 L45,20 L50,40 L55,30 L65,30 C70,30 75,26 80,30 L130,30 C133,30 135,28 138,30 L145,30 L150,32 L155,20 L160,40 L165,30 L175,30 C180,30 185,26 190,30 L260,30 C263,30 265,28 268,30 L275,30 L280,32 L285,20 L290,40 L295,30 L305,30 C310,30 315,26 320,30 L390,30 C393,30 395,28 398,30 L405,30 L410,32 L415,20 L420,40 L425,30 L435,30 C440,30 445,26 450,30 L520,30"
    stroke="#ff4081"
    stroke-width="2.5"
    stroke-linecap="round"
  />
</svg>

<div class="contact-info">
  <b>Philipp Wiesenbach</b><br>
  <a href="mailto:philipp.wiesenbach@uni-heidelberg.de">philipp.wiesenbach@uni-heidelberg.de</a> 
</div>