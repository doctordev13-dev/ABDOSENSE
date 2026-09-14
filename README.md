# AbdoSense: Continuous Intra-Abdominal Pressure Monitoring System

[![Status](https://img.shields.io/badge/Status-Prototype-blue.svg)]()
[![Hardware](https://img.shields.io/badge/Hardware-Arduino_Nano%20%7C%20Strain_Gauge-orange.svg)]()
[![Domain](https://img.shields.io/badge/Domain-Translational_Medicine%20%7C%20Edge_AI-green.svg)]()

> An AI-Augmented, Piezoresistive Transduction Framework for Continuous, Non-Invasive Intra-Abdominal Pressure Monitoring[cite: 1]. 

## 🎥 System Demonstration
<!-- Ensure your video is located in the assets folder or replace the link with an Unlisted YouTube URL -->
[![AppdoSense Demonstration Video](assets/video_thumbnail.jpg)](assets/demonstration_video.mp4)  
*Click the image above to view the full hardware and software demonstration.*

---

## 📝 Project Overview
**Theme:** AI in Clinical Care: AI-Augmented Clinical Decision Making (2024)[cite: 1].

**Target Population:** Critically ill post-laparotomy surgical patients, poly-trauma admissions, acute pancreatitis cohorts, and intensive care patients at imminent risk of Intra-Abdominal Hypertension (IAH) and Abdominal Compartment Syndrome (ACS)[cite: 1].

### Background & Clinical Need
Intra-abdominal hypertension (IAH) and abdominal compartment syndrome (ACS) cause severe multi-organ hypoperfusion and ICU mortality exceeding 40%[cite: 1]. The clinical standard, transvesical manometry via the Modified Kron's technique, is discontinuous, labour-intensive, and carries significant risks of catheter-associated urinary tract infections (CAUTI) and bladder trauma[cite: 1]. AbdoSense was engineered as a non-invasive device pairing a skin-conformal piezoresistive tensiometer with multi-modal edge AI to provide continuous IAP values at the bedside[cite: 1].

---

## ⚙️ Hardware Architecture & Physics
AppdoSense integrates a skin-conformal piezoresistive strain gauge patch, an instrumentation amplifier, and an Arduino Nano core[cite: 1]. 

<div align="center">
  <img src="assets/hardware_pic_1.jpg" alt="AppdoSense Sensor Module" width="45%">
  <img src="assets/hardware_pic_2.jpg" alt="AppdoSense Data Acquisition Setup" width="45%">
  <p><i>Left: Skin-conformal piezoresistive patch. Right: Arduino Nano core and amplifier integration.</i></p>
</div>

Based on the thin-walled Law of Laplace, abdominal wall tension ($T$) couples with internal pressure[cite: 1]:
$$T=\frac{IAP\cdot r}{2\cdot t_{w}}$$

Visceral micro-strain ($\epsilon=\Delta L/L_{0}$) produces proportional fractional resistance shifts ($\Delta R/R_{0}=GF\cdot\epsilon$) and differential Wheatstone bridge voltage[cite: 1]:
$$\Delta V_{out}\approx\frac{V_{in}\cdot GF\cdot\epsilon}{4}$$

This is calibrated linearly as[cite: 1]:
$$IAP=m\cdot\Delta V_{out}+b$$

---

## 🧠 AI-Augmented Signal Processing
To eliminate false alarms, an embedded edge AI classifier continuously cross-evaluates real-time strain signals with surface electromyography, ventilatory airway pressures, and vital parameters[cite: 1]. 

The AI applies spectral wavelet decomposition and dynamic compliance filtering to isolate sustained hydrostatic compartment pressure from transient non-pathological confounders such as[cite: 1]:
* Somatic muscular guarding[cite: 1].
* Bladder distension[cite: 1].
* Coughing and ventilator dyssynchrony[cite: 1].

---

## 📊 Validation & Key Findings
This framework was validated on an observational cohort of 50 healthy volunteers across resting and dynamic provocation manoeuvres in the supine position[cite: 1].

* **Performance:** The prototype achieved rapid dynamic response (<450 ms latency) without baseline signal drift[cite: 1].
* **Accuracy:** Recorded a mean resting IAP of 3.4 ± 1.1 mmHg, precisely matching recognized physiological resting ranges (0-5 mmHg)[cite: 1]. 
* **Specificity:** During provocation testing (Valsalva straining, voluntary abdominal guarding), the multi-modal AI engine differentiated true sustained compartment hypertension from transient physiological artifacts with 95.8% specificity[cite: 1].
* **Automated Alerting:** Accurately triggered automated alerts upon crossing pathological IAH thresholds (≥ 12 mmHg)[cite: 1].

---

## 🌍 Clinical Impact
AbdoSense provides a continuous, non-invasive alternative to transvesical catheterization, completely avoiding CAUTI hazards while drastically reducing intensive care nursing burden[cite: 1]. By combining continuous bio-sensing with AI-driven artifact suppression, this low-cost solution delivers reliable early warnings against ACS, transforming advanced critical care monitoring in resource-limited global settings[cite: 1].

---

## 🤝 Team & Presentations
<div align="center">
  <img src="assets/team_presentation_1.jpg" alt="Presenting AppdoSense" width="45%">
  <img src="assets/team_presentation_2.jpg" alt="Team Presentation" width="45%">
  <p><i>Demonstrating the AppdoSense prototype with the interdisciplinary development team.</i></p>
</div>

* **Lead Clinical Author:** Dr. Debankur Chakraborty, MBBS (Hons), R.G. Kar Medical College, WBUHS[cite: 1].
* **Co-Authors:** Abhinav Paniketty (Biomedical Engineer), Bhagyashree Samel (Product Designer), Dr. Nancy (Junior Resident, Pharmacology)[cite: 1].
* **Clinical Guides & Mentors:** Dr. Gayatri Muley, Dr. Zeenal Punamiya, Ms. Shreya Kurumpilai[cite: 1].

## 📬 Contact
**Dr. Debankur Chakraborty**  
📧 doctordev13@gmail.com | 📞 +91 7439624842[cite: 1] 
