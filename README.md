<div id="top"></div>

<h1 align="center">Digital Forensics & Cybercrime Investigation</h1>

<p align="center"><em>Disk and mobile forensic investigations across five cases — signature analysis, metadata examination, keyword search, and timeline reconstruction — using Autopsy and Kali Linux forensic tools.</em></p>

<p align="center">
  <img src="Project_Case_1/Project%20Screenshot/cyber.PNG" width="80%" alt="Cybercrime investigation">
</p>

![Autopsy](https://img.shields.io/badge/Autopsy-disk%20forensics-2e7d32)
![ExifTool](https://img.shields.io/badge/ExifTool-metadata-6a1b9a)
![Kali Linux](https://img.shields.io/badge/Kali%20Linux-forensics-1679A7)
![License](https://img.shields.io/badge/license-MIT-green)

> **About the data.** These investigations use **training / educational forensic images** (disk and mobile `.dd` / EnCase images distributed for digital-forensics coursework, including the widely used Jodi Arias training image). The names, emails, and locations in the evidence belong to those teaching scenarios.

---

## Overview

This project works through five forensic scenarios, each starting from a seized disk or phone image and ending in a defensible, evidence-backed conclusion. Across the cases it demonstrates the core techniques of a digital forensic examination:

| Technique | Where it is used |
|---|---|
| File-signature (magic-number) analysis | Case 1 — detecting a renamed JPEG |
| Unallocated-space / file carving | Case 1 — recovering a deleted image |
| Document & image metadata analysis (ExifTool) | Case 2 — authenticating a reference and a photo |
| Keyword search (raw vs. indexed) | Case 3 — email and contact discovery |
| Mobile forensics (device identifiers, chat recovery) | Case 4 — motive, alibi, and timeline |

**Tools:** Autopsy, ExifTool, Kali Linux forensic utilities, and Google Maps for geolocation verification.

---

## Case 1 — Stalking (disk forensics)

**Scenario.** A suspect, arrested for stalking, claims he holds no photographs of the target. He was observed using a Nexus 5 phone. The task is to examine his computer for hidden images.

**Signature analysis.** Autopsy's *Extension Mismatch Detected* module flagged files whose contents did not match their extension:

<p align="center"><img src="Project_Case_1/Project%20Screenshot/2.jpeg" width="85%" alt="Extension mismatch in Autopsy"></p>

Inspecting the file header confirmed the magic number **`FF D8 FF E0`** — a JPEG image — on a file disguised with a `.sys` extension:

<p align="center"><img src="Project_Case_1/Project%20Screenshot/3.jpeg" width="85%" alt="JPEG header on a .sys file"></p>

**Finding.** The suspect had renamed image files to hide them. The disguised files, and a relevant ~40 kB JPEG carved from **unallocated space**, were recovered and shown to relate to the target — contradicting his claim.

<p align="center"><img src="Project_Case_1/Project%20Screenshot/8.jpeg" width="85%" alt="Image carved from unallocated space"></p>

---

## Case 2 — Suspected misrepresentation (document & image metadata)

**Scenario.** A job applicant, Mira Chep, submitted a Word reference and a photo of herself in Rome. The task is to determine whether both are authentic.

**Document metadata.** ExifTool on the reference `.docx` showed the author **Sara Bartholomew**, company **Blue Sky Travel**, and a create date of **2015-07-01** — consistent with the applicant's account:

<p align="center"><img src="Project_Case_1/Project%20Screenshot/9.jpeg" width="80%" alt="ExifTool metadata of the reference document"></p>

**Image metadata.** The photo's EXIF data showed it was taken with a **Nexus 5**, not the claimed iPhone 6, and carried GPS coordinates **41°53′24.6″N, 12°29′32.2″E**, which resolve to the Colosseum in Rome:

<p align="center"><img src="Project_Case_1/Project%20Screenshot/11.jpeg" width="80%" alt="EXIF metadata showing Nexus 5 and GPS"></p>
<p align="center"><img src="Project_Case_1/Project%20Screenshot/14.jpeg" width="80%" alt="GPS coordinates mapped to Rome"></p>

**Finding.** The reference and the location are genuine; only the stated camera model differs. The evidence supports the applicant's claims.

---

## Case 3 — Refugees across Europe (keyword search & email analysis)

**Scenario.** Kyle Dammer is suspected of involvement in trafficking refugees through Europe. His seized computer must be examined for his email address, correspondence, and accomplices.

Using **keyword searches** in Autopsy, the investigation recovered:

- The suspect's email address and three incriminating messages tying him to the trafficking operation;
- Four possible accomplices identified from the correspondence;
- One email **ruling out** a named individual, who asked to be removed from the plan;
- Physical addresses associated with two of the accomplices.

<p align="center"><img src="Project_Case_1/Project%20Screenshot/16.jpeg" width="85%" alt="Keyword search results in Autopsy"></p>
<p align="center"><img src="Project_Case_1/Project%20Screenshot/18.jpeg" width="85%" alt="Recovered email correspondence"></p>

**Forensic concepts applied.** This case also documents the difference between a **raw search** (line-by-line, text only) and an **indexed search** (word-by-word across text and binary), and explains **slack space** as a source of residual evidence from deleted files.

---

## Case 4 — Murder investigation (mobile forensics)

**Scenario.** A phone image (`GalaxyNexusArias-dm0.dd`) must be examined for device identifiers, motive, alibi, and evidence placing the suspect at the scene on the day of the murder.

Findings recovered from the device:

- **Device identifiers** — the phone's IMSI and ICCID were extracted from the image.
- **Motive** — recovered chat messages reveal a jealousy-driven dispute over the victim's relationship with another person.
- **False alibi** — messages contradict the suspect's stated whereabouts.
- **Links to a third party** — conversations show contact with a known arms dealer, including a visit to arrange a purchase, with date, time, and location.
- **Placement at the scene** — messages confirm the suspect planned to be at the victim's house on the date of the murder.

<p align="center"><img src="Project_Case_1/Project%20Screenshot/24.jpeg" width="85%" alt="Device identifiers recovered from the phone image"></p>
<p align="center"><img src="Project_Case_1/Project%20Screenshot/47.jpeg" width="85%" alt="Recovered chat evidence"></p>

**Finding.** The combined message, timeline, and location evidence establishes motive, opportunity, and presence at the scene.

---

## Skills demonstrated

- Forensic examination of both **disk** and **mobile** images with Autopsy
- **File-signature analysis** and **file carving** from unallocated space
- **Metadata forensics** on documents and images, including EXIF/GPS geolocation
- **Keyword search** strategy and understanding of raw vs. indexed searches and slack space
- Building **evidence-based conclusions** suitable for a case report

## Repository structure

```
.
├── README.md
├── LICENSE
└── Project_Case_1/
    ├── README.md                 # case report (this content)
    └── Project Screenshot/       # evidence screenshots (Autopsy, ExifTool)
```

## Author

Asif Alif — digital forensics, network security, and post-quantum cryptography.

<p align="right">(<a href="#top">back to top</a>)</p>
