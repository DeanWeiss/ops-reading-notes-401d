Dean Weiss
22 November 2022

# What is a Burp Suite?

It is a suite of tools from PortSwigger that help penetration testing of web applications on HTTP and HTTPS. It can intercept web requests and edit them in real time. 

- Intruder allows you to import a request and then configure arrange of payloads to attempt and can then run through them automatically. 
- Repeater allows you to import a web request and then make manual modifications to it and see the response side by side allowing you to make minor adjustments to attempted exploits and easily see if it’s working. A dashboard feature shows a list of identified issues, although these need to be manually checked for false positives.
- Sequencer is designed to analyse the randomness of data such as session IDs, CSRF tokens, and password reset tokens. 
- The analysis requires more than 100 samples but can identify weaknesses in how supposedly random values are being generated. 
- Decoder allows you to decode strings from a range of encoding standards as well as allowing you to encode data again. 
- Comparer allows you to compare two strings to check for minor differences.


source: https://www.technipages.com/what-is-burp-suite
