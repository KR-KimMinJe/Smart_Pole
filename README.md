# Ⅰ. **개요**
*   개발 기간 : 2019.12.03 ~ 2019.12.04
*   개발 목적 : 
*   대한전기학회 워크샵. 129-130
*   상명 Prime 성과우수대회 최우수상

# Ⅱ. **동작 구성도**
<img src="https://user-images.githubusercontent.com/73852272/98265582-9778d500-1fcc-11eb-98c6-f5327c863156.png" width="400" hieght="400">

* 환자는 어깨에 부착된 고유번호를 OCR을 통해 인식받아 기기를 할당받는다.
* 할당 되어진 기기는 환자의 옆모습을 중점으로 따라간다.
* 의료진은 환자의 상태를 앱에서 쉽게 확인할 수 있다.

# Ⅲ. **개발환경**
* Android Studio
* RaspberyPI

# Ⅳ. 주요 기능
### 1. OCR을 통한 글자 인식
### 2. ObjectDetection을 통한 객체 인식
### 3. Load Cell을 이용한 수액 무게 측정
### 4. UDP 통신을 통해 앱과 통신
  
# Ⅴ. 세부 기능
### 1. OCR
<img src="https://user-images.githubusercontent.com/73852272/98271963-dfe7c100-1fd3-11eb-8f74-ba969f03f014.png" width="400" hieght="400">

* Frame상에서 글자를 추출하여 문자열로 변환

### 2. Object Detection
<img src="https://user-images.githubusercontent.com/73852272/98271976-e24a1b00-1fd3-11eb-98e4-83134f5f09cb.png" width="400" hieght="400">

* Frame 상에서 '사람' 객체를 검출

