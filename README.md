# Brute Force Login Tool

![GitHub repo size](https://img.shields.io/github/repo-size/Praveenms13/Brute-Force-Login?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)

## Overview

This is a simple Brute Force Login tool written in Python. It is designed to assist in testing the security of login forms or API login endpoints. The tool supports both GET and POST HTTP methods for brute force attacks and gives results based on the retrieved status code.

## Prerequisites

- Python3
- PIP

![Python Version](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge)
![GitHub top language](https://img.shields.io/github/languages/top/Praveenms13/Brute-Force-Login?style=for-the-badge)
![GitHub language count](https://img.shields.io/github/languages/count/Praveenms13/Brute-Force-Login?style=for-the-badge)
![GitHub last commit](https://img.shields.io/github/last-commit/Praveenms13/Brute-Force-Login?color=red&style=for-the-badge)

![GitHub stars](https://img.shields.io/github/stars/Praveenms13/Brute-Force-Login?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/Praveenms13/Brute-Force-Login?style=social)

## Features

- **Form Analysis:** Extracts and analyzes HTML form attributes to identify input names for username and password fields, extracts the `type` of an input tag or button tag, also extracts all the required tokens, cookies for a login session.

<p align="center">
  <img width="80%" src="inp.jpg" alt="Centered Image">
</p>

- **Wordlist Attack:** Supports username and password brute force attacks using a provided wordlist file.
- **GET and POST Methods:** Choose between GET and POST methods based on the target's login mechanism.
- **Cookie Support:** Optionally provide a cookie value for authentication.
- **User-friendly Interface:** Provides clear and colored console output for better user interaction.

## Installation (Release from PyPI)

[![PyPI Version](https://img.shields.io/pypi/v/brute-force-attacker?style=for-the-badge&logo=PyPI&logoColor=white)](https://pypi.org/project/brute-force-attacker/)
[![Supported OS](https://img.shields.io/badge/Works%20on-Ubuntu-E95420?style=for-the-badge&logo=Ubuntu&logoColor=white)](https://en.wikipedia.org/wiki/Ubuntu)

Install the `brute-force-attacker` package using pip:

```bash
pip install brute-force-attacker
```

Find the latest release on <a href="https://pypi.org/project/brute-force-attacker/">PyPI</a>.


### How to Run as command line tool

```
brute -w <wordlist_file> -t <target_url> -m <http_method> [-u <username>] [-c <cookie_value>]
```

- `-t` or `--target`: Specify the target URL.
- `-w` or `--wordlist`: Specify the wordlist file.
- `-m` or `--method`: Specify the HTTP method (get or post).

Optional arguments:

- `-u` or `--username`: Specify the username for targeted brute force (optional).
- `-c` or `--cookie`: Specify the cookie value for authentication (optional).

## Examples

### Brute Force Login using POST with username

#### Here admin is the username, word1.txt contains all the common passwords (Passwords only)

```
brute -w word1.txt -u admin -t "https://forms.praveenms.site/login.php" -m POST
```

### Brute Force Login using POST without username

#### By the below syntax you can run the brute force attack without usernames as it takes all the common username and password from the file named word2.txt

```
brute -w word2.txt -t "https://forms.praveenms.site/login.php" -m POST
```

### Brute Force Login using GET with Username

#### This works on HTTP Get method with username where the username is given and the password is left Blank where it is extracted from the word1.txt

```
brute -w word1.txt -t "https://forms.praveenms.site/login.php?username=admin&password=" -m GET
```

### Brute Force Login using GET with Username

#### This works on HTTP Get method without username and password where the username and password is left Blank, it is extracted from the word2.txt

```
brute -w word2.txt -t "https://forms.praveenms.site/login.php?username=&password=" -m GET
```

## Disclaimer

This tool is intended for educational and testing purposes only. Unauthorized access to systems or networks without permission is illegal.

## License 

![](https://img.shields.io/badge/license-MIT-green)  <a href="https://choosealicense.com/licenses/mit/">MIT</a>

### Target Site: https://forms.praveenms.site/login.php

The above site is used to test the Brute force login
