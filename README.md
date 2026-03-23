
#### **Step 1:** Git clone
```bash
git clone https://github.com/salmonbara/OSCP-Exam-Report-Template-Markdown.git
cd OSCP-Exam-Report-Template-Markdown/OSCP-Template-Report
```

#### **Step 2:** md structure before convert to docx
```bash
┌──(smbr㉿kali)-[~/Desktop/OSCP-Template-Report]
└─$ tree
├──  '4.1 Target #1 – 192.168.0.0.md'
├──  '4.2 Target #2 – 192.168.0.0.md'
├──  '4.3 Target #3 – 192.168.0.0.md'
├──  '5.1 MS01 – 192.168.0.0.md'
├──  '5.2 MS02 – 10.0.0.0.md'
├──  '5.3 DC01 – 10.0.0.0.md'
├──  'image 1.png'
├──  'image 2.png'
└──  OSCP-Exam-Report.docx
```

#### **Step 3:** Install pandoc package
```bash
sudo apt install pandoc
```

#### **Step 4:** Convert all .md to docx file
```bash
# Without template file
┌──(smbr㉿kali)-[~/Desktop/OSCP-Template-Report]
└─$ pandoc *.md \                                                                  
-f gfm \                               
-V mainfont="Aptos" \                  
-V monofont="Aptos" \                  
--highlight-style=breezedark \         
-o OSCP_Exam_Report.docx

# With offsec template file 
# Download from https://www.offsec.com/pwk-online/OSCP-Exam-Report.docx
┌──(smbr㉿kali)-[~/Desktop/OSCP-Template-Report]
└─$ pandoc *.md \                                                                  
-f gfm \                               
-V mainfont="Aptos" \                  
-V monofont="Aptos" \                  
--highlight-style=breezedark \         
--reference-doc=OSCP-Exam-Report.docx \
-o OSCP_Exam_Report.docx
```
