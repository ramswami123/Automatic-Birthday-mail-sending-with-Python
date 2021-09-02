# Automatic-Birthday-mail-sending-with-Python
Apart from this, Also create an Excel sheet for containing records like this: Name, Email, Contact, Birthday, and Year.   Approach:  For the sending email part, We define a sendEmail() function which will start a Gmail session, send the email, and quit the session.  For the SMS part, we must have an account on www.fast2sms.com from where we will get an API key. This API key is used to send SMS over mobile numbers using your account on fast2sms then We create a sendsms() function which will verify the API key and send SMS. In the driver code section, we read the data from Excel sheet and match today’s date with any of the birthdays. If there is a match, we call the sendEmail() and sendsms() functions and also we add the current year in the Excel sheet. Also, we have used ToastNotifier from win10toast library to show desktop notifications once the e-mail and SMS has been sent successfully
Pandas is an open-source library that is built on top of NumPy library. It is a Python package that offers various data structures and operations for manipulating numerical data and time series. It is mainly popular for importing and analyzing data much easier. Pandas is fast and it has high-performance & productivity for users.
In Python, date and time are not a data type of its own, but a module named datetime can be imported to work with the date as well as time. Datetime module comes built into Python, so there is no need to install it externally. 


Steps to send mail from Gmail account:

First of all, “smtplib” library needs to be imported.
After that, to create a session, we will be using its instance SMTP to encapsulate an SMTP connection.
s = smtplib.SMTP('smtp.gmail.com', 587)
In this, you need to pass the first parameter of the server location and the second parameter of the port to use. For Gmail, we use port number 587.

For security reasons, now put the SMTP connection in the TLS mode. TLS (Transport Layer Security) encrypts all the SMTP commands. After that, for security and authentication, you need to pass your Gmail account credentials in the login instance.The compiler will show an authentication error if you enter invalid email id or password.
Store the message you need to send in a variable say, message. Using the sendmail() instance, send your message. sendmail() uses three parameters: sender_email_id, receiver_email_id and message_to_be_sent. The parameters need to be in the same sequence.
This will send the email from your account. After you have completed your task, terminate the SMTP session by using quit().

resources:geek for geeks(documentation)
          python.org

          
