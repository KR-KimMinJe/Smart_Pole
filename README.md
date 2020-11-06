# Ⅰ. **개요**
*   개발 기간 : 2019.12.03 ~ 2019.12.04
*   개발 목적 : 
*   대한전기학회 워크샵. 129-130
*   상명 Prime 성과우수대회 최우수상

# Ⅱ. **동작 구성도**
<img src="https://user-images.githubusercontent.com/73852272/98375722-dae34a00-2085-11eb-91c0-2c81fe0310fd.jpg" width="400" hieght="400">

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

### 3. User Tracking
<img src="https://user-images.githubusercontent.com/73852272/98373376-7ffc2380-2082-11eb-9178-7df4f5ad5257.png" width="400" hieght="400">

* 프레임 상에 '사람' 객체가 검출 되었다면 해당 객체의 BBox를 제외한 여백 값(파란색 화살표)을<br>제거한다. 
* BBox가 그려지는 OpenCV의 Ractangle 함수의 시작 값과 끝 값을 받아
<br>BBox 내에서 (좌측Width-우측Width,상위Height-하위Height) 좌표를<br>
'사람' 객체의 정중앙 값으로 가정하고 정중앙 값의 이동에 따라 모터를 제어하여
<br>BBox의정중앙 값이 항상 Frame상에서의 정중앙에 오도록 하여 따라간다.

### 4. Load Cell
<img src="https://user-images.githubusercontent.com/73852272/98375090-fb5ed480-2084-11eb-9b53-a3748b8ccd2f.jpg" width="300" hieght="300">

* 링거대의 걸림쇠 부분에 Load Cell을 부착하여<br>링거액의 잔액을 실시간으로 어플리케이션에서 확인할 수 있도록 한다.

### 5. Application
<img src="https://user-images.githubusercontent.com/73852272/98375494-84760b80-2085-11eb-9c82-6d263aeb801c.png" width="300" hieght="300">

  &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; 1. 의료진용&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;2. 환자용

