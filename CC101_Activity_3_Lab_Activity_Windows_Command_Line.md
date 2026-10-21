# CC 101 Laboratory Activity: Exploring the Windows Command Line

**Sorsogon State University – College of Information and Communications Technology, Bulan Campus**

| Item | Details |
| --- | --- |
| Course | CC 101 Introduction to Computing (BSCS 1st Year) |
| Course Outcome | CO2: Identify the functions and relationships of major hardware and software components |
| Output | Command Line Exploration Documentation (PDF) |
| Estimated time | 2 to 2½ hours |
| Reference | CC 101 Lecture Notes: Exploring the Windows Command Line |
| Student | John Jeric L. Sola, BSCS 1-1 |

---

## Instructions

Follow every step in order, take the screenshots marked **[Screenshot]**, and answer the questions marked **[Answer]**.

- You need a Windows 10 or 11 computer. No administrator rights are needed.
- Take screenshots with `Windows + Shift + S`.
- Replace the sample values with your own details.
- Type every command yourself; do not copy and paste.

---

## Part A: Open the Two Shells

**Commands typed (Command Prompt):**

```
cls
echo "John Jeric L Sola BSCS 1-1"
```

**Figure A1.** Command Prompt showing the `echo` output.

![Figure A1](images/figure-A1.png)

**Commands typed (PowerShell):**

```powershell
echo "John Jeric L Sola BSCS 1-1"
```

**Figure A2.** PowerShell showing the `echo` output.

![Figure A2](images/figure-A2.png)

**A-Q1.** Compare the two prompts. What is different, and what does each part of the Command Prompt prompt mean?

> _(No answer recorded in the original worksheet.)_

---

## Part B: Inspect Your System (Command Prompt)

**Commands typed:**

```
whoami
hostname
ver
systeminfo | findstr /B /C:"OS Name" /C:"OS Version" /C:"System Type" /C:"Total Physical Memory"
ipconfig
```

**Figure B1.** `whoami`, `hostname`, and `ver` output.

![Figure B1](images/figure-B1.png)

**Figure B2.** Filtered `systeminfo` output.

![Figure B2](images/figure-B2.png)

**Figure B3.** `ipconfig` output showing the IPv4 address.

![Figure B3](images/figure-B3.png)

**B-Q1.** Results table:

| Item | Your result |
| --- | --- |
| Logged-in account (whoami) | PC-5\Administration |
| Computer name (hostname) | PC-05 |
| OS name | Microsoft Windows 10 Pro |
| OS version | 10.0.19045 N/A Build 19045 |
| System type (x64 or ARM) | x64-based PC |
| Total physical memory (RAM) | 15,675 MB |
| IPv4 address | 192.168.88.105 |

**B-Q2.** The `|` symbol is called a **pipe**. Run `systeminfo` alone and compare. What did `| findstr` do?

> The findstr is containing the text that you re looking for, while. The systeminfo show the detailed information about you computer.

---

## Part C: Build a Folder Structure

**Commands typed:**

```
cd %USERPROFILE%
mkdir CC101-Lab
cd CC101-Lab
mkdir Notes Projects Screenshots
echo Name: John Jeric Sola > profile.txt
echo Section: BSCS 1-1 >> profile.txt
echo Favorite app: YouTube >> profile.txt
type profile.txt
tree /F
```

**Figure C1.** All commands and the output of `type`.

![Figure C1](images/figure-C1.png)

**Figure C2.** `tree /F` showing the folder structure.

![Figure C2](images/figure-C2.png)

**Figure C3.** File Explorer and Notepad side by side showing `profile.txt`.

![Figure C3](images/figure-C3.png)

**C-Q1.** What would happen if you used `>` instead of `>>` in the second echo line? Test it on a new file (test.txt) and explain.

> _(No answer recorded in the original worksheet.)_

---

## Part D: Copy, Rename, and Delete Files

**Commands typed:**

```
copy profile.txt Notes\profile-copy.txt
cd Notes
ren profile-copy.txt about-me.txt
echo This file will be deleted > temp.txt
dir
del temp.txt
dir
cd ..
tree /F
```

**Figure D1.** From `copy` to the first `dir`.

![Figure D1](images/figure-D1.png)

**Figure D2.** From `del` to `tree /F`.

![Figure D2](images/figure-D2.png)

**D-Q1.** After `del temp.txt`, check your Recycle Bin. Is temp.txt there? What does this tell you about deleting files from the command line?

> _(No answer recorded in the original worksheet.)_

---

## Part E: Explore PowerShell

**Commands typed:**

```powershell
cd $HOME\CC101-Lab
Get-ChildItem
Get-Content profile.txt
$PSVersionTable
Get-Help Get-ChildItem
[Convert]::ToString(347, 2)
[Convert]::ToString(347, 8)
'{0:X}' -f 347
```

**Figure E1.** `Get-ChildItem`, `Get-Content`, and `$PSVersionTable`.

![Figure E1](images/figure-E1.png)

**Figure E2.** `Get-Help Get-ChildItem`.

![Figure E2](images/figure-E2.png)

**Figure E3.** Number conversions with PowerShell.

![Figure E3](images/figure-E3.png)

**E-Q1.** Write your number in decimal, binary, octal, and hexadecimal.

> _(No answer recorded in the original worksheet.)_

---

## Part F: Discover a New Command

**Command chosen:** `time /t` (Command Prompt)

**Figure F1.** Help output.

![Figure F1](images/figure-F1.png)

**Figure F2.** Command result (`time /t` returned `06:03 PM`).

![Figure F2](images/figure-F2.png)

**F-Q1.** What does your chosen command do, and when would it be useful?

> _(No answer recorded in the original worksheet.)_

---

## Part G: Reflection

**G-Q1.** Which task in this activity was faster in the CLI than in the GUI? Which was easier in the GUI? Explain why.

> For me the CLI, because like the command systeminfo quickly display.

**G-Q2.** What error did you encounter (if any), what caused it, and how did you fix it?

> One of the error that i encounter is the tree /f, to fix it i ask one of my classmate to help me, and it works that's how i fix it.

**G-Q3.** Give one real-world job or situation in computing where knowing the command line would be important.

> IT support because it use command line to troubleshoot computer, check system information, and fix network problem.

---

## Commands Learned

| Command | Shell | What it does |
| --- | --- | --- |
| `cls` | Command Prompt | Clears the screen |
| `echo` | Command Prompt / PowerShell | Displays text, or writes it to a file with `>` / `>>` |
| `whoami` | Command Prompt | Shows the logged-in account |
| `hostname` | Command Prompt | Shows the computer name |
| `ver` | Command Prompt | Shows the Windows version |
| `systeminfo` | Command Prompt | Shows detailed system information |
| `findstr` | Command Prompt | Filters lines containing given text |
| `ipconfig` | Command Prompt | Shows network adapter and IP information |
| `cd` | Command Prompt / PowerShell | Changes the current folder |
| `mkdir` | Command Prompt | Creates a folder |
| `type` | Command Prompt | Displays the contents of a file |
| `tree /F` | Command Prompt | Shows the folder structure including files |
| `copy` | Command Prompt | Copies a file |
| `ren` | Command Prompt | Renames a file |
| `dir` | Command Prompt | Lists files and folders |
| `del` | Command Prompt | Deletes a file |
| `Get-ChildItem` | PowerShell | Lists files and folders |
| `Get-Content` | PowerShell | Displays the contents of a file |
| `$PSVersionTable` | PowerShell | Shows PowerShell version details |
| `Get-Help` | PowerShell | Shows help for a command |
| `[Convert]::ToString()` | PowerShell | Converts a number to another base |
| `time /t` | Command Prompt | Displays the current time |
