# ucms

Scope of influence

V1.6

Repair scheme

Store user account with session

Environment construction method

(1) : download from the official website and unzip it to the WWW directory, phpstudy, but the PHP version should be above 7.0

Vulnerability related code

function setadminname($value) {
	setcookie('admin_'.cookiehash, $value, time()+604800,null,null,null,true);
}

Vulnerability recurrence method

Payload

First step

Ordinary users only have these functions

![image](https://user-images.githubusercontent.com/27337983/139574084-51b50134-1e15-4747-8459-1804e058a2fe.png)

Step 2

Ordinary user access  /ucms/index.php?do=sadmin

Will appear

![image](https://user-images.githubusercontent.com/27337983/139574118-30674d61-7b3d-49b6-a5d5-aa6bbbc994f3.png)

Error error

Step 3

Change the get path to /ucms/index.php?do=sadmin

Modify the admin of the cookie_ Modify the 304a1a value to admin to access the column configuration upload shell


![image](https://user-images.githubusercontent.com/27337983/139574149-3cf6ea7f-3ae5-4d36-8afd-ab4fdae0b676.png)






