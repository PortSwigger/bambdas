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
java -jar BambdaChecker-1.3.jar
```

Verify the output. To do this quickly, check the exit code is 0 for a valid run. 

This will also update or generate markdown files as appropriate. This is only for pre-submission validation and these changes should not be included within your pull request.

If you only want to perform the validation check without affecting the markdown, then run:

```
java -jar BambdaChecker-1.3.jar validateonly
```

### What it checks for

- JavaDoc comments containing the Bambda description and @author tag.

## Submission Guidelines

1. Please make sure the Bambda is syntactically valid.
2. Please make sure the Bambda is formatted correctly.
   - Ensure that there is a JavaDoc style comment describing the Bambda containing an appropriate @author tag. For an example see [this bambda](https://github.com/PortSwigger/bambdas/blob/main/Proxy/HTTP/FilterOnCookieValue.bambda).
   - You may provide a link to your GitHub profile in the format `@author <author_name> (https://github.com/<author_profile>)`. Links must not be obscured.
   - Your description should be relatively short and precede the author tag. Longer details can be added after the author tag. These will remain in the Bambda, but will not be included in the generated markdown.
   - Indentation is four spaces, not tabs.
   - Ensure that the filename uses camel casing.
3. Please make sure the Bambda is optimized.
4. Please avoid excessive use of comments.
   - Use of appropriately named variables should mean that your Bambda is self-documenting.
5. Please ensure that your submission does not modify or include any additional markdown files.
6. Bambdas that attempt to reimplement *Burp Suite Professional* functionality will not be accepted.

## Code of Conduct
Please ensure that you are familiar with and respect our [code of conduct](https://github.com/PortSwigger/bambdas/blob/main/CODE_OF_CONDUCT.md).
