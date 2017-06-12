# Style Guide

## **Typed Commands**


---

###  **Text**

<p>
<pre>Here's an example:

&gt;\`\`\`bash
$ ifconfig
\`\`\`
</pre>
</p>

**`>`** - This makes it have the callout bar on the side
**```** - Wrapping text in triple backticks makes it a code blockquote
**`bash`** - This is the language that will be used for syntax highlighting

<br>

**Warning**: Be careful when choosing the language. The stable version of MDWiki uses highlight.js. If an unknown language is chosen then the page will never render. See https://github.com/dynalon/mdwiki/issues/39 for details. Using bash, python, and sql (in lowercase) all seem to work. Honestly, it rarely seems to do much highlighting at this point, so we could just ignore it for now. The unstable version of MDWiki replaces highlight.js with prism.js, but my understanding is that the master has issues that prevent successful build from source.

<br>

<!--

###  **Rendered**
>```
$ ifconfig
```

<br>
## **Links**

---

###  **Text**

```
[**`https://localhost/scanners/pilots.php`**](https://localhost/scanners/pilots.php)
```

<br>
###  **Rendered**
[**`https://localhost/scanners/pilots.php`**](https://localhost/scanners/pilots.php)
<br>
## **Tables**

---


###  **Text**

```
<table><tr bgcolor="grey"><th>Key Name</th><th>Type</th><th>Data</th></tr>
<tr><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr><tr><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr><tr><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr></table>
```

**Note:** The stable version of MDWiki has a bug in the way it handles HTML tables. The spacing increases associated with the number of lines the HTML spans. You will likely need to make the HTML less readable (span fewer lines) in order to not have lots of stray spacing.

<br>
###  **Rendered**

<table><tr bgcolor="grey"><th>Key Name</th><th>Type</th><th>Data</th></tr>
<tr><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr><tr><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr><tr><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr></table>

<br>
## **Spacing Issues**

---

<br>
### **Lack of space**

**Note:** Often a `<br>` tag will need to be added to increase the spacing of elements in the markdown view.
<br>
## **Text Callout/highlighting**

---

<br>

## **Tool Names/Actions**

---


Items that will be bolded:
Tool Names: Wireshark, tshark, bro, etc.
Actions: Click submit, Right-click, etc.
###  **Text**

```
**Wireshark**
```

<br>
###  **Rendered**

**Wireshark**
<br>
## **Paths/Shell Commands/Filenames**

---

###  **Text**

```
**`/etc/passwd`**
```
<br>
###  **Rendered**

**`/etc/passwd`**

## **Exercise Step Numbers**

---

<br>
### **Text**

```
**2\.**
```
<br>
### **Rendered**

**2\.**

## **Menu Navigation - Arrows**
### **Text**

```
&rarr;
```
<br>
### **Rendered**

&rarr;

## **Indentation**

---

<br>
### **Text**

```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A.  Click on packet 2051 (SYN) and expand the arrow next to "Transmission Control Protocol…."
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;B.  Right-click on "Flags: 0x002 (SYN)".
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;C.  Go to "Apply as Filter"
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;D.  Choose "…and Selected".
```
<br>
### **Rendered**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A.  Click on packet 2051 (SYN) and expand the arrow next to "Transmission Control Protocol…."
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;B.  Right-click on "Flags: 0x002 (SYN)".
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;C.  Go to "Apply as Filter"
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;D.  Choose "…and Selected".

-->
