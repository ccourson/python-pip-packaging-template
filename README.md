# Example Package

This is a simple example package. You can use
[Github-flavored Markdown](https://guides.github.com/features/mastering-markdown/)
to write your content.

From article:
[Packaging Python Projects](https://packaging.python.org/tutorials/packaging-projects/)

## Generating distribution archives

Unix

    python3 -m pip install --upgrade build
    python3 -m build

Windows

    py -m pip install --upgrade build
    py -m build

## Uploading the distribution archives

The first thing you’ll need to do is register an account on Test PyPI. https://test.pypi.org/account/register/

Create token: https://test.pypi.org/manage/account/#api-tokens

For the username, use \_\_token__

For the password, use the token value, including the pypi- prefix plus token value.

Unix

    python3 -m pip install --user --upgrade twine
    python3 -m twine upload --repository testpypi dist/*

Windows

    py -m pip install --user --upgrade twine
    py -m twine upload --repository testpypi dist/*
