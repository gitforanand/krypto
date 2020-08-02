# Krypto
To upload to S3 using Customer Managed Key S3 Client Side Encryption using CMK.

# Requirement

1. AWS CLI with necessary config and credentials updated
2. Permission to upload into the specified bucket
3. JDK 1.5 and above

# How to execute

java -jar krypto.jar -h
-----------------------------------------------------------------
Encrypting and placing files on S3 with customer managed keys...

ErrorMissing required options: i, e, k, r, b

usage: java -jar krypto.jar -e [ "AES | DES | HmacSHA1 | HmacSHA256" ]

            -i [ " /tmp/file.txt | c:\temp\file.txt" ]

            -k [ "ANY-STRING-OF-CHARS" ]

            -r [ "us-east-1" ]

 -b,--bucket <arg>       Bucket Name
 -e,--encryption <arg>   Encryption type
 -h,--help               Bucket Name
 -i,--input <arg>        File to be encrypted with path
 -k,--key <arg>          Encryption Key
 -r,--region <arg>       AWS Region

-----------------------------------------------------------------
# Encryption key -k
The log displays a base-64 encoded key & default key is "Encrypt"
# Sample Output

-----------------------------------------------------------------
Encrypting and placing files on S3 with customer managed keys...
FileName           : text.txt
Input              : /Users/demo/Documents/projects/JAVA/text.txt
EncryptionType     : AES128
InputEncryptionKey : QURCQ0VER0g=
AWS Region         : US_EAST_1
MyRegion           : us-east-1

Files uploaded successfully without wrapping key
-----------------------------------------------------------------

# Terms
This program is open to use and I do not gurantee for any loss or damages occured. I have tested the same and did not incur any loss.


