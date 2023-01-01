# GitHub-Actions-Exercise

This repository illustrate a simple example of how to use [Pylint](https://pylint.pycqa.org/en/latest/) with the *GitHub Actions*. Pylint is a static code analyzer, it looks for errors and enforces coding standards. 

The structure of this repository is straightforward, it includes a directory *src*, which contains a python file (*main.py*). A GitHub Action workflow is created that setup python (version 3.9), installs dependencies (i.e upgrade pip and install pylint), and finally analyses the code with the pylint. Further, a branch protection rule is set up that requires every pull request to pass all checks and one approving review to accept the merge.

The *main.py* contains a single line of code, that prints "Hello World". But, according to pylint's coding standard, any non-empty python file, should contain a docstring at the top. Until this docstring is missing, any pull request will not pass the pylint check.

To illustrate the capability of pylint and GitHub actions, I have created two branches (*development* and *development_fix*), *development_fix* branch includes docstring in *main.py* file, thus its pull request passes all checks. Whereas, the *development* branch doesn't follow pylint's standards and fails its checks.
