---
title: XCode Project,Target,Scheme
author: Harry JongSeok Lee
date: 2021-04-12 15:00:00 +0900
categories: [학습, SoftSquared]
tags: [숙제, 소프트스퀘어드, ios, 13기, 1주차]
pin: false
comments: true
---



## 1. Project    
***

![Project Window](/assets/post/20210412/project-window.png)   

Project는 하나 혹은 여러개의 소프트웨어를 만들기 위한 `모든 리소스를 관리하는 저장소:repository`를 
의미한다. 하나 이상의 Target을 가질 수 있으며, 프로젝트에 속해있는 Target(들)의 기본 빌드설정(Build Settings)을 
따로 정의할 수 있다. 

### a) Info    

Project의 기본정보(info)를 설정할 수 있는 창으로,   
Deployment Target, Configuration, Localizations 3개의 섹션으로 구분된다.      
<br/>

- __Deployment Target__ 

  iOS Deployment Target은 `지원하는 최소 버전` 을 의미한다.  

- __Configurations__

  빌드환경을 결정하는 곳으로, 기본 `Relese`, `Debug` 가 정의되어 있다.   
  빌드환경을 여러가지로 설정할 수 있으므로, 아래와 같이 환경에 맞는 config/info 를 적용 할 수 있다. 

- __Localizations__
  
  `지역화(다국어)설정` 부분, 다국어를 지원할 언어를 추가/삭제할 수 있다.   

<br/>  

### b) Build Settings   

`Build Settings` 는 Build시 적용되는 정보를 포함하는 **<u>상수 및 식에 대한 정의</u>** 라 할 수 있다.   
Project에 정의된 Build Settings 는 프로젝트에 포함된 모든 Target에 전파(상속)되지만,    
각 Target 에서 명시적으로 재정의(Overide)함으로써 Target Level Build Setting도 구성할 수 있다.

> ex) Debug/Build 구성   

<br/>

### c) Swift Packages 

`npm`,`maven`,`gradle`,`nuget` 같은 Project에 사용하는 Library 등에 대한 종속성(dependency)을 관리하는 
Swift Package Manager (이하 SPM) 관리 화면으로, 프로젝트의 Swift Package에 추가된 Library의 경우 하위 Target 들로 
자동 상속된다.   

> Package Manager 의 종류   
> 1) CocoaPods (3rd Party)  
> 2) Carthage (3rd Party)  
> 3) Swift Package Manager (Apple)    

<br/> 
## 2. Target
*** 

Target은 하나의 Product를 의미하며, 하나의 Product는 App이 될 수도 있고 Library가 될 수도 있다.   
Project에는 하나 이상의 Target이 포함될 수 있으며, 하나의 target은 각각 하나의 Product를 생성한다.  



<br/> 
## 참고 
***   
- [Xcode Concept](https://developer.apple.com/library/archive/featuredarticles/XcodeConcepts/Concept-Targets.html)
- [Xcode Target, Project, Workspace, Scheme 그리고 Build Setting](https://zeddios.tistory.com/706)   
- [Framework Part 1 : Static Framework 와 Dynamic Framework](http://minsone.github.io/ios/mac/ios-framework-part-1-static-framework-dynamic-framework)  
- [CocoaPods vs Carthage vs Swift Package Manager](https://onelife2live.tistory.com/39) 
- [[Swift 5.2] Swift Package Manager를 이용하여 패키지를 통합 관리하기 - Proxy Module](http://minsone.github.io/ios/mac/swift-package-manager-proxy-modular)
- [Localizing the information Property List Files](https://developer.apple.com/library/archive/documentation/MacOSX/Conceptual/BPInternational/LocalizingYourApp/LocalizingYourApp.html)
