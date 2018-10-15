<script>
function copyToClipboard(text) {
    if (window.clipboardData && window.clipboardData.setData) {
        // IE specific code path to prevent textarea being shown while dialog is visible.
        return clipboardData.setData("Text", text); 

    } else if (document.queryCommandSupported && document.queryCommandSupported("copy")) {
        var textarea = document.createElement("textarea");
        textarea.textContent = text;
        textarea.style.position = "fixed";  // Prevent scrolling to bottom of page in MS Edge.
        document.body.appendChild(textarea);
        textarea.select();
        try {
            return document.execCommand("copy");  // Security exception may be thrown by some browsers.
        } catch (ex) {
            console.warn("Copy to clipboard failed.", ex);
            return false;
        } finally {
            document.body.removeChild(textarea);
        }
    }
}
</script>

Welcome to the SANS SEC555 Wiki
----------


![Cyber Defense](CyberDefense_logo.jpg)
### **`SEC555 Portal Version: 1.0.3`**

---

The goal of the SEC555 wiki is to provide knowledge to the security community. As one gets better we all get better! As such this is a free source of cyber defense information primarily around Security Information Event Management (SIEM) systems.

The other goal is for (**SEC555: SIEM with Tactical Analytics**)[https://www.sans.org/course/siem-with-tactical-analytics] students and is to increase the **in-class**, and, most importantly, **after-class** value of the course material. It is also designed as a method to give back to the security community by providing free information. This wiki is, and likely always will be, very much a work in progress.

Contained in the wiki, you will find:

- Tool and technique cheat sheets
- Reference guides
- Information about 555 instructors
- Electronic Copies of the Lab Guides (**copy and paste, FTW!!!**) (**Digital labs are only available on student VM - SEC555 course attendees only**)
...and more

Note: If you are using the student VM included when taking SEC555 you have the capability of turning on automatic wiki/lab updating.

Recommendations - PLEASE READ
----------
There are two things that are **highly recommended** to do before diving in.

1. **Discover how to use the Smart Player**. Videos are played using Smart Player and there are some features you may not know exist without checking [out this guide](/Resources/SmartPlayer.md). The videos created in the wiki took a tremendous amount of time to put together due to adding many features that Smart Player allows such as searching for any word spoken by the presenter and jumping to that section of the video.
2. If you are a SEC555 student, **enable automatic updates of the wiki and lab content**

How to manually update the wiki
----------

To manually update the wiki content run the command below.

```bash
$ wikiup
```

<button onclick="copyToClipboard('wikiup')" style="background-image: url(/clipboard.svg); background-repeat: no-repat; height: 40px; width: 40px;"> 
</button>

<p> </p>

If the above command cannot be found your system is using the prior update script which can be ran using this command below:

```bash
$ sudo pwsh -file /scripts/wiki_update.ps1
```

<button onclick="copyToClipboard('sudo pwsh  -file /scripts/wiki_update.ps1')" style="background-image: url(/clipboard.svg); background-repeat: no-repat; height: 40px; width: 40px;"> 
</button>

<p> </p>

Enable Automatic Updates
----------

This section only applies to students of SEC555 using the wiki within the SEC555 course provided student virtual machine. In order to enable automatic wiki/lab updating run the following command:

```bash
sudo crontab -e
```

<button onclick="copyToClipboard('sudo crontab -e')" style="background-image: url(/clipboard.svg); background-repeat: no-repat; height: 40px; width: 40px;"> 
</button>

<p> </p>

Then uncomment the cron job for either the 9 AM automatic update or the update after reboot (or both):

```bash
# Uncomment the below entry to automatically update the SEC555
# wiki. The default check occurs at 9 AM but can be changed.
#0 9 * * * /bin/bash /opt/wikiup.sh

# Uncomment the below entry to automatically update the SEC555
# wiki after each reboot.
#@reboot bin/bash /opt/wikiup.sh
```

When finished the cron entry should look similar to this:

```bash
# Uncomment the below entry to automatically update the SEC555
# wiki. The default check occurs at 9 AM but can be changed.
0 9 * * * /bin/bash /opt/wikiup.sh

# Uncomment the below entry to automatically update the SEC555
# wiki after each reboot.
@reboot /bin/bash /opt/wikiup.sh
```

---


Course/Lab/Wiki Bugs or Suggestions
----------

---

Please let us know if you find any bugs in the courseware/labs/wiki we need to squash. Also, reach out if you have suggestions to improve the course (e.g. content/labs/tools that should be added, removed, or updated). The easiest way to submit these improvements is by sending an email to **<justin@hasecuritysolutions.com>**

---

Alumni Mailing List
----------

---

Join the 555 alumni Slack channel:

[https://sec555.com/slack.php](https://sec555.com/slack.php)

---
