Executable Tamper-Protection: CRC32 Checksum Validation
by Detonate (detonate@start.com.au)

CRC32 code by Neo (http://vbcode.8m.com/)
His original CRC32 code can be found at http://www.planet-source-code.com/vb/scripts/ShowCode.asp?lngWId=1&txtCodeId=4822
The CRC32 routines of his are very high speed and this is an excellent algorithm to use for this program

How it works:
Simply add CRC32.BAS module to your VB project, and activate it at the start of your program like this:
 If IntegrityOK <> 1 Then Msgbox "CRC32 checksum failed"
You must run the APPLYCRC32 program over your exe before you run it. APPLYCRC32 reads the file, calculates
a checksum, and appends the checksum to the end of the exe file. When youre exe file calls IntegrityOK(),
it reads the last 8 bytes of its own file, and if the two checksums match, then you know your file hasn't
been tampered with.

CRC32 is a very effective (and fast) checksum calculation, and this is a great way of preventing crackers
from at least writing software patches (those little programs which change a few bytes in order to do
things the programmers didnt want them to do :-)   CRC32 is not as "bullet-proof" as MD5, but it is 
VERY effective, and probably perfect for everyone at planetsourcecode.com's needs. Enjoy! :-)  

FOLDERS:
\applycrc\	- The program to read the contents of your project.exe file, calculate its crc32 checksum,
		  and append the checksum to the end of the project.exe file
\program\	- Skeleton program that calls the CRC32 check to make sure its own file hasnt been tampered with

PLEASE VOTE FOR THIS CODE! :-)
- Detonate  (detonate@start.com.au)
