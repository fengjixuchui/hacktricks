# Office file analysis

{{#include ../../../banners/hacktricks-training.md}}

<figure><img src="../../../images/image (48).png" alt=""><figcaption></figcaption></figure>

\
Use [**Trickest**](https://trickest.com/?utm_source=hacktricks&utm_medium=text&utm_campaign=ppc&utm_content=office-file-analysis) to easily build and **automate workflows** powered by the world's **most advanced** community tools.\
Get Access Today:

{% embed url="https://trickest.com/?utm_source=hacktricks&utm_medium=banner&utm_campaign=ppc&utm_content=office-file-analysis" %}

For further information check [https://trailofbits.github.io/ctf/forensics/](https://trailofbits.github.io/ctf/forensics/). This is just a sumary:

Microsoft has created many office document formats, with two main types being **OLE formats** (like RTF, DOC, XLS, PPT) and **Office Open XML (OOXML) formats** (such as DOCX, XLSX, PPTX). These formats can include macros, making them targets for phishing and malware. OOXML files are structured as zip containers, allowing inspection through unzipping, revealing the file and folder hierarchy and XML file contents.

To explore OOXML file structures, the command to unzip a document and the output structure are given. Techniques for hiding data in these files have been documented, indicating ongoing innovation in data concealment within CTF challenges.

For analysis, **oletools** and **OfficeDissector** offer comprehensive toolsets for examining both OLE and OOXML documents. These tools help in identifying and analyzing embedded macros, which often serve as vectors for malware delivery, typically downloading and executing additional malicious payloads. Analysis of VBA macros can be conducted without Microsoft Office by utilizing Libre Office, which allows for debugging with breakpoints and watch variables.

Installation and usage of **oletools** are straightforward, with commands provided for installing via pip and extracting macros from documents. Automatic execution of macros is triggered by functions like `AutoOpen`, `AutoExec`, or `Document_Open`.

```bash
sudo pip3 install -U oletools
olevba -c /path/to/document #Extract macros
```

<figure><img src="../../../images/image (48).png" alt=""><figcaption></figcaption></figure>

\
Use [**Trickest**](https://trickest.com/?utm_source=hacktricks&utm_medium=text&utm_campaign=ppc&utm_content=office-file-analysis) to easily build and **automate workflows** powered by the world's **most advanced** community tools.\
Get Access Today:

{% embed url="https://trickest.com/?utm_source=hacktricks&utm_medium=banner&utm_campaign=ppc&utm_content=office-file-analysis" %}

{{#include ../../../banners/hacktricks-training.md}}
