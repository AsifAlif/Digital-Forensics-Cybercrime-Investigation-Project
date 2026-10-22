<div id="top"></div>

<h1 align="center">Digital Forensics & Cybercrime Investigation</h1>

<p align="center"><em>Disk and mobile forensic investigations across multiple cases — signature analysis, metadata examination, file carving, keyword search, and timeline reconstruction — conducted with Autopsy and Kali Linux forensic tools.</em></p>

<p align="center">
  <img src="Project%20Screenshot/cyber.PNG" width="85%" alt="Cybercrime investigation">
</p>

![Autopsy](https://img.shields.io/badge/Autopsy-disk%20forensics-2e7d32)
![ExifTool](https://img.shields.io/badge/ExifTool-metadata-6a1b9a)
![Kali Linux](https://img.shields.io/badge/Kali%20Linux-forensics-1679A7)
![License](https://img.shields.io/badge/license-MIT-green)

---

## About the project

This project presents a set of digital forensic investigations carried out on seized computer and mobile device images. Each case begins with an evidence image and ends with a defensible, evidence-backed conclusion, using **Autopsy** and a range of **Kali Linux** forensic tools. The investigations cover file-signature analysis, recovery of data from unallocated space, document and image metadata examination, keyword searching, and mobile-device forensics.

> **Note on the data.** These cases use **training / educational forensic images** distributed for digital-forensics coursework (including the widely used Jodi Arias mobile training image). The names, emails, and locations in the evidence belong to those teaching scenarios.

<p align="right">(<a href="#top">back to top</a>)</p>

---

## Case 1: Stalking

A male suspect, Rawi Hasse, was arrested for stalking and harassment, accused of repeatedly photographing another man. He claims to hold no pictures of the target and was observed using a Nexus 5 phone. The target's reference photograph was provided for comparison:

<p align="center"><img src="Project%20Screenshot/1.jpeg" alt="Target photograph"></p>

### Task 1 — Perform a signature analysis to identify suspicious files on the suspect's computer.

Running a signature analysis in Autopsy on Rawi Hasse's hard drive revealed an extension mismatch:

<p align="center"><img src="Project%20Screenshot/2.jpeg" alt="Extension mismatch detected in Autopsy"></p>

The highlighted file carries a `.sys` extension, but its signature does not match that file type. Examining the header shows it begins with **`FF D8 FF E0`**, the standard JPEG signature:

<p align="center"><img src="Project%20Screenshot/3.jpeg" alt="JPEG signature on a .sys file"></p>

This confirms a deliberate signature/extension mismatch: an image file renamed to look like a system file.

<p align="center"><img src="Project%20Screenshot/4.jpeg" alt="Suspicious file detail"></p>
<p align="center"><img src="Project%20Screenshot/5.jpeg" alt="Suspicious file detail"></p>

These are the suspicious files identified on the computer.

### Task 2 — Examine the suspicious files found in relation to this case.

<p align="center"><img src="Project%20Screenshot/6.jpeg" alt="Suspicious file examination"></p>
<p align="center"><img src="Project%20Screenshot/7.jpeg" alt="Suspicious file examination"></p>

These two files are the ones relevant to the case.

### Task 3 — Examine the unallocated space to recover a relevant JPEG of about 40 kB, and show the method used.

Carving the unallocated space recovered the following image:

<p align="center"><img src="Project%20Screenshot/8.jpeg" alt="Image carved from unallocated space"></p>

The recovered file is a ~40 kB JPEG held in unallocated space and depicts the target, directly relating it to the case and contradicting the suspect's claim.

<p align="right">(<a href="#top">back to top</a>)</p>

---

## Case 2: Suspected misrepresentation

Sheffield Travel, a specialist travel agent, is hiring for trips to Rome. An applicant, **Mira Chep**, submitted a reference in Microsoft Word format, stating it came from **Sara Bartholomew** at **Blue Sky Travel**, where she claims to have worked as a travel consultant in Rome for six months. She also supplied a photograph of herself at the Colosseum, claiming it was taken on her iPhone 6. The task is to determine whether the reference and the photograph are authentic.

### Task 1 — Explain metadata and its use in forensic examination.

Metadata — "data about data" — records a file's history, such as when it was created, modified, and last accessed. In a forensic examination, metadata is essential for authenticating a file's origin. For an image it can reveal whether the picture is original or edited, which device captured it, and where it was taken; for a document it can reveal the file type, authorship, timestamps, and whether its signature has been altered.

### Task 2 — Examine the metadata of the reference and report the findings.

Running ExifTool on `Mira Chep Reference.docx` returned:

<p align="center"><img src="Project%20Screenshot/9.jpeg" alt="ExifTool output for the reference document"></p>

The document's author is **Sara Bartholomew**, the company is **Blue Sky Travel**, and the create date is **2015-07-01**. This is consistent with the applicant's account, indicating the reference is authentic.

### Task 3 — Examine the metadata of the applicant's photograph and report the findings.

The supplied photograph, `Colosseum.jpg`:

<p align="center"><img src="Project%20Screenshot/10.jpeg" alt="Applicant's photograph in Rome"></p>

Its EXIF metadata shows the camera model was a **Nexus 5**, not the claimed iPhone 6:

<p align="center"><img src="Project%20Screenshot/11.jpeg" alt="EXIF camera model: Nexus 5"></p>

Additional metadata, including GPS coordinates, was also recovered:

<p align="center"><img src="Project%20Screenshot/12.jpeg" alt="Additional EXIF metadata"></p>
<p align="center"><img src="Project%20Screenshot/13.jpeg" alt="EXIF GPS coordinates"></p>

The coordinates are **41°53′24.64″N, 12°29′32.19″E**. Searching them on Google Maps places the photograph in Rome, at the location shown in the image:

<p align="center"><img src="Project%20Screenshot/14.jpeg" alt="GPS coordinates mapped to Rome"></p>

The photograph was therefore genuinely taken in Rome at the stated location; only the camera model differs from the applicant's claim.

### Task 4 — Recommendation for Sheffield Travel.

The evidence supports the applicant's account: the reference metadata is authentic and attributes the document to Sara Bartholomew at Blue Sky Travel, and the photograph was genuinely taken in Rome. On this basis, the applicant's claims of relevant experience are substantiated, and she can be considered a credible candidate for the post.

<p align="right">(<a href="#top">back to top</a>)</p>

---

## Case 3: Refugees across Europe

**Kyle Dammer**, based in Austria, is suspected of involvement in trafficking refugees from Syria through Europe, and of connection to the movement of a vehicle in which 27 refugees were found on the Austrian border on 23 July 2015. His computer was seized on 1 August 2015 and the hard drive was examined with **Autopsy**.

### Task 1 — Find the suspect's email address and up to three emails that could serve as evidence of involvement in trafficking.

A keyword search for "Kyle Dammer" was run in Autopsy:

<p align="center"><img src="Project%20Screenshot/15.jpeg" alt="Keyword search in Autopsy"></p>
<p align="center"><img src="Project%20Screenshot/16.jpeg" alt="Keyword search results"></p>

The suspect's email address was identified as **Kyle865@hotmail.com**. The search then recovered relevant correspondence:

<p align="center"><img src="Project%20Screenshot/17.jpeg" alt="Email from Kyle Dammer to JDurmen"></p>

This message is from `Kyle865@hotmail.com` to `JDurmen@gmail.com`.

<p align="center"><img src="Project%20Screenshot/18.jpeg" alt="Email from Kyle Dammer to jomag"></p>

This message, from `Kyle865@hotmail.com` to `jomag@pmail.co.pl`, indicates involvement in trafficking across Europe.

<p align="center"><img src="Project%20Screenshot/19.jpeg" alt="Email from Ben Toman to Kyle Dammer"></p>

This message is from Ben Toman to Kyle Dammer. Together, the three emails and their contents support the suspicion that Kyle Dammer was involved in trafficking refugees from Syria through Europe.

### Task 2 — Find the names of four possible contacts who may have worked with the suspect.

<p align="center"><img src="Project%20Screenshot/17.jpeg" alt="Contact Jako Durmen"></p>

The first contact is **Jako Durmen** (`JDurmen@gmail.com`).

<p align="center"><img src="Project%20Screenshot/18.jpeg" alt="Contact Jo Magdi"></p>

The second contact is **Jo Magdi** (`jomag@pmail.co.pl`).

<p align="center"><img src="Project%20Screenshot/20.jpeg" alt="Contact Josip Kova"></p>

The third contact is **Josip Kova** (`JosipK@t-com.hr`).

<p align="center"><img src="Project%20Screenshot/19.jpeg" alt="Contact Ben Toman"></p>

The fourth contact is **Ben Toman**.

### Task 3 — Find one email that rules out one of the accomplices.

<p align="center"><img src="Project%20Screenshot/21.jpeg" alt="Email ruling out an accomplice"></p>

This message from **Jo Magdi** (`jomag@pmail.co.pl`) to Kyle Dammer asks to be removed from the plan, ruling him out as a participant.

### Task 4 — Find physical addresses associated with two accomplices.

<p align="center"><img src="Project%20Screenshot/22.jpeg" alt="Josip Kova address"></p>

Josip Kova's physical address is in Croatia.

<p align="center"><img src="Project%20Screenshot/23.jpeg" alt="Jako Durmen address"></p>

Jako Durmen's physical address is in Europe.

### Task 5 — Explain the difference between a raw search and an indexed search, and state which was used and why.

A **raw search** matches text files line by line and does not search binary files; in Autopsy this corresponds to an *exact match* search.

<p align="center"><img src="Project%20Screenshot/15.jpeg" alt="Raw (exact match) search in Autopsy"></p>

An **indexed search** matches both text and binary files, word by word, comparing each word of the query against the indexed content; in Autopsy, substring and regular-expression searches are indexed. A raw search was used here because it executes line by line and returns results faster than an indexed search for this query.

### Task 6 — Explain slack space and how data left there can be recovered.

**Slack space** is the unused storage left over when a file does not fill the entire cluster allocated to it. For example, a 2 kB file stored in a 4 kB cluster leaves 2 kB of slack space. Because deleted data is not immediately overwritten, residual information from previously deleted files can remain in slack space, where it can be recovered with specialist forensic tools — making it an important source of evidence.

<p align="right">(<a href="#top">back to top</a>)</p>

---

## Case 4: Jodi Arias — murder suspect

A mobile device image (`GalaxyNexusArias-dm0.dd`) was examined in **Autopsy** for device identifiers, motive, alibi, and evidence placing the suspect at the scene.

### Task 1 — Find the IMSI and ICCID numbers of the phone.

<p align="center"><img src="Project%20Screenshot/24.jpeg" alt="IMSI recovered from the phone image"></p>

The **IMSI** is **2060188**.

<p align="center"><img src="Project%20Screenshot/25.jpeg" alt="ICCID recovered from the phone image"></p>

The **ICCID** is **5b514492-dd44-49d1-a155-f32802a74d8c**.

### Task 2 — Evidence of a motive for murder.

Recovered messages between Travis Alexander and Jodi Arias establish the motive:

<p align="center"><img src="Project%20Screenshot/26.jpeg" alt="Recovered conversation"></p>
<p align="center"><img src="Project%20Screenshot/27.jpeg" alt="Recovered conversation"></p>
<p align="center"><img src="Project%20Screenshot/28.jpeg" alt="Recovered conversation"></p>
<p align="center"><img src="Project%20Screenshot/29.jpeg" alt="Recovered conversation"></p>
<p align="center"><img src="Project%20Screenshot/30.jpeg" alt="Recovered conversation"></p>
<p align="center"><img src="Project%20Screenshot/31.jpeg" alt="Recovered conversation"></p>
<p align="center"><img src="Project%20Screenshot/32.jpeg" alt="Recovered conversation"></p>
<p align="center"><img src="Project%20Screenshot/33.png" alt="Recovered conversation"></p>
<p align="center"><img src="Project%20Screenshot/34.png" alt="Recovered conversation"></p>
<p align="center"><img src="Project%20Screenshot/35.jpeg" alt="Recovered conversation"></p>
<p align="center"><img src="Project%20Screenshot/36.jpeg" alt="Recovered conversation"></p>
<p align="center"><img src="Project%20Screenshot/37.jpeg" alt="Recovered conversation"></p>
<p align="center"><img src="Project%20Screenshot/38.jpeg" alt="Recovered conversation"></p>
<p align="center"><img src="Project%20Screenshot/39.jpeg" alt="Recovered conversation"></p>
<p align="center"><img src="Project%20Screenshot/40.jpeg" alt="Recovered conversation"></p>
<p align="center"><img src="Project%20Screenshot/41.jpeg" alt="Recovered conversation"></p>

The conversation reveals that the suspect learned of the victim's relationship with another person, leading to escalating arguments and explicit threats. This establishes the motive for the murder.

### Task 3 — Evidence of a false alibi.

<p align="center"><img src="Project%20Screenshot/42.jpeg" alt="Alibi-related messages"></p>
<p align="center"><img src="Project%20Screenshot/43.jpeg" alt="Alibi-related messages"></p>
<p align="center"><img src="Project%20Screenshot/44.jpeg" alt="Alibi-related messages"></p>
<p align="center"><img src="Project%20Screenshot/45.jpeg" alt="Alibi-related messages"></p>
<p align="center"><img src="Project%20Screenshot/46.jpeg" alt="Alibi-related messages"></p>

Messages between the suspect and Mabel show the suspect's stated whereabouts, which contradict the claimed alibi.

### Task 4 — Evidence of links with Edgar Kanne.

The case file identifies Edgar Kanne as a drug and arms dealer. The investigation recovered:

<p align="center"><img src="Project%20Screenshot/47.jpeg" alt="Links to Edgar Kanne"></p>
<p align="center"><img src="Project%20Screenshot/48.jpeg" alt="Links to Edgar Kanne"></p>

The conversation shows the suspect knew Edgar Kanne and visited his house to arrange a purchase, contradicting her statements that she did not know him and had never been there.

### Task 5 — Evidence of purchasing a weapon.

<p align="center"><img src="Project%20Screenshot/47.jpeg" alt="Weapon purchase evidence"></p>
<p align="center"><img src="Project%20Screenshot/48.jpeg" alt="Weapon purchase evidence"></p>

These messages indicate a weapon was purchased, with the location given as Gardeners at 7:45 on 2019-03-18.

### Task 6 — Evidence placing the suspect at the victim's house on the day of the murder (10 July 2019).

<p align="center"><img src="Project%20Screenshot/49.jpeg" alt="Placement evidence"></p>
<p align="center"><img src="Project%20Screenshot/50.jpeg" alt="Placement evidence"></p>
<p align="center"><img src="Project%20Screenshot/51.jpeg" alt="Placement evidence"></p>
<p align="center"><img src="Project%20Screenshot/52.jpeg" alt="Placement evidence"></p>

The messages between the suspect and the victim show that, on 9 July 2019, the suspect arranged to visit the victim's house the following day — 10 July 2019, the date of the murder. This places the suspect at the scene on the day in question.

<p align="right">(<a href="#top">back to top</a>)</p>

---

## Skills demonstrated

- Forensic examination of both **disk** and **mobile** images with Autopsy
- **File-signature analysis** and **file carving** from unallocated space
- **Metadata forensics** on documents and images, including EXIF/GPS geolocation
- **Keyword search** strategy, and the distinction between raw and indexed searches and the role of slack space
- Building **evidence-based conclusions** suitable for a formal case report

## Tools

Autopsy · ExifTool · Kali Linux forensic utilities · Google Maps (geolocation verification)

## Author

Asif Alif — digital forensics, network security, and post-quantum cryptography.

<p align="right">(<a href="#top">back to top</a>)</p>
