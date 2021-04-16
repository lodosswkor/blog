---
title: XCode info.plist
author: Harry JongSeok Lee
date: 2021-04-14 23:26
categories: [학습, SoftSquared]
tags: [숙제, 소프트스퀘어드, ios, 13기, 1주차]
pin: false
comments: true
---


## Information Property List 
***

번들(Bundle)을 식별하고, 설정하는 key-Value 으로 값이 포함된 리소스.    
Info.plist 라는 이름이로 저장되며, 파일명은 대소문자를 구분한다.   
그리고 저장위치는 번들의 타입이나 플랫폼에 따라 달라진다.   

> IOs App 번들의 경우에는 Root에 저장되며,   
>  MacOS App 번들의 경우엔 Contents 디렉터리 내에 저장된다.    

### A) Core Settings 
***

#### 1) Bundle Configuration 
번들의 설정 부분을 결정하며, 대표적으로 앱의 이름, 버전등이 있다. 

<table >
  <tr>
    <td>Type</td>
    <td>XCode Name</td>
    <td>Key</td>
    <td>Value</td>
    <td>Contents</td>
  </tr>
  <tr style="font-size:9pt;"> 
    <td rowspan="2" style="font-size:10pt;">Categorization</td>
    <td><a href="https://developer.apple.com/documentation/bundleresources/information_property_list/cfbundlepackagetype" target="_blank">Bundle OS Type code</a></td>
    <td>CFBundlePackageType</td>
    <td>String</td>
    <td>번들의 타입정보를 설정하며. 4개의 문자를 사용한다. Default는 <span style="">BNDL</span>(APP = APPL, Framework = FMWK, Bundles = BNDL) </td>
  </tr>
  <tr style="font-size:9pt;"> 
    <td><a href="https://developer.apple.com/documentation/bundleresources/information_property_list/lsapplicationcategorytype" target="_blank">Application Category</a></td>
    <td>LSApplicationCategoryType</td>
    <td>String</td>
    <td>앱스토어에서 사용할 카테고리를 설정한다.</td>
  </tr>
  <tr style="font-size:9pt;"> 
    <td style="font-size:10pt;" rowspan="3">Identification</td>
    <td><a href="https://developer.apple.com/documentation/bundleresources/information_property_list/cfbundleidentifier" target="_blank">Bundle identifier</a></td>
    <td>CFBundleIdentifier</td>
    <td>String</td>
    <td>유니크한 번들의 아이디를 정하며, Reverse DNS 타입으로 설정한다. (ex) io.ideatags.{appname} </td>
  </tr>
  <tr style="font-size:9pt;"> 
    <td>-</td>
    <td><a href="https://developer.apple.com/documentation/bundleresources/information_property_list/wkappbundleidentifier" target="_blank">WKAppBundleIdentifier</a></td>
    <td>String</td>
    <td>Watch OS 앱용 번들 아이디, WatchOS 앱을 생성하면 자동으로 생성,저장된다.</td>
  </tr>
  <tr style="font-size:9pt;"> 
    <td>-</td>
    <td><a href="https://developer.apple.com/documentation/bundleresources/information_property_list/wkcompanionappbundleidentifier" target="_blank">WKCompanionAppBundleIdentifier</a></td>
    <td>String</td>
    <td>Watch OS와 iOS app이 연동되어 있는 앱의 경우, 사용하며 CFBundleIdentifier와 동일하다.</td>
  </tr>
  <tr style="font-size:9pt;"> 
    <td style="font-size:10pt;" rowspan="3">Naming</td>
    <td><a href="https://developer.apple.com/documentation/bundleresources/information_property_list/cfbundlename" target="_blank">Bundle name</a></td>
    <td>CFBundleName</td>
    <td>String</td>
    <td>사용자에게 보여지는 번들(앱) 이름, 15자 이하의 짧은 이름이며 CFBundleDisplayName Key가 비어있다면, 이 Key의 값을 사용자에게 보여준다.</td>
  </tr>
  <tr style="font-size:9pt;"> 
    <td><a href="https://developer.apple.com/documentation/bundleresources/information_property_list/cfbundledisplayname" target="_blank">Bundle display name</a></td>
    <td>CFBundleDisplayName</td>
    <td>String</td>
    <td>CFBundleName보다 더 긴 이름을 사용할 수 있는 Key</td>
  </tr>
  <tr style="font-size:9pt;"> 
    <td><a href="https://developer.apple.com/documentation/bundleresources/information_property_list/cfbundlespokenname" target="_blank">Accessibility Bundle Name</a></td>
    <td>CFBundleSpokenName</td>
    <td>String</td>
    <td>text-in-speech용 번들(앱) 이름</td>
  </tr>
  <tr style="font-size:9pt;"> 
    <td style="font-size:10pt;" rowspan="4">Bundle Version</td>
    <td><a href="https://developer.apple.com/documentation/bundleresources/information_property_list/cfbundleversion" target="_blank">Bundle version</a></td>
    <td>CFBundleVersion</td>
    <td>String</td>
    <td>빌드된 번들들을 구분하기 위한 빌드번호. 한자리의 숫자, 혹은 3자리 까지의 .으로 구분된 숫자로 구성 (ex) 1.0.1 - Target/General에 Build 영역 </td>
  </tr>
  <tr style="font-size:9pt;"> 
    <td><a href="https://developer.apple.com/documentation/bundleresources/information_property_list/cfbundleshortversionstring" target="_blank">Bundle versions string (short)</a></td>
    <td>CFBundleShortVersionString</td>
    <td>String</td>
    <td>Target->Gerneral의 Version 영역, 앱스토어 등에 보여지는 버전을 3자리의 구분된 숫자들로 구성</td>
  </tr>
  <tr style="font-size:9pt;"> 
    <td><a href="https://developer.apple.com/documentation/bundleresources/information_property_list/cfbundleinfodictionaryversion" target="_blank">InfoDictionary version</a></td>
    <td>CFBundleInfoDictionaryVersion</td>
    <td>String</td>
    <td>Plist 버전정보, XCode에서 자동설정함 (변경금지)</td>
  </tr>
  <tr style="font-size:9pt;"> 
    <td><a href="https://developer.apple.com/documentation/bundleresources/information_property_list/nshumanreadablecopyright" target="_blank">Copyright (human-readable)</a></td>
    <td>NSHumanReadableCopyright</td>
    <td>String</td>
    <td>copyright 속성</td>
  </tr>
  <tr style="font-size:9pt;"> 
    <td style="font-size:10pt;" rowspan="4">Operating System Version</td>
    <td><a href="https://developer.apple.com/documentation/bundleresources/information_property_list/lsminimumsystemversion" target="_blank">Minimum system version</a></td>
    <td>LSMinimumSystemVersion</td>
    <td>String</td>
    <td>최소 지원 OS 버전</td>
  </tr>
  <tr style="font-size:9pt;"> 
    <td><a href="https://developer.apple.com/documentation/bundleresources/information_property_list/lsminimumsystemversionbyarchitecture" target="_blank">Minimum system versions, per-architecture</a></td>
    <td>LSMinimumSystemVersionByArchitecture</td>
    <td>String</td>
    <td>최소 지원 아키텍쳐 ex) i386, ppc, ppc64, x86_64 (MACOS) </td>
  </tr>
  <tr style="font-size:9pt;"> 
    <td>-</td>
    <td><a href="https://developer.apple.com/documentation/bundleresources/information_property_list/minimumosversion" target="_blank">MinimumOSVersion</a></td>
    <td>String</td>
    <td>최소 지원 OS 버전. General Setting pane의 Deployment Target을 사용함으로 Info.plist에서 지정하지 않는다.</td>
  </tr>
</table>
   

#### 2) User Interface



### B). Services 

### 참고 
[Property List: Information Property List](https://developer.apple.com/documentation/bundleresources/information_property_list)