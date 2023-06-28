# 배추마켓🥬


[배포 URL]

* URL: ----
 

## 프로젝트 소개

* 배추 마켓은 "<b>배</b>움의 <b>추</b>진력을 더하는 마켓"의 약자입니다.

* 전공서적, 교과서 등을 거래하고 스터디 그룹을 만들어 배움의 추진력을 더하기 위한 커뮤니티 플랫폼 입니다.

## 기술스택

<img src="https://img.shields.io/badge/html5-E34F26?style=for-the-badge&logo=html5&logoColor=white"> 
<img src="https://img.shields.io/badge/css-1572B6?style=for-the-badge&logo=css3&logoColor=white">
<img src="https://img.shields.io/badge/sass-CC6699?style=for-the-badge&logo=sass&logoColor=white"> 

맡은 주제 엔터이듬 왜 선택하게 되었는지

각자 맡은 파트 및 구성


## 팀원 소개 및 역할 분담

⭐ 이현주 <팀리더> - mixin, 메인페이지등 제작

🐰 김승연 - Q&A 페이지, 채팅 페이지 제작

🐰 신동혁 - 디자인, 게시판 페이지 제작

🐰 양정아 - 프로필, 프로필카드, 프로필 수정페이지 제작


## 파일 구조

```
📦 src
 ┣ 📂 images
 ┣ 📂 scss
 ┃ ┣ 📂 base
 ┃ ┣ 📂 components
 ┃ ┣ 📂 layout   
 ┃ ┣ 📂 pages 
 ┃ ┃ ┣ 📂 board
 ┃ ┃ ┣ 📂 mainpage
 ┃ ┃ ┣ 📂 profile
 ┃ ┃ ┣ 📂 qna
 ┃ ┃ ┣ 📜 _home.scss
 ┃ ┃ ┗ 📜 _index.scss
 ┃ ┣ 📂 themes
 ┃ ┣ 📂 utils                   
 ┣ 📂 style
 ┃ ┗ 📂 pages
 ┗📂 views
   ┣  📂 board
   ┣  📂 mainPage
   ┣  📂 profile
   ┗  📂 qna
```

각 인원 별로 `메인`, `게시판`, `Q&A`, `프로필` 을 나눠 진행하였다.

## 중요하게 생각한 부분
가독성


## 직면한 문제

### sprite

![image](https://github.com/hanchumon/cabbage-market/assets/74224516/e9740c65-9076-4900-9672-84cb3fac427c)

스프라이트 포지션의 틀어짐



* 기존 진행 방법

![3대지 1](https://github.com/hanchumon/cabbage-market/assets/74224516/3fa6b528-cb7b-4e71-a166-efab3d3f974d)

``` $sprites: Home, Board, Chat, Place, MyPage, Ppll;
  $x: 0;
  $y: 0;
  @each $sprite in $sprites {
    &#{$sprite} {
      background-position: $x $y;
    }
    $x: $x - 20px;
  }
  $sprites: FillHome, FillBoard, FillChat, FillMap, FillMyPage;
  $x: 0;
  $y: -20px;
  @each $sprite in $sprites {
    &#{$sprite} {
      background-position: $x $y;
    }
    $x: $x - 20px;
  ```
`Figma`에서 이미지를 가져 스프라이트 이미지를 제작하였지만, 코딩을 진행하다 보니 
빠진 이미지와 필요없는 이미지가 섞여서 계속되는 수정을 반복해야 했다.
그런 과정에 자주 파일을 주고 받다 보니 팀원들간의 코드 충돌과 스프라이트 이미지의 잘못된 구성이 골치거리였다.


* 수정 진행 방법

![3대지 1](https://github.com/hanchumon/cabbage-market/assets/74224516/2dbd944e-6f29-4eea-a40a-0ef05e8e17c2)

``` 
  // ----------20-------------
   &Message{@include whbp($size:rem(16px),$bpX:rem(-20px),$bpY:rem(-200px));}
   &Recommand{@include whbp($size:rem(16px),$bpX:rem(-40px),$bpY:rem(-200px));}
   &Comment{@include whbp($size:rem(16px),$bpX:rem(-60px),$bpY:rem(-200px));}
   &PlaceGray{@include whbp($size:rem(16px),$bpX:rem(-100px),$bpY:rem(-200px));}
   &PictureGray{@include whbp($size:rem(16px),$bpX:rem(-120px),$bpY:rem(-200px));}
   &MdHeart{@include whbp($size:rem(16px),$bpX:rem(-140px),$bpY:rem(-200px));}
   &Bell{@include whbp($size:rem(26px),$bpX:rem(-160px),$bpY:rem(-200px));}
```






## 느낀점

⭐ 이현주 - 프로젝트하면서 생각보다 부족한 점을 많이 깨달을수 있어서 좋았고, 하면서 조금씩 늘어가는 실력을 볼 수 있어서 보람찬 시간이었습니다. 팀원들과 하는 첫번째 프로젝트였는데 협업이라는게 생각보다 할수록 쉽지않고 번거롭지만 함께 완성해 나간다는게 정말 보람찼습니다.

🐰 김승연 - HTML 코드 리뷰를 받으면서 마크업 설계에 대한 공부가 부족하다는걸 많이 느꼈고, 다른 분들의 피드백을 받으면서 많이 공부가 되었다. sass를 사용하기로 했는데 개인적으로 sass가 너무 어렵다고 느껴져 혼자 css로 코드를 짜게 됐는데 이 점이 개인적으로도 실망스러웠고 아쉬웠다.


🐰 신동혁 - 기초 설계가 정말 중요하다고 몇번이고 느끼게 되었다. 
초반에 설계가 미흡하면 나중에 수정을 반복하게 되고 공동작업으로 이뤄지기 때문에 푸쉬 풀을 하며 충돌이 많이 발생하는 부분을 후회하게 되었다. 

🐰 양정아 - 프로젝트를 하면서 내가 얼마나 성장했나, 내가 뭘 배웠고 뭘 모르는지 알 수 있게 된 계기가 돼서 좋았고, 혼자가 아닌 팀원과 같이 만들어 보는 경험을 하게 돼서 좋았습니다.
