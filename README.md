Jellybean a cli tool for the [catbox api](https://catbox.moe/)  

written in [dysnomia](https://github.com/return5/Project-Dysnomia)  

named for my cat [Jellybean](#Jellybean)

## use
``jellybean [request] [flag(s)]``  

note: request must be first argument.  


## request
- df	
  - delete file(s) from catbox. 
    - accepted flags: [-h][-ih] -f  
- ra
	- remove file(s) from an album on catbox.
      - accepted flags: [-h] -s -f  
- ca
	- create album on catbox.
      - accepted flags: [-h] -t -d -f  
- da
	- delete an album on catbox.
      - accepted flags: [-h] -s  
- ea
	- edit album on catbox.
      - accepted flags: [-h] -s -t -d -f  
- uu
	- upload a file from url to catbox.
      - accepted flags: [-h][-ih] -f  
- fu
	- upload a file to catbox.
      - accepted flags: [-h][-ih] -f  
- h
	- print help message
- aa
	- add file(s) to album on catbox.
      - accepted flags: [-h] -s -f  

## flags
- s
  - short. the 6 alphanumeric character in the generated url for an album.  
- t
  - title
- f
  - file(s). list of file(s) to upload. with the uu request, -f is the list of url(s) to upload from.  
- ih
  - ignore hash.  ignores -h and also userhash field in Config.dys. can be set in Config.dys  
- h
  - userhash. can be provided as an argument or set in Config.dys  
- d
  - description  

## Config.dys  
   config file. set variables here as an alternative to passing in as commands.
- userhash  
  - the user hash  
- ignoreHash  
  - set to true to ignore the -h option and also to ignore userhash in Config.dys  

## examples
  - upload a single file anonymously   
  ```dysnomia jellybean -fu -ih -f myFile.jpg```  

  - upload two files to an account using  userhash   
   ```dysnomia jellybean.dys -fu -h myHash -f myFile1.jpg myFile2.jpg```  

  - create an album(assuming userhash in config)   
    ```dysnomia jellybean.dys -ca -t myAlbum -d a_photo_album -f 123.jpg 456.jpg 790.jpg```  


## Jellybean  
this is my cat Jellybean  
![jellybean](/picture/Jellybean.png)
