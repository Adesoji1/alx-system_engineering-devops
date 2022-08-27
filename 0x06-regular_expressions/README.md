# 0x06 Regular expression

## Background Context
For this project, you have to build your regular expression using Oniguruma, a regular expression library that which is used by Ruby by default. Note that other regular expression libraries sometimes have different properties.

Because the focus of this exercise is to play with regular expressions (regex), here is the Ruby code that you should use, just replace the regexp part, meaning the code in between the //:

	sylvain@ubuntu$ cat example.rb
	#!/usr/bin/env ruby
	puts ARGV[0].scan(/127.0.0.[0-9]/).join
	sylvain@ubuntu$
	sylvain@ubuntu$ ./example.rb 127.0.0.2
	127.0.0.2
	sylvain@ubuntu$ ./example.rb 127.0.0.1
	127.0.0.1
	sylvain@ubuntu$ ./example.rb 127.0.0.a



## Requirements
### General
* Allowed editors: vi, vim, emacs
* All your files will be interpreted on Ubuntu 20.04 LTS
* All your files should end with a new line
* A README.md file, at the root of the folder of the project, is mandatory
* All your Bash script files must be executable
* The first line of all your Bash scripts should be exactly #!/usr/bin/env ruby
* All your regex must be built for the Oniguruma library

### 0. Simply matching School

<img width="969" alt="ec65557f0da1fbfbff6659413885e4d4822f5b1d" src="https://user-images.githubusercontent.com/36323983/186537818-5058d0ec-680d-43c7-bde1-c7d95b03d22a.png">

### 1. Repetition Token #0

<img width="959" alt="e7db3c377d46453588fc84f3a975661d142fee91" src="https://user-images.githubusercontent.com/36323983/186537911-4150bbbf-6661-4772-87bc-c3e38df1510e.png">


### 2. Repetition Token #1

<img width="967" alt="c59ff11db195d5cf17d1790a5141ae2f234786d2" src="https://user-images.githubusercontent.com/36323983/186537979-2cc0bc8b-e9fd-4d9a-9175-247bb26a940f.png">


### 3. Repetition Token #2

<img width="974" alt="3b6bf4aeca6a0c2de584e7f5d68d11eef57ce205" src="https://user-images.githubusercontent.com/36323983/186538022-38fd2e8f-6c7b-4fb1-b815-b701feb01685.png">


### 4. Repetition Token #3

<img width="956" alt="f8dbcb9cf5ae569a8645027dc46e81cb372ce28e" src="https://user-images.githubusercontent.com/36323983/186538059-001ca8d6-fe51-4e23-b975-1ad9336f810b.png">


### 5. Not quite HBTN yet

	sylvain@ubuntu$ ./5-beginning_and_end.rb 'hn' | cat -e
	$
	sylvain@ubuntu$ ./5-beginning_and_end.rb 'hbn' | cat -e
	hbn$
	sylvain@ubuntu$ ./5-beginning_and_end.rb 'hbtn' | cat -e
	$
	sylvain@ubuntu$ ./5-beginning_and_end.rb 'h8n' | cat -e
	h8n$
	sylvain@ubuntu$
	$
	
### 6. Call me maybe
Requirement:
* The regular expression must match a 10 digit phone number

		sylvain@ubuntu$ ./6-phone_number.rb 4155049898 | cat -e
		4155049898$
		sylvain@ubuntu$ ./6-phone_number.rb " 4155049898" | cat -e
		$
		sylvain@ubuntu$ ./6-phone_number.rb "415 504 9898" | cat -e
		$
		sylvain@ubuntu$ ./6-phone_number.rb "415-504-9898" | cat -e
		$
		sylvain@ubuntu$

### 7. OMG WHY ARE YOU SHOUTING?

![shouting](https://user-images.githubusercontent.com/36323983/186538549-6bd6f5e3-4100-42d4-bf48-5427884ae17b.jpg)

Requirement:
* The regular expression must be only matching: capital letters

		sylvain@ubuntu$ ./7-OMG_WHY_ARE_YOU_SHOUTING.rb "I realLy hOpe VancouvEr posseSs Yummy Soft vAnilla Dupper Mint Ice Nutella cream" | cat -e
		ILOVESYSADMIN$
		sylvain@ubuntu$ ./7-OMG_WHY_ARE_YOU_SHOUTING.rb "WHAT do you SAY?" | cat -e
		WHATSAY$
		sylvain@ubuntu$ ./7-OMG_WHY_ARE_YOU_SHOUTING.rb "cannot read you" | cat -e
		$
		sylvain@ubuntu$
