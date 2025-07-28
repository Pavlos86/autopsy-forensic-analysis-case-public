# Forensic Analysis Report: The John Doe Case

*Exercise designed to practice digital forensic analysis skills with Autopsy, based on the examination of a .E01 image obtained from a suspicious Windows system.*

## 🌱 How to Start This Project?

In this lab, you will simulate the role of a digital forensic analyst who receives a segmented `.E01` image, previously created with [FTK Imager](https://www.exterro.com/digital-forensics-software/ftk-imager) on Windows.

> ℹ️ If you want to learn how the `.E01` image was created, check the complementary article: [How to Generate a Forensic .E01 Image with FTK Imager](https://4geeks.com/lesson/how-to-create-a-forensic-e01-image-on-windows)

Your objectives will be:

- Download the segmented `.E01` image. [download here](https://storage.googleapis.com/cybersecurity-machines/evidence-jondoe-e01.zip)
- Analyze the image in [Autopsy](https://www.autopsy.com/).
- Investigate possible evidence of data exfiltration.

## Part 1 – Analysis with Autopsy

1. Open **Autopsy** and select **"New Case"**.
2. Load the `.E01` image as a **disk image or VM file**. You do not need to import each segmented image separately; just select the `.E01` file and the rest will load automatically, as **Autopsy** detects all associated segments as long as they are in the same folder and have sequential names.
3. Run the following modules:

    - File Metadata
    - Recent Activity
    - Data Artifacts
    - Deleted Files
    - Keyword Search

Explore artifacts such as: compressed files, recently opened files history, suspicious browsing, 7-Zip prefetch, recycle bin, and timeline.

## Part 2 - Technical Forensic Analysis Report

Next, you must complete a structured report with your findings. Each section contains a brief explanation to help you write a clear, professional, and evidence-based presentation.

### 1. Introduction

Write a general summary of the case. Include:

- The context: Who is the suspect? What type of incident is being investigated?
- The objective of your analysis.
- What type of evidence you received (a `.E01` image) and how it was processed.

> **Example:**  
> *A possible data leak committed by the internal user `johndoe` is analyzed. For this, a forensic `.E01` image extracted from a Windows Server 2019 system is examined. The goal is to identify traces of sensitive file manipulation, compression, browsing to transfer sites, and possible evidence deletion.*

### 2. Tools Used

List all tools used during your investigation. Include both forensic and complementary software.

**Example:**

- Autopsy 4.x
- ZIP file viewer (7-Zip, WinRAR, etc.)
- HashMyFiles (optional)
- Web browser (for searches)

### 3. Relevant Evidence

Clearly describe the evidence found that indicates malicious or suspicious activity. Organize it into subsections:

#### a. Manipulated Files

- Files recently opened or accessed.
- Paths, names, and timestamps.

#### b. Compression

- Evidence of software usage such as 7-Zip.
- Compressed file found (`backup.zip`).
- ZIP content and path.

#### c. Suspicious Browsing

- Web history (wetransfer, mega, etc.).
- Indicators of exfiltration intent.

#### d. Evidence Deletion

- Deleted files found in the recycle bin or recovered.
- System logs showing recent activity.

#### e. Prefetch and Artifacts

- Prefetch files showing execution of key programs (7-Zip, Notepad, browser).
- Approximate execution times.

### 4. Timeline

Reconstruct key events in chronological order. Use file metadata, prefetch, and recent activity.

> **Example:**
> ```
> 11:55 – Sensitive file accessed from an unusual path  
> 12:03 – Creation of a compressed file detected in a user folder  
> 12:11 – Browsing activity to file transfer services  
> 12:18 – Deletion actions recorded on the system  
> 12:25 – Clean shutdown event recorded by the system  
> ```

### 5. Conclusions

Write your conclusions as if presenting your report to a supervisor or client:

- Is there evidence of a possible data leak?
- What method was used?
- Which user was involved?
- What degree of intent or premeditation can be inferred?

> Avoid personal opinions: your analysis should be based on concrete evidence.

### 6. Annexes

Include any additional resources that support your investigation:

- Relevant screenshots.
- Hashes of key files.
- Absolute paths found.
- Log fragments, if applicable.

## 📦 How to Submit This Project?

The completed report must be submitted in `PDF` format through the academy platform.
