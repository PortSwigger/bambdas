## Contributing

Thanks for contributing to the Bambdas repository! 🚀

> 🔎 Note on scan checks: This repository is for Java-based Bambda scripts (including custom scan checks). If you want to contribute scan checks written in the BChecks language, please head to the [BChecks repository](https://github.com/PortSwigger/BChecks?tab=contributing-ov-file) instead.

This page is a quick reference for users who have contributed before. It covers:

- An overview of the submission process  
- How to run validation manually  
- The submission requirements your script must meet

If this is your first time contributing, start with our step-by-step guide instead: [Submitting scripts to our GitHub repository](https://portswigger.net/burp/documentation/desktop/extend-burp/bambdas/creating/contribute-scripts).

> Please make sure you are familiar with and respect our [Code of Conduct](https://github.com/PortSwigger/bambdas/blob/main/CODE_OF_CONDUCT.md) when making submissions.

---

### 📦 Submission process overview

To ensure an efficient review, please submit one script at a time. Bundling multiple scripts may delay publication if any of them require changes.

Follow these steps to submit your script:

1. Add a Javadoc block at the top of your script that meets our [file requirements](https://github.com/PortSwigger/bambdas/blob/main/CONTRIBUTING.md#submission-guidelines).
2. Refine your script to meet our [quality standards](https://github.com/PortSwigger/bambdas/blob/main/CONTRIBUTING.md#submission-guidelines).
3. Export your script from Burp's Bambda library. Use camel case for the filename.
4. Fork our GitHub repository.
5. In the forked repo, add your script to the appropriate directory.
6. Run the [Validate Bambdas](https://github.com/PortSwigger/bambdas/actions/workflows/bambda-checker-validate-only.yml) GitHub workflow.
7. Open a pull request.

We'll review your submission and get back to you with any feedback.

---

### ✅ Submission guidelines

Each file must meet the following requirements:

- Be a `.bambda` file.  
  _Do not include or modify markdown files — `README.md` files are generated automatically after merge._
- Be in YAML format, containing the required metadata: `ID`, `name`, `function`, `location`, and `source`.  
  _To ensure metadata is correct, [export your script](https://portswigger.net/burp/documentation/desktop/extend-burp/bambdas/managing#exporting-scripts) from the Bambda library in Burp._
- Have a filename in camel case. For example, `MyCustomScript.bambda`
- Start with a Javadoc block, in the following order:
  1. A short description (1–2 sentences) of what the script does.
  2. An `@author` tag in this format:
     ```java
     @author <your_name> (https://github.com/<your_profile>)
     ```
     _Use a direct, unobscured GitHub profile link._
  3. If needed, add extra notes below the `@author` tag.  
     _These won’t appear in the directory README._
     
> For an example, see [this script](https://github.com/PortSwigger/bambdas/blob/main/Filter/Proxy/HTTP/FilterOnCookieValue.bambda).

Your code must meet the following quality standards:

- Compile successfully in Burp.
- Be readable and well-formatted:
  - Avoid long lines.
  - Use consistent code styling.
  - Avoid using tabs for indentation. Four spaces is preferred.
  - Use clear, descriptive variable names instead of excessive comments.
- Consider performance by avoiding unnecessary complexity or resource usage, which can slow down Burp.
- It doesn't replicate functionality that already exists in Burp Suite Professional.

---

### 🧪 Running validation locally

The easiest way to validate your script is by using the [Validate Bambdas](https://github.com/PortSwigger/bambdas/actions/workflows/bambda-checker-validate-only.yml) GitHub workflow. This automates the process and is the recommended option for most contributors.

If you prefer to validate locally during development, you can do so using Java 17 or higher.

To run validation locally:

1. Open a terminal and go to the top-level directory containing your script.
2. Run one of the following commands:
   - To validate only:  
     ```bash
     java -jar BambdaChecker-1.5.jar validateonly
     ```
   - To validate and generate an updated `README.md` (for your own reference only):  
     ```bash
     java -jar BambdaChecker-1.5.jar
     ```

> **Note:** Do not commit the locally generated `README.md` in your pull request.

3. Review the results. A successful run returns exit code `0`.
