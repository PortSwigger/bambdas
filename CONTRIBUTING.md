# Contributing

When contributing to this repository, please first feel free to raise a pull request.

Please note that we have a code of conduct. Please follow it in all your interactions with the project.

## Pull Request Process

Your submission should only include .bambda files. The README.md files are automatically updated or generated after pull requests have been merged based on the description within your Bambda (see [Bambda Checker](#bambda-checker) below).
1. Place your Bambda in the appropriate folder.
2. Include a description of the Bambda you are adding in the pull request.
3. Make sure the Bambda follows our [Submission Guidelines](#submission-guidelines).
4. Engage with any comments and feedback given in the review.
5. If your pull request contains multiple Bambdas, please be aware that you may be asked to split your PR. This would happen if some Bambdas require further feedback while others are ready to merge.

### Bambda Checker
This is a standalone Java program that is run as part of the pull request process. It performs basic validation against Bambdas and is also used to generate or update the README.md files. It can be run manually, e.g. if you want to see how your Bambda will appear in the markdown files.

### How to run manually

Requirements: Java 17+

In the top level directory of the folder containing your Bambdas, run the following command:
```
java -jar BambdaChecker-1.1.jar
```

Verify the output. To do this quickly, check the exit code is 0 for a valid run. 

This will also update or generate markdown files as appropriate. This is only for pre-submission validation and these changes should not be included within your pull request.

If you only want to perform the validation check without affecting the markdown, then run:

```
java -jar BambdaChecker-1.1.jar validateonly
```

### What it checks for

- JavaDoc comments containing the Bambda description and @author tag.

## Submission Guidelines

1. Please make sure the Bambda is syntactically valid.
2. Please make sure the Bambda is formatted correctly.
   - Ensure that there is a JavaDoc style comment describing the Bambda containing an appropriate @author tag. For an example see [this bambda](https://github.com/PortSwigger/bambdas/blob/main/Proxy/HTTP/FilterOnCookieValue.bambda).
   - Your description should be relatively short and preceed the author tag. Longer details can be added after the author tag. These will remain in the Bambda, but will not be included in the generated markdown.
   - Indentation is four spaces, not tabs.
   - Ensure that the filename uses camel casing.
3. Please make sure the Bambda is optimized.
4. Please avoid excessive use of comments.
   - Use of appropriately named variables should mean that your Bambda is self-documenting.
5. Please ensure that your submission does not modify or include any additional markdown files.



## Code of Conduct

### Our Pledge

In the interest of fostering an open and welcoming environment, we as
contributors and maintainers pledge to making participation in our project and
our community a harassment-free experience for everyone, regardless of age, body
size, disability, ethnicity, gender identity and expression, level of experience,
nationality, personal appearance, race, religion, or sexual identity and
orientation.

### Our Standards

Examples of behavior that contributes to creating a positive environment
include:

* Using welcoming and inclusive language
* Being respectful of differing viewpoints and experiences
* Gracefully accepting constructive criticism
* Focusing on what is best for the community
* Showing empathy towards other community members

Examples of unacceptable behavior by participants include:

* The use of sexualized language or imagery and unwelcome sexual attention or
advances
* Trolling, insulting/derogatory comments, and personal or political attacks
* Public or private harassment
* Publishing others' private information, such as a physical or electronic
  address, without explicit permission
* Other conduct which could reasonably be considered inappropriate in a
  professional setting

### Our Responsibilities

Project maintainers are responsible for clarifying the standards of acceptable
behavior and are expected to take appropriate and fair corrective action in
response to any instances of unacceptable behavior.

Project maintainers have the right and responsibility to remove, edit, or
reject comments, commits, code, wiki edits, issues, and other contributions
that are not aligned to this Code of Conduct, or to ban temporarily or
permanently any contributor for other behaviors that they deem inappropriate,
threatening, offensive, or harmful.

### Scope

This Code of Conduct applies both within project spaces and in public spaces
when an individual is representing the project or its community. Examples of
representing a project or community include using an official project e-mail
address, posting via an official social media account, or acting as an appointed
representative at an online or offline event. Representation of a project may be
further defined and clarified by project maintainers.

### Enforcement

Instances of abusive, harassing, or otherwise unacceptable behavior may be
reported by contacting the project team via issues. All
complaints will be reviewed and investigated and will result in a response that
is deemed necessary and appropriate to the circumstances. The project team is
obligated to maintain confidentiality with regard to the reporter of an incident.
Further details of specific enforcement policies may be posted separately.

### Attribution

This Code of Conduct is adapted from the [Contributor Covenant][homepage], version 1.4,
available at [http://contributor-covenant.org/version/1/4][version]

[homepage]: http://contributor-covenant.org
[version]: http://contributor-covenant.org/version/1/4/
