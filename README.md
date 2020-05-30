## Linux 

***

Hello Linux!

***
<img src = "/images/linuxLogo.PNG" align = "center"> </img>

***

### 1. Linux VScode 설치
https://code.visualstudio.com/docs/setup/linux


<br>

#### 1-1) vscode install 1
<img src = "https://github.com/wallahan/linux/blob/master/images/vscodeinstall.PNG"></img><br>

<br>

#### 1-2) vscode install 2 
<img src = "https://github.com/wallahan/linux/blob/master/images/down.png"></img><br>

<img src = "https://github.com/wallahan/linux/blob/master/images/install.png"></img><br>

<br>

#### 2) vscode extension install 
- intellisense 자동완성 편의기능 등 <br>
<img src = "https://github.com/wallahan/linux/blob/master/images/extension.png"></img><br>


#### 3-1) 컴파일러1 :: gcc, g++ compiler intall
<pre>
<code>
sudo apt-get install build-essential
</codE>
</pre>

<br>

#### 3-2) 컴파일러2 :: VScode에 컴파일러 등록
<img src = "https://github.com/wallahan/linux/blob/master/images/gcc1.png"></img><br>
<img src = "https://github.com/wallahan/linux/blob/master/images/gcc2.png"></img><br>

<br>

#### 4) 빌드
<img src = "https://github.com/wallahan/linux/blob/master/images/build.png"></img><br>
<img src = "https://github.com/wallahan/linux/blob/master/images/exec.png"></img><br>

<br>

### 4-2) 빌드 :: 빌드용 bat 파일 만들기
* bat파일로 파일명을 인자로 받아서, 빌드와 실행까지 되는 bat파일을 만들었다.
<pre>
<code>
echo it is building....

gcc -c $1.c
gcc -o $1.exe $1.o
echo
echo it has finished the build.
echo
echo --------------------------
echo --------- exec -----------
echo --------------------------
echo
./$1.exe
</code>
</pre>

<br>

* 실행결과 <br>
<img src = "https://github.com/wallahan/linux/blob/master/images/bat0.png"></img><br>
<img src = "https://github.com/wallahan/linux/blob/master/images/bat1.png"></img><br>

#### 단축키 변경 :: 창닫기, 단어 블럭 선택 


***
END
