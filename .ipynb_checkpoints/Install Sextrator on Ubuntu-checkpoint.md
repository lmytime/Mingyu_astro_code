## Notes: Install Sextrator on Ubuntu

---
### To say
When installing for the first time, I tried to install using the tar.gz source code, but encountered many problems, including FFTW3 problems. After that, I used the rpm package on the advice of Dongdong senior and successfully installed it. The rpm package must be converted to a deb package on ubuntu before installation.


### Website
---
The official website is
    www.astromatic.net/software/sextractor

 ### Installation Process
 ---
 First need to install `alien`, the role is to convert the` rpm` package to a `deb` package.

    sudo apt install alien 
     
Download the rpm package of sextrator.

    sudo wget https://www.astromatic.net/download/sextractor/sextractor-2.19.5-1.x86_64.rpm
    
After that we perform format conversion.

    sudo alien sextractor-2.19.5.x86_64.rpm
    
Note that when format conversion is performed, there must not be a folder named `sextractor-2.19.5` in this folder.
Then install it with the converted `deb` package.

    sudo dpkg -i sextractor_2.19.5-1_amd64.deb
    
Note that the specific file names may be different.


## Have an issue 

Have to reinstall before using sometimes.