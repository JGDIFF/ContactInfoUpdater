## QLogin Documentation


### Introduction

One of the most crucial aspects to any tech company is security, and one of the easiest way that malicious hackers will find a way to infiltrate your web services is through your own employees, almost always without them knowing. QLogin is lightweight security application that is used to keep track of your employees to prevent cyberattacks before they happen. 

QLogin is a lightweight form application that runs entirely on the native C# framework with minimal dependencies.


### Prerequisites
Qlogin is desgined to be run on company machines that are running on a single dynamic network, however the program will still function on any personal machine, but you may not be able to use all of its features. 

You will need:
A computer
A working internet connection. 
A windows computer (No macOS support)

### Installation
In a sense, the installation process itself is the entire program, as Qlogin is an information collection tool, it should only be run upon registration, an important contact information update (i.e an employee moves or changes names) or once every 10 days just to confirm your already existing information.

Simply unpack the .exe and run the program, the first two screens you will be presented with are:

<img src="/1.PNG">
![First screen](/1.PNG)

<img src='/2.PNG'>
![Second screen](/2.PNG)

These two pages are there to let the user know exatcly what he/she is doing and to ensure the user knows that their information needs to be accurate and that their sensitive data is stored securely. 


Once you click on to the third page, the actual information collection begins, the breakdown is as follows:

3rd page, name information:
The user is asked to enter their first name, last name and their preferred nickname if they have one

4th page, job/position information: 
This page is where the user will enter their managers name, what department they work for etc.

5th page, contact information:
This page is where the user will enter their cell phone number and additional contact information

6th page, Geolocation information
This page is where the user will enter their zip cod and their interer provider information. While it may seem intrusive, the point of this information is to quickly be able to discern from genuine employee login attempts, if an employee lives in Oregon, but tries to send a login request from Mumbai, India. We can very easily deny this request with a simple api call to ``` getZip ``` from our API.

### Troubleshooting / Common Errors

Common Error #1:
```
FATAL ERROR: incorrect input format for field answer "FIELD", return invalid
```
This error means the user gave an incorrect type for a certain field, i.e the user entered characters into the phone number field, this is almost always caused by excess spaces at the end of user input and is an easy error to fix.

Common Error #2: 
```
FATAL ERROR: Could not connect to specified host server "ABUNCHOFDATA"
```
This error shows if the program cannot connect to host server, users will almost always have to contact their system administrator to solve this issue as it means that either the target server is down or the config was not setup properly. It should be noted that upon this error triggering, the current sessions information is stored locally on the users PC and the program will instantly halt execution as a privacy concern.

If a user has any concerns about their personal information being collected, they should take it up with their system administrator. 


### FAQ

Question: Is my information secure?

Answer: It is as secure as your system administator wants it to be, the qLogin program itself does very little and has no known security flaws, any system administator worth his salt will have your information secured nicely.

Question: Why does the program keep running? It hasn't been 10 days since it ran last.

Answer: This usually means you have incomplete information somewhere within the program, double check that you have answered every mandatory question.

Question: Will there be macOS support?

Answer: Never, qLogin is built on the C# framework which is exclusively for windows (It's the entire point of the language)



### Support or Contact

Feel free to create an issue if you see one :) 
