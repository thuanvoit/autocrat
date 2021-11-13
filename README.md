# HOW TO AUTOCRAT SHEETS AND DOCS

**REQUIREMENTS:**

**Autocrat** add-on (installed on KissickLab Drive Account)

**Templates** available under directory **/Rafi\_Lab\_Label\_Printer/Templates [DO NOT MODIFY]/**

**Data Sheets** with a column **QR CODE LINK**.  Please refer [**\[HOW TO\]**](https://docs.google.com/document/u/1/d/1k9xcFDAskF0ogZGzIpSG9CTIrpjm2IKcPghAZOIswsY/edit) to generate QR CODE.

**[PLEASE USE A COPY OF YOUR ORIGINAL DATA SHEET TO GENERATE LABEL]**

-----
**Google Sheet sample data used:**

![](source/pic.001.png)

**Google Docs Template used:**

|![](source/pic.002.png)|<p></p><p>**<<QR\_CODE>>** links to QR CODE LINK</p><p>**<<PATIENT\_NA>>** links to NAME</p><p>**<\<DATE\>>** links to DATE</p><p>**<\<WHOM\>>** links to BY</p>|
| :- | :- |
-----
**STEPS TO MERGE DATA**

**STEP 1:**

On your Google Sheets data, launch **Autocrat** under **Extensions** dropdown menu.

![](source/pic.003.png)



**STEP 2:**

> Click ![](source/pic.004.png) on the job if you have the same Sheets layout and Docs template. Click on ![](source/pic.005.png) to create a new job.  Name your job and click ![](source/pic.006.png) to the next step.

![](source/pic.007.png)

> Search template named **"1.5x0.5 Thermal Label Template v2"** and select it.

![](source/pic.008.png)

> This screen indicates the template is selected.  Click the Next button.

![](source/pic.009.png)



**STEP 3:**

> Select the Sheet you’d like to merge data as in the picture below. 

![](source/pic.010.png)

![](source/pic.011.png)

**STEP 5:**

> Name the file which will be saved after merging Sheets data and template.

> Type should be Google Docs for the best result.  **Single output mode** and **No Page Breaks.**

![](source/pic.012.png)



**STEP 6**: Select the destination folder on Drive for the export labels.

![](source/pic.013.png)![](source/pic.014.png)

**STEP 7:**

> Save the job and click the RUN button to merge.

![](source/pic.015.png)



**Sheets after merging.**  [Many columns created after merging, recommend using a copy of the original data sheet.]

![](source/pic.016.png)

**Labels after merging.** [MUST EXPORT TO PDF]

![](source/pic.017.png)

**Export this Docs to PDF to print.**

![](source/pic.018.png)


-----
# QR CODE GENERATING
**QR CODE LINK FOR LABEL (REQUIRED):**

Create the last column named **QR CODE LINK**.  The formula below generates a link to **QR CODE** for each patient, where **PATIENT-CODE** is the patient's unique code (cell position).

>=HYPERLINK("https://api.qrserver.com/v1/create-qr-code/?size=1000x1000&data="&ENCODEURL(**PATIENT-CODE**))

Example:

![](>qr_gen.001.png)


-----
**QR CODE IMAGE (OPTIONAL):**

Create a column named **QR CODE IMAGE**.  The formula below generates a **QR CODE** image embedded in a cell, where **PATIENT-CODE** is the patient's unique code (cell position).

>=image("https://api.qrserver.com/v1/create-qr-code/?size=500x500&data="&ENCODEURL(**PATIENT-CODE**))

Example:

![](source/qr_gen.002.png)

Result: 

![](source/qr_gen.003.png)