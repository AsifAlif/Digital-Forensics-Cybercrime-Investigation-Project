<div id="top"></div>




<!-- PROJECT LOGO -->
<br />
<h3 align="center">Cyber Crime Investigation Project Report</h3>
<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/cyber.PNG">
</p>


  <p align="center">
   
</div>

<!-- ABOUT THE PROJECT -->
## About The Project


A group of People is involved in human trafficking, Here I have given a computer encase Image file to find out who is responsible for Human Trafficking.
I have also Given a Phone encase image file and after investigation of that Image file I have to find out who is the Murderer. I have also Given another Computer Image file from that i have to find out the suspicious files Related to that case. To do The proper Forensics Cyber crime investigation i have used Autopsy and many other kali linux Forensics Investigation tools.

<p align="right">(<a href="#top">back to top</a>)</p>



## Case 2: Stalking

A male suspect Rawi Hasse has been arrested for stalking and harassment. He was allegedly repeatedly taking pictures of his target, another male. He claims that he has no pictures of the target in his possession. He has been observed to use a Nexus 5 phone to take pictures.

Here i have been given the target picture to know what he looks like. His picture is:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/1.jpeg">
</p>

**Task 1:**

Perform a signature analysis to determine whether there are any suspicious files on the suspect's computer.

**Ans:**

After doing forensics investigation of Rawi Hasse  Computer hard drive i have found this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/2.jpeg">
</p>

From the above screenshot on the red marking area we can see the signature is missmatched and the original file was jpg but after missmatch it is in sys extention.

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/3.jpeg">
</p>

From here we can prove that the file signature of this file starts with FF D8 FF E0 that is the jpg file signature. But it has the sys extension. So we can clearly prove it is file signature extention mismatched.

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/4.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/5.jpeg">
</p>

From the above evidence we can clearly identify these are the suspicious files of that computer. **Task 2:**

Examine any suspicious files found relating to this case.

**Ans:**

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/6.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/7.jpeg">
</p>

These two are the suspicious files relating to these case. **Task 3:**

Use a technique of your choice to examine the Unallocated data on the disk to find at least one relevant jpg image of about 40kB in size. Show how you have done this.

**Ans:**

After doing the investigation i have found this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/8.jpeg">
</p>

From this picture we can see it is the target picture with 40kb in size and it is in jpg format and it is an unallocated data.

This image also relates this case.

## Case 3: Suspected Misrepresentation

Sheffield Travel is a specialist travel agent wanting to hire someone to handle trips to Rome. Mira Chep applied for the post, and has provided a reference in Microsoft Word format to accompany her job application. Mira claims that the reference comes from Sara Bartholomew at BlueSkyTravel, where she says she worked as a travel consultant in Rome for 6 months. The Human Resources department of Sheffield Travel contacted BlueSkyTravel, and were told by Sarah Bartholomew that Mira had worked at BlueSkyTravel, but had left quite suddenly after an argument. Sara Bartholomew emailed a reference to Mira Chep on 1st July 2015.

You have been given a digital copy of the reference from Mira Chep to examine and determine whether it is authentic or not.

The job Mira applied for at Sheffield Travel requires experience of travelling in Rome. Mira supplied a digital photograph of herself at the colosseum, claiming that it was taken by a fellow traveller using Mira's iPhone 6.

**Task 1:**

Explain the concept of metadata and its use in forensics examination. **Ans:**

A particular electronic file's history can be understood by digital or computer forensic investigators using metadata, which is frequently referred to as data about data. This history could include the date the file was created, when it was modified, and when it was accessed, among other info that can be used to describe the file.

Without the metadata we can not authenticate the origin of a file and all the others info that needed to run a forensics investigation.

With a picture metadata we can identify if a picture is real or not, if the picture is taken from a specific phone, if the photo is modified or not , the geolocation of the photo and all the others information to run a forensics investigation.

With a file metadata we can identify what kind of file it is, if the signature of the file is changed or not, at which time the file is modified and all the other information to run the investigation.

**Task 2:**

Examine the metadata relating to the reference given and report on your findings . **Ans:**

After checking the metadata of the Reference file with exiftool that Mira provided “Mira Chep Reference.docx” i have found this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/9.jpeg">
</p>

From here we can see the Author of this file is Sara Bartholomew and the created date was 2015-07-01 that means 1st July 2015. And we can also see that the company name is Blue Sky Travel.So we can say that this reference is real and authentic.

**Task 3:**

Examine the metadata of the photograph of the applicant in Rome, and report on your findings. **Ans:**

Here we have been given a photograph of Mira Chep named Colosseum.jpg. The picture is:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/10.jpeg">
</p>

After finding the meta data with exiftool i have found this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/11.jpeg">
</p>

Here from this screenshot we can see that camera model name that was used to take this picture is Nexus 5 not iphone 6.

I have found other metadata as well associated with this picture:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/12.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/13.jpeg">
</p>

From the above screenshot we can see the Geolocation of the place of the picture from where the picture were taken. That is: 41 deg 53' 24.64" N, 12 deg 29' 32.19" E

When i search with this geolocation on google map i found this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/14.jpeg">
</p>

We can see this place is in Rome and the also this is the exact place that was shown on the picture that was given to us.

So it is identified that the picture is taken from Rome of the exact location that she says. **Task 4:**

What recommendation would you make for Sheffield Travel .

**Ans:**

According to the evidence that i have got so far, i can say that Mira is saying the truth that she works for Blue Sky Travel. I have also test the metadata of the Reference letter that Mira provided and it is authentic and true. She also tells the truth about her photograph that was taken in Rome.

My recommendation for Sheffield Travel to take Mira as a employee of their company.Because Mira says the truth and all the evidence proves that. She had got experience from her previous company and also the the real reference letter. She could be a valuable Travel Agent and employee for their company.

## Case 4: Refugees across Europe

According to the document we know that, Kyle Dammer in Austria is suspected of involvement in human trafficking of refugees from Syria through Europe.It is also suspected that he was in some way involved in the movement of the vehicle in which 27 refugees were found suffocated on the Austrian Border on 23 July 2015. Police seized his computer on 1 August 2015, and have asked you to examine the hard drive.

To analyze the hard drive i used the Digital Forensics investigation Tool  called Autopsy.

**Task 1:**

Use a keyword search to find the email address that Kyle Dammer uses, and to find up to three emails to or from Kyle Dammer which could be used as evidence that Kyle Dammer has been involved in trafficking refugees from Syria through Europe.

**Ans:**

To complete this task i use a keyword search on the autopsy with Kyle Dammer :

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/15.jpeg">
</p>

And i got this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/16.jpeg">
</p>

Here from this screenshot we can see the email address that Kyle Dammer used and that is : [**Kyle865@hotmail.com**](mailto:Kyle865@hotmail.com)

After that i have found this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/17.jpeg">
</p>

From here we can see the mail is coming from <Kyle865@hotmail.com> to [JDurmen@gmail.com ](mailto:JDurmen@gmail.com)I have also found this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/18.jpeg">
</p>

From this picture we can see the mail is coming from <Kyle865@hotmail.com> to <jomag@pmail.co.pl> . And after reading the mail conversation we can understand that Kyle Dammer is involved in human trafficking in Europe.

I have also found this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/19.jpeg">
</p>

From this picture we can see the mail is coming from Ben Toman to Kyle Dammer.

So according to the above Evidence i have found the mail address that Kyle Dammer used and i have also found the three emails and also their conversation that clearly proves that Kyle Dammer has been involved in trafficking refugees from Syria through Europe.

**Task 2:**

Use Keyword Searches to find the names of four possible contacts who may have worked with Kyle Dammer

**Ans:**

After doing the  Keyword Searches with Kyle Dammer i have found this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/17.jpeg">
</p>

The first contact is **Jako Durmen** and his email address is <JDurmen@gmail.com>
<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/18.jpeg">
</p>

We can see from the above picture email conversation the second contact who worked with  Kyle Dammer is **Jo Magdi** and the email address is <jomag@pmail.co.pl>

I have found this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/20.jpeg">
</p>

From the above screenshot we can see the Third possible contact who worked with Kyle Dammer is **Josip Kova** and the mail address is <JosipK@t-com.hr>

I have also found this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/19.jpeg">
</p>

From the screenshot we can see the fourth contact who worked with  Kyle Dammer is **Ben Toman .**

**Task 3:**

Find one email ruling out one of the accomplices. **Ans:**

During investigation of the Hard disk i have found this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/21.jpeg">
</p>

From the above screenshot we can see a email conversation from **Jo Magdi** to **Kyle Dammer**. After reading the conversation we can see that **Jo Magdi** wants him out of this human trafficking plan . So we can say that **Jo Magdi** that means <jomag@pmail.co.pl> this email wants him out from this plan.

**Task 4:**

Find physical addresses associated with two accomplices. **Ans:**

During Investigation i have found this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/22.jpeg">
</p>

From the above screenshot we can see Josip Kova physical address is Croatia. I have also found this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/23.jpeg">
</p>

By this picture we can tell Jako Durmen physical address is in Europ. **Task 5:**

Explain the difference between a "raw search" and an "indexed search". State which search you have used and why

**Ans:**

Raw search means that searches only look for matches in text files using a line-by-line search. Binary files are not searched. In Autopsy on the keyword search box the Exact match is the raw search. It searches line by line.

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/15.jpeg">
</p>

From this picture we can see the raw search in autopsy. We can see i have used the raw search here because it searches one by one and takes short time to execute and returns time faster compared to the indexed search.

Indexed searches look for matches in text and binary files. It searches word by word. The string we enter in indexed search it searches every word of the string to every line of the image file. So it takes longer time to execute. In autopsy the substring match, Regular expression is the Indexed search.

**Task 6:**

Explain what "slack space" is, how data may be left in slack space and how it may be found using forensic tools.

**Ans:**

Slack space is the extra storage that remains on a computer's hard drive when a file does not require the entire amount of space that the operating system has allocated. Slack space analysis is a crucial part of computer forensics.

Usually, computers store files on hard drives in groups of a particular file size. Data may be kept on the hard drive in clusters of four kilobytes, for example, depending on the file system. There will be two kilobytes of slack space if the computer saves a file that is only two kilobytes in a four kilobyte cluster.

Slack space is an important form of evidence in the forensic investigation industry. Slack space often has pertinent details on a suspect that a prosecutor might utilize in trial. For example, if a user saved new files that only filled half of a hard drive cluster after deleting data that took up the entire cluster, the half would not necessarily be vacant. It might include any information that was left over from the deleted files. Using specialized computer forensic tools, forensic investigators may extract this information.

## Case 5: Jodi Arias-Murder Suspect

**Task 1:**

What are the IMSI and ICCID numbers for Jodi’s phone?

During the investigation with the GalaxyNexusArias-dm0.dd file with Autopsy tool i have found this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/24.jpeg">
</p>

From here we can see i have found the IMSI number and that is: **2060188** I have also found this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/25.jpeg">
</p>

From here we can see that i have found the ICCID number and that is: **5b514492-dd44-49d1-a155-f32802a74d8c**

**Task 2:**

Evidence of a motive for Murder **Ans:**

After investigating Jodi Arias phone image file i have found the conversation between Travis Alexander and Jodi Arias. I am attaching the screenshots of the conversation between them to prove the motive of the murder.

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/26.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/27.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/28.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/29.jpeg">
</p>
<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/30.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/31.jpeg">
</p>
<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/32.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/33.png">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/34.png">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/35.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/36.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/37.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/38.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/39.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/40.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/41.jpeg">
</p>

From the above conversation we can see Travis Alexander had a relationship with a girl penny other than Jodi Arias. Jodi Arias somehow knows that her boyfriend has a relation with another girl. The make argument with each other with this. By reading the conversation we can also see Travis Alexander wants to go paris with penny and by reading this messages penny got angry and she messaged penny that if she goes to paris with Travis Alexander then she will kill him and break penny’s legs.

This is the motive of the murder.

**Task 3: Evidence of False Alibi**

**Ans:**

From the forensics investigation of Jodi’s phone i have found this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/42.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/43.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/44.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/45.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/46.jpeg">
</p>

From the conversation between jodi and Mabel we can see jodi did go to Mabel’s house on 9th july 2019.

**Task 4: Evidence of Links with Edgar Kanne**

What evidence can you find that Jodi is not telling the truth when she states

She does not know Edgar Kanne

She has never been to his house

**Ans:**

From the document we know that Edgar Kanne is a drug and gun dealer. During the investigation i have found this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/47.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/48.jpeg">
</p>

From the above conversation we can see that, jodi knows Edger kanne and she had gone to his house to make a deal to buy Arms.

**Task 5: Evidence of purchasing a weapon**

Police suspect that Jodi may have purchased a weapon to kill Travis. What evidence can you find that Jodi may have purchased a weapon. Give the location, date and time of a likely purchase with reasons for your deductions.

**Ans:**

After doing the proper investigation i have found this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/47.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/48.jpeg">
</p>

From these two screenshot we can see Jodi did purcase the weapon and the location was Gardeners at 7:45 on 2019-03-18

**Task 6:**

What evidence is there that locates Jodi at Travis Alexander's house on Wednesday 10th July 2019, the date of the Murder?

**Ans:**

During investigation i have found this:

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/49.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/50.jpeg">
</p>

<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/51.jpeg">
</p>
<p align="center">

<img src="https://github.com/AsifAlif/Digital-Forensics-Cybercrime-Investigation-Project/blob/main/Project_Case_1/Project%20Screenshot/52.jpeg">
</p>
From these conversation screenshot between jodi and Travis we can understand that, on 9th july 2019 jodi told Travies that she would go to Travis house the other day that means 10th july 2019 that is the murder day and wearing Travis favourites. Travis said ok and he was free all night on 10th july 2019.

This proves that Jodi had gone to Travis house on 10th july 2019 on the Murder day.
