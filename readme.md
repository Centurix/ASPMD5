## ASPDump ##

Version 1.0.1 documentation (Monday the 14th April, 2003)

This is a VBScript implementation of the RSA's MD5 algorithm. This script will take a text string of arbitrary length and calculate an MD5 hash from it. Very useful o encrypt things like passwords in databases or transferring over the wire.

How does it work?
The MD5 algorithm is documented in RFC 1321. The algorithm uses module math to calculate a 'one-way' hash from a set of data.

Requirements
You will require a web server that supports ASP, with version 5.0 or higher of the VBScript library.

Installation instructions
Copy class_md5.asp onto your IIS server, make sure the folder it sits in has the correct rights to run ASP scripts (check the IIS management console to make sure), and then include the file into your ASP project using a server side include.

Usage

To use the class, you need to create an instance 
of the MD5 object, feed it some text and retrieve the hash:
```
Dim objMD5
Set objMD5 = New MD5
objMD5.Text = "This is test text"
Response.Write objMD5.HEXMD5 ' This will display an MD5 hash
```
