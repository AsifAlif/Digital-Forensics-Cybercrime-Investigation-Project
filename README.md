<div id="top"></div>

<h1 align="center">Digital Forensics & Cybercrime Investigation</h1>

<p align="center"><em>A collection of hands-on digital forensic investigations on seized computer and mobile evidence, conducted with Autopsy and Kali Linux forensic tools.</em></p>

<p align="center">
  <img src="Project_Case_1/Project%20Screenshot/cyber.PNG" width="85%" alt="Cybercrime investigation">
</p>

![Autopsy](https://img.shields.io/badge/Autopsy-disk%20forensics-2e7d32)
![ExifTool](https://img.shields.io/badge/ExifTool-metadata-6a1b9a)
![Kali Linux](https://img.shields.io/badge/Kali%20Linux-forensics-1679A7)
![License](https://img.shields.io/badge/license-MIT-green)

---

## About

This repository documents a series of digital forensic investigations carried out on seized disk and mobile device images. Each case begins with an evidence image and ends with a defensible, evidence-backed conclusion, applying core forensic techniques: file-signature analysis, file carving from unallocated space, document and image metadata examination, keyword searching, and mobile-device forensics.

> **Note on the data.** These cases use **training / educational forensic images** distributed for digital-forensics coursework. The names, emails, and locations in the evidence belong to those teaching scenarios.

## 📂 Full case report → [`Project_Case_1`](Project_Case_1/README.md)

The complete, step-by-step investigation — with methodology, screenshots, and findings for every task — is in **[Project_Case_1](Project_Case_1/README.md)**. It covers four cases:

| Case | Scenario | Techniques |
|---|---|---|
| **1 — Stalking** | Recovering images a suspect hid on his computer | File-signature analysis, carving from unallocated space |
| **2 — Suspected misrepresentation** | Authenticating a job applicant's reference and photo | Document & image metadata (ExifTool), EXIF/GPS geolocation |
| **3 — Refugees across Europe** | Tracing a trafficking suspect's emails and accomplices | Keyword search (raw vs. indexed), slack-space analysis |
| **4 — Jodi Arias (murder)** | Establishing motive, alibi, and presence at the scene | Mobile forensics, device identifiers, chat recovery |

**➡️ [Open the full investigation report](Project_Case_1/README.md)**

## Tools

Autopsy · ExifTool · Kali Linux forensic utilities · Google Maps (geolocation verification)



<p align="right">(<a href="#top">back to top</a>)</p>
