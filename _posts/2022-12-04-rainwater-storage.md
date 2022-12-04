---
title: 아두이노를 이용한 빗물 저장 장치
author: Kim Geonwoo
date: 2022-12-04 2:30:00 +0900
categories: [Exhibition,2022년]
tags: [post,kimgeonwoo]     # TAG names should always be lowercase, 띄어쓰기도 금지 
---

------------------------------------------
# 아두이노를 이용한 빗물 저장 장치

## 작품 제작 동기
고등학교 시절 환경 관련 동아리, 캠페인에 참여하면서 자연스럽게 환경 분야에 관심을 가지게 되었고 그 중 수업 시간에 배운 친환경 하우스에 관심을 가지게 되었습니다. 친환경 하우스란 친환경 에너지로 발전을 하거나 빗물을 재사용하는 등 방법으로 환경오염을 줄인 주택을 말합니다. 해외의 경우 독일의 프라이부르크나 영국의 베드제드와 같이 친환경 하우스가 도입된 도시들까지 있는 반면에, 우리나라의 경우 이제야 태양전지가 보급되는 수준입니다. 그래서 친환경 하우스 기술 중 하나인 빗물 저장 장치를 만들어서 친환경 하우스에 대한 긍정적인 인식을 심어주고자 하였습니다.

-----

## 작품 구조 및 알고리즘
작품은 아두이노 파트와 앱인벤터 파트로 나누어져 있습니다. 외관은 우드락으로 제작하였습니다.
<img src="/assets/img/post/2022-12-04-rainwater-storage/final2.jpg" width="80%">
<img src="/assets/img/post/2022-12-04-rainwater-storage/final1.jpg" width="80%">

### 아두이노 파트
두 개의 수위센서를 빗물이 저장되는 플라스틱 용기에 부착하고 두 수위 센서의 측정값의 평균값을 수위 측정에 이용했습니다. L298N 모터드라이브로 두 개의 수중펌프를 제어하였고 외부전력으로 9V 전지를 연결하였습니다. 블루투스 모듈을 연결해서 휴대폰과 블루투스 통신이 가능하게 했습니다. 물을 보낼 위치를 휴대폰으로부터 전달받으면 설정된 위치에 해당하는 모터를 작동시킵니다.
<img src="/assets/img/post/2022-12-04-rainwater-storage/arduino.jpg" width="80%">

### 앱인벤터 파트
구글 앱인벤터를 이용해서 안드로이드 어플을 만들었습니다. 블루투스 연결과 해제가 가능하며 새로고침 버튼을 통해서 아두이노로부터 수위 센서의 값을 불러올 수 있습니다. 불러온 센서값을 자체 함수로 계산하여 mL 용량으로 변환하고 이를 휴대폰 화면에서 확인할 수 있게 하였습니다. 여기서 함수는 50ml 간격으로 물을 붓고 측정된 센서값과 실제 mL 사이의 관계를 1차 함수로 만든 것입니다. 물을 보낼 위치를 리스트에서 선택할 수 있으며 선택된 위치는 화면에 보여지게 됩니다. 전송 버튼은 설정된 물을 보낼 위치를 아두이노에게 전달합니다.  
<img src="/assets/img/post/2022-12-04-rainwater-storage/appinventor.jpg" width="80%">

-----

## 결론 및 기대효과
빗물이 저장된 후 사용되기까지 과정을 휴대폰을 통해 확인할 수 있기 때문에 편리하게 사용할 수 있습니다. 이를 통해서 빗물 저장 장치가 어떤 식으로 도입될 수 있는지에 대한 가능성을 확인할 수 있었습니다. 그러나 빗물 저장 장치로서 여과 등의 현실적인 문제를 담지 못하였다는 점이 아쉬운 점입니다. 물을 보내는 양을 조절할 수 있게 하거나 날씨에 따라 작동 여부를 결정할 수 있다면 더욱 효과적일 것입니다. 개인적으로는 아두이노와 다양한 소자들을 사용해보고 앱인벤터를 다뤄보는 좋은 경험이 되었습니다.