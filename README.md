# Github-Actions-Exercise

This reprository illustrate a simple example on how to use [Pylint](https://pylint.pycqa.org/en/latest/) with the *Github Actions*. Pylint is a static code analyser, it looks for errors and enforces coding standards. 

The structure of this repository is very simple, it includes a directory *src*, which contains a python file (*main.py*). A Github Action workflow is created that setup python (version 3.9), install dependencies (i.e upgrade pip and install pylint) and finally analyse the code with the pylint. Further, a branch protection rule is setup that requires every pull-request to pass all checks and one approving review to accept the merge.

The *main.py* contains a single line of code, that prints "Hello World". But, according to pylint's coding standard, any non-empty python file, should contain a docstring at the top. Untill this docstring is missing, any pull request will not pass the pylint check.

To illustrate the capability of pylint and github actions, I have created two branches (*development* and *development_fix*), *development_fix* branch includes docstring in *main.py* file, thus its pull request passes all check. Whereas, *development* branch doesn't following pylint's standards and fails its checks.
