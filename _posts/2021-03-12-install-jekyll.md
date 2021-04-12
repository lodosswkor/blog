---
title: Jekyll + Github + Fork 블로그 만들기 
author: Harry JongSeok Lee
date: 2021-03-12 15:00:00 +0900
categories: [Tutorial]
tags: [jekyll, blog]
pin: false
comments: true
---

## Prerequisites 

Jekyll + Github 블로그 만들기는 아래의 순서대로 진행됩니다. 
  
  - 설치 (윈도우 위주)  
  - 테마선택/설정 
  - Post 작성 
  - github page 사이트
  - etcs.

## Installation 

   Jekyll은 Ruby를 사용함으로, 윈도우용 *`Ruby`, `Gem`, `Bundler`* 를 설치합니다. 또한 gem package manager는 git을 통해서 정보를 받기 때문에,  **윈도우용 gitscm**을 설치해야 합니다. 

   [Jekyll 설치문서 (en)](https://jekyllrb.com/docs/installation/)   
   [Jekyll 설치문서 (ko)](http://jekyllrb-ko.github.io/docs/installation/)  
   [GIT SCM 사이트](https://git-scm.com/download/win)

### - install Ruby+devkit

   설치문서에 따라, [Ruby+Devkit](https://rubyinstaller.org/downloads/) 에서 **Ruby+Devkit 2.7.2-1 (x64)** 을 다운받아 설치합니다. 
   
   <span style="color:red">!) 설치 시 **ridk install** 을 반드시 선택하셔야 합니다. </span>  

   ![Ruby+Devkit Install1](/assets/post/install.PNG)
   
   **ridk install** 설치화면.   

   ![Ruby+Devkit Install2](/assets/post/install2.PNG)

   설치가 완료되면 시작 -> cmd 창을 여시고, 아래와 같이 명령어를 칩니다.

   ```console
   ruby --version 
   ```

   오류가 안나면 **Ruby+Devkit**이 정상 설치된 것입니다.   
 
   
### - Jekyll, Bundler 설치 
   
   Jekyll 설치문서에 따라, **Jekyll, Bundler**를 설치합니다.   
   [Jekyll 설치문서 (ko)](http://jekyllrb-ko.github.io/docs/installation/)
   
   ```console
   bundle install jekyll, Bundler
   ```

   설치가 완료되면 아래 명령어를 쳐보세용 ^^;   

   ```console
   jekyll -v 
   ```  
   
   자 이제 Jekyll 을 사용할 준비가 되었습니다!!.
    
## 테마선택/설정  



자기가 원하는 Jekyll 디자인을 선택할 수 있습니다  

[jekyllthemes.org](http://jekyllthemes.org/)

설명은 **Chripy Theme** 로 진행합니다.  

[chrispy theme](http://jekyllthemes.org/themes/jekyll-theme-chirpy/)  
[chrispy theme/demo](https://chirpy.cotes.info/)   


## Post 작성 

## github page 만들기


## Etcs. 

favicon 생성 사이트 :(http://jekyllthemes.org/themes/jekyll-theme-chirpy/)   

### - 마크다운 문법 
   
[https://guides.github.com/features/mastering-markdown/](https://guides.github.com/features/mastering-markdown/)   
[https://gist.github.com/ihoneymon/652be052a0727ad59601](https://gist.github.com/ihoneymon/652be052a0727ad59601)   
[https://post.naver.com/viewer/postView.nhn?volumeNo=24627214&memberNo=42458017](https://post.naver.com/viewer/postView.nhn?volumeNo=24627214&memberNo=42458017)     
[https://shields.io/](https://shields.io/)  







