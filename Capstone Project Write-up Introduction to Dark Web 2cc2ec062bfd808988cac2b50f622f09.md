# Capstone Project Write-up : Introduction to Dark Web Operations (Security Blue Team)

![image.png](Capstone%20Project%20Write-up%20Introduction%20to%20Dark%20Web/image.png)

I did not really know much about the important of Dark Web Operations in Defensive Security when choosing for the SOC role, but after going through the course I learnt something new needed in the Defensive area; the Dark Web usage. The Dark Web is not as illegal as they say it is, depends on how you utilize it. Through this course, I learnt both the good and bad usage of the Dark Web. Thanks to this part of the SBT-**CERTIFIED JUNIOR DETECTION ENGINEER.**

## Introduction

After a successful completion of the course, I was introduced to how the “three part of the Internet” **Clear Web, Deep Web** and **Dark Web,**  are being used for a particular purpose and the type of information needed from each part. The skills and search showcased here are the same of how law enforcement  officers infiltrate **Dark Web** to collect evidence that would be used in the case of legal prosecution against individuals involved in illegal activity.

![image.png](Capstone%20Project%20Write-up%20Introduction%20to%20Dark%20Web/image%201.png)

## Challenge Scenario

Last month, our efforts led to the successful dismantling of a major drug trafficking network operating within the UK through the TOR network. The network's primary marketplace was taken down, significantly disrupting their operations and preventing further illicit substances from reaching our streets. However, critical intelligence suggests that one of the masterminds behind this network evaded capture and continued their illegal activities. They have established a platform to "tell their stories" of criminal exploits, serving as a covert hub for their operations. Your mission is to bring this individual to justice. This will not be easy, but we are confident in your expertise and ability to achieve this mission. Your success is pivotal to dismantling this criminal enterprise and safeguarding the public.

**1] Gain Access to the Site:** *(Visit the URL below. Right-click and select “Inspect Element” when presented with a login screen. Select the ‘Console’ tab and enter the command: generateUserCredentials(). Decode the answer, and you’re good to go!)*

**2] Find evidence that the individual(s) is involved in drug trafficking**

**3] Find any information about the locations in which these criminals congregate.**

**4] Site:** http://panznjcktrpezyln5frnjxf5gv4xoyi7wvd3ykeu6bejxvbynhfpasqd.onion

## Challenge Walk-through

![image.png](Capstone%20Project%20Write-up%20Introduction%20to%20Dark%20Web/image%202.png)

**Gain Access to the Site:** *(Visit the URL below. Right-click and select “Inspect Element” when presented with a login screen. Select the ‘Console’ tab and enter the command: generateUserCredentials(). Decode the answer, and you’re good to go!)*

First I was given a login page with no username and password.

![image.png](Capstone%20Project%20Write-up%20Introduction%20to%20Dark%20Web/image%203.png)

To get the username and password, I need to check the **Inspect tab** as said in the hint above.

Following that, I was able to get the credentials but it was encoded in base64

**S0Y3eWJ1RDE6QWx5aGZvdDBWOVZJV202Vw==** 

which needs to be decoded back to plaintext.

![image.png](Capstone%20Project%20Write-up%20Introduction%20to%20Dark%20Web/image%204.png)

Upon a successful decoding from base64, using the **CyberChef** tool, I was presented with the username and password.

**KF7ybuD1:Alyhfot0V9VIWm6W**

![image.png](Capstone%20Project%20Write-up%20Introduction%20to%20Dark%20Web/image%205.png)

**Then a successful login using the credentials we had…**

**username - KF7ybuD1**

**password - Alyhfot0V9VIWm6W**

![image.png](Capstone%20Project%20Write-up%20Introduction%20to%20Dark%20Web/image%206.png)

The dashboard for the marketplace site.

I was presented with **hexadecimal code** which can help in solving the puzzle. So decoding it will help in this stage.

![image.png](Capstone%20Project%20Write-up%20Introduction%20to%20Dark%20Web/image%207.png)

Again, using the **CyberChef** tool to decode the hexadecimal codes.

**44 72 75 67 73 - Drugs**

57 65 20 68 61 76 65 20 50 65 72 63 6F 63 65 74 2C 20 43 6F 64 65 69 6E 65 2C 20 61 6E 64 20 59 65 72 63 73 21 - **We have Percocet, Codeine, and Yercs!**

**50 6C 65 61 73 75 72 65 - Pleasure**

45 6E 6A 6F 79 20 79 6F 75 72 20 76 69 63 65 73 20 77 69 74 68 20 73 65 72 76 61 6E 74 73 20 61 74 20 79 6F 75 72 20 64 69 73 70 6F 73 61 6C - **Enjoy your vices with servants at your disposal**

**44 72 6F 70 73 - Drops**

53 65 65 20 79 6F 75 72 20 64 65 6D 6F 6E 73 20 77 69 74 68 20 74 68 65 73 65 20 67 61 6C 61 78 79 20 65 79 65 2D 64 72 6F 70 73 - **See your demons with these galaxy eye-drops**

> **NOTE: following the challenge request can help you tackle what is needed.**
> 

![image.png](Capstone%20Project%20Write-up%20Introduction%20to%20Dark%20Web/image%208.png)

Now, scrolling through the page, at the **Messages** board, I came across a link which then lead me to another page, the hacking group they operate in.

![image.png](Capstone%20Project%20Write-up%20Introduction%20to%20Dark%20Web/image%209.png)

Being part of the challenge, I was able to find the illegal site which is the **Hacker Group**  name, **Midnite.**

![image.png](Capstone%20Project%20Write-up%20Introduction%20to%20Dark%20Web/image%2010.png)

Again, looking through the **Recent Transactions** board, an amount of money was presented in a link form.

What can it provide…? Let’s check.

![image.png](Capstone%20Project%20Write-up%20Introduction%20to%20Dark%20Web/image%2011.png)

 A transaction log visible under the “**Recent Transactions**” section. Provided me with the customer’s full name, email address, and the purpose of the transaction and more, a very useful information.

![image.png](Capstone%20Project%20Write-up%20Introduction%20to%20Dark%20Web/image%2012.png)

Under the car part board, we can find a text saying:

**Contact me at …….. if you are serious.** 

The most valuable information needed for the contacting has been encoded again in hexadecimal format which needs to be decoded to provide the real contact details.

![image.png](Capstone%20Project%20Write-up%20Introduction%20to%20Dark%20Web/image%2013.png)

And again, **CyberChef** for decoding the hexadecimal code.

74 77 69 7A 7A 65 72 69 63 68 61 72 64 40 67 6D 61 69 6C 2E 63 6F 6D - [**twizzerichard@gmail.com**](mailto:twizzerichard@gmail.com)

After, the hexadecimal was an email of the user.

## Challenge Solves.

1. What command is used in the Console to generate valid credentials? Provide the credentials, too.

**generateUserCredentials(), KF7ybuD1, Alyhfot0V9VIWm6W**

2. After logging in, what are the titles of the three pinned posts seen on the website in ASCII text? Please place them in respective order.

**Drugs, Pleasure, Drops**

3. Look at the Messages board. They are mentioning another illegal site. Provide its name.

**Midnite**

4. A transaction log is mistakenly visible under the “Recent Transactions” section. Provide the customer’s full name, email address, and the purpose of the transaction.

**Frank Castle, [frankcastle2093@gmail.com](mailto:frankcastle2093@gmail.com), Hookers and Drugs**

5. It looks like the user PJ is hosting an illegal party. What city is this taking place and when? We could catch him there and shut down this entire operation.

**Cardiff, February 14, 2025**

6. What is the email of the user selling ‘stolen’ car parts?

[**twizzerichard@gmail.com**](mailto:twizzerichard@gmail.com)

## Conclusion

Realizing the importance of Dark Web Operations in Defensive (SOC) Security helps to find more information about an organization and to identify malicious activities that adversaries use for their attacks. It helps to collect intelligence about individuals or groups, tracking them of their illegal activities and crime-commits.  Understanding the Dark Web Operations helps prevent further illicit substances from reaching our streets. 

## Thank You.