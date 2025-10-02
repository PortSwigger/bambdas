# Bambda scripts

Welcome to the official Bambda scripts repository from PortSwigger. This repo contains a collection of scripts developed by both PortSwigger and the community with 🧡

---

## 📑 On this page

- [Types of Bambda scripts](#types-of-bambda-scripts)
- [Repository contents](#repository-contents)
- [Importing scripts into Burp](#importing-scripts-into-burp)
- [Updating scripts in your library](#updating-scripts-in-your-library)
- [Contributing your own scripts](#contributing-your-own-scripts)
- [Resources](#resources)

---

## Types of Bambda scripts

Bambdas are scripts that run in supported Burp tools. They enable you to quickly personalize Burp Suite by creating:

- **Table filters** – Dynamically filter tables in Burp.
- **Table columns** – Add custom table columns to surface important data.
- **Repeater custom actions** – Extract, transform, and analyze data in Burp Repeater.
- **Match and replace rules** – Replace parts of HTTP and WebSocket messages as they pass through the proxy.
- **Custom scan checks** – Create your own active and passive scan checks. This repo contains checks written in Java. For checks written in our BChecks language, see the [BChecks repository](https://github.com/PortSwigger/BChecks).

> 💡 You can use table filter scripts in both **Burp Suite Community Edition** and **Burp Suite Professional**. All other scripts require **Burp Suite Professional**.

---

## Repository contents

You can explore the repository by script type:

### Table filters
- [HTTP history](https://github.com/PortSwigger/bambdas/tree/main/Filter/Proxy/HTTP)
- [WebSockets history](https://github.com/PortSwigger/bambdas/tree/main/Filter/Proxy/WS)
- [Site map](https://github.com/PortSwigger/bambdas/tree/main/Filter/SiteMap)
- [Logger view filter](https://github.com/PortSwigger/bambdas/tree/main/Filter/Logger/View)

### Table custom columns
- [HTTP history](https://github.com/PortSwigger/bambdas/tree/main/CustomColumn/Proxy/HTTP)
- [WebSockets history](https://github.com/PortSwigger/bambdas/tree/main/CustomColumn/Proxy/WS)
- [Logger](https://github.com/PortSwigger/bambdas/tree/main/CustomColumn/Logger)

### Other types
- [Repeater custom actions](https://github.com/PortSwigger/bambdas/tree/main/CustomAction)
- [Match and replace rules](https://github.com/PortSwigger/bambdas/tree/main/MatchAndReplace)
- [Custom scan checks](https://github.com/PortSwigger/bambdas/tree/main/CustomScanChecks)
  - This repo contains checks written in Java. To view or contribute checks written in our BChecks language, see the [BChecks GitHub repository](https://github.com/PortSwigger/BChecks).

---

## Importing scripts into Burp

To use scripts from this repository, import them into your Bambda library in Burp. Once imported, you can load your scripts across Burp and in different projects as required.

To import GitHub scripts into Burp:
1. Download scripts from this repo, or download the full repo as a ZIP file.
2. If using the ZIP file, extract its contents.
3. In Burp, go to **Extensions > Bambda library**.
4. Click **Import**. The **Import scripts** dialog opens.
5. Select the `.bambda` files or the extracted ZIP folder.
6. Click **Open**.

Burp adds the selected files to your Bambda library. If you select a folder, Burp automatically finds and includes any `.bambda` files within it and its subfolders.

> ⚠️ **Warning:** Scripts can run arbitrary code. For security reasons, please be cautious when importing and using scripts.

---

## Updating scripts in your library

To keep your scripts up to date with the latest changes in this repository, simply re-import them. Burp prompts you to confirm whether to overwrite existing scripts.

For more detailed guidance, see [Updating your scripts](https://portswigger.net/burp/documentation/desktop/extend-burp/bambdas/importing#updating-your-scripts).

---

## Contributing your own scripts

Thank you for contributing to the community 🧡 We love seeing your scripts!

### If you're new to contributing:
Start with the step-by-step guide:  
➡️ [Submitting scripts to our GitHub repository](https://portswigger.net/burp/documentation/desktop/extend-burp/bambdas/creating/contribute-scripts)

### If you've contributed before:
Check out the quick reference guide to refresh your memory on the process and guidelines:  
➡️ [Contributing quick reference guide](https://github.com/PortSwigger/Bambdas/blob/main/CONTRIBUTING.md)  

Please make sure you are familiar with and respect our [Code of Conduct](https://github.com/PortSwigger/bambdas/blob/main/CODE_OF_CONDUCT.md) when making submissions.

---

## Resources

### Learn more about script types:
- [**Bambdas documentation**](https://portswigger.net/burp/documentation/desktop/extend-burp/bambdas) – Detailed information on all script types and where they can be used.
- [**Bambdas**](https://www.youtube.com/watch?v=neQpukwW43g) – A quick video introduction with examples of filter scripts.
- [**Bambda table filters**](https://www.youtube.com/watch?v=EYSsd2I7qcs) – Video overview of table filter scripts.
- [**Bambda table customization**](https://www.youtube.com/watch?v=QyME5blj3e4) – Video overview of creating custom table column scripts.
- [**Introducing Custom Actions**](https://www.youtube.com/watch?v=u3GX4LgMdHQ) – Video on using custom actions to customize Burp Repeater.
- [**Introducing the Bambda library**](https://www.youtube.com/watch?v=XtkXHCG4RL8) – Video on storing and managing your scripts.

### Learn to write your own scripts:
- [**Creating scripts documentation**](https://portswigger.net/burp/documentation/desktop/extend-burp/bambdas/creating) – Guidance on creating scripts in Burp, including reference material and examples.
- [**Bambda output console**](https://www.youtube.com/watch?v=J1kN8yDRzMo) – Video on using the output console to test and debug your scripts.

### See scripts in action:
- [**Finding that one weird endpoint, with Bambdas**](#) – Blog post by [James Kettle]([https://portswigger.net/research](https://portswigger.net/research/finding-that-one-weird-endpoint-with-bambdas)), on using filter scripts during testing.
- [**Lab: Limit overrun race conditions**](https://portswigger.net/web-security/race-conditions/lab-limit-overrun-race-condition) – Web Security Academy lab that uses a custom action.
