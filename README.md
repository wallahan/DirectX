## Linux 

***

Hello Linux!

***
<img src = "/images/linuxLogo.PNG" align = "center"> </img>

***

### 1. Linux VScode 설치
https://code.visualstudio.com/docs/setup/linux <br>
<img src = "https://github.com/wallahan/linux/blob/master/images/vscodelogo.png"></img><br>

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

<br>

#### 3-1) 컴파일러1 :: gcc, g++ compiler intall
<pre>
<code>
sudo apt-get install build-essential
</code>
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

* 한줄로 빌드하기
<pre>
<code>
gcc 코드파일명.c -g -o ./경로/실행파일명.exe
gcc main.c -g -o ./main.exe
</code>
</pre>

<br>

* 실행결과 <br>
<img src = "https://github.com/wallahan/linux/blob/master/images/bat0.png"></img><br>
<img src = "https://github.com/wallahan/linux/blob/master/images/bat1.png"></img><br>

<br>

#### 4-3) VScode Task를 이용해 build 하기 ( bat파일 없이 )

* tasks.json 파일을 연다. <br>
<img src = "https://github.com/wallahan/linux/blob/master/images/tasksfile.png"></img><br>

<br>

* tasks 객체안에 {} 객체로 커맨드 실행을 만들수 있다. <br>
<img src = "https://github.com/wallahan/linux/blob/master/images/taskObject.png"></img><br>

<br>

* 나만의 task를 만들어보자 ( 최대한 간단하게 구성했다 )
   + ${file} : 파일명.확자자명 ( 현재 vscode에 포커싱된 )
   + ${fileBasenameNoExtension} : 파일명만 ( 현재 vscode에 포커싱된 )  <br>
 <img src = "https://github.com/wallahan/linux/blob/master/images/mytask.png"></img><br>
  

* 빌드후 바로 실행되게 만들어보자 ( 한줄에 여러 명령어 && )
   + && : 앞 커맨드 명령이 성공하면, 이 뒤에 오는 명령어를 실행한다
<img src = "https://github.com/wallahan/linux/blob/master/images/buildandexec.png"></img><br>

<br>

#### 5-1) 내가 만든 my task 실행해보기 
<img src = "https://github.com/wallahan/linux/blob/master/images/mytaskexec1.png"></img><br>
<img src = "https://github.com/wallahan/linux/blob/master/images/mytaskexec2.png"></img><br>
<img src = "https://github.com/wallahan/linux/blob/master/images/mytaskexec3.png"></img><br>

<br>

#### 5-2) 내가 만든 my task , 빌드 단축키를 새로 지정해 실행 해보기
* 빌드와 실행 단축키 : 새로 등록 F9로 등록해보자 
   + File > Preference > Keyboard Shortcut 
   + 우측상단 아이콘 클릭 <br>
   <img src = "https://github.com/wallahan/linux/blob/master/images/keyicon.png"></img><br>
   + 이 경로에 있는 키바인딩.json파일이 열리게 된다 <br>
   <img src = "https://github.com/wallahan/linux/blob/master/images/keypath.PNG"></img><br>
   + keybindings.json에 바인딩할 명령어를 작성한다.<br> 
   ( my c builder를 바로 링크하진못한다, 정확한건 아래설명 )
   <img src = "https://github.com/wallahan/linux/blob/master/images/keybind.PNG"></img><br>
   
* 어떻게 build 단축키를 실행했는데, 내가 만든 my c builder가 뜨는걸까?
   + task 변수중 group.kind값을 build로 지정하면 workbench.action.tasks.build 실행시 뜨게된다
<img src = "https://github.com/wallahan/linux/blob/master/images/addbuild.png"></img><br>

<br>

#### 단축키 변경 :: 창닫기, 단어 블럭 선택 


***
END
