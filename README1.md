## 개요
대부분 여행을 가기 위해서는 사전지식을 미리 웹사이트로부터 검색하여 정보를 찾아야 한다.<br/>
일상의 피로를 탈피하기 위해 떠나는 여행의 시작을 고달픈 정보 탐색과 함께 해야 하는 아련한 현실을 해결하기 위해<br/>
대량의 여행 사진을 CNN 모델에 학습시켜 학습되지 않은 사진을 보고 그 사진의 장소, 이름, 맛집, 주변 숙박업소를 추천해주는 서비스<br/>

## 필요성
* 외국인뿐만 아니라 일반인도 모든 여행지 정보를 알고 있기는 어렵다.
* 다양한 여행지 정보를 검색보다 빠르게 제공할 수 있다.

## 제안자 능력
* 데이터 수집 및 처리 능력 <br/>
 포털사이트(구글, 네이버)에 있는 이미지 데이터를 크롤링하여 전처리, 및 데이터 증폭 (Selenium 및 openCV, ImageGenerator 이용)
* 웹 사이트 개발 능력<br/>
 HTML5, CSS3를 이용하여 웹 사이트 구축
 Flask 서버구축 및 결과물 출력<br/>
* 딥러닝 모델 설계<br/>
 합성곱 신경망을 이용히야 학습 훈련 진행

 ## 관련 업종/기술 분석
 * 나만의 맛집 검색 "망고플레이트"<br/>
 여러 맛집 정보를 지역별, 유형별, 가격대별로 분류되머 후기를 남기고 정보를 공유하는 플랫폼이다.
 * 액티비티 예약 플랫폼 'Klook'<br/>
 여행지 근처에서 즐길 수 있는 놀거리(액티비티, 체험, 투어, 교통편 등) 정보를 제공하고 쉽게 예약이 가능하다.

 ## 개발 내용

# 1. 데이터 선정 (국보 15종)
![image](https://user-images.githubusercontent.com/110643793/208844455-3abbaaa6-f62f-480c-8148-3d8d4a2771c9.png)
* 선정 이유 : 
 1. 특징이 명확하여 한눈에 알아보기 쉬움
 2. MZ 세대들에게 잊혀진 문화유산을 알릴 기회 제공
 3. 한국 역사를 알지 못하는 외국인에게 쉽게 정보 제공 가능
# 2. 데이터 수집 (클래스당 1,000장씩)
![image](https://user-images.githubusercontent.com/110643793/208847699-69bb01ea-a713-4739-b05d-9158a712bccc.png)
* Selenium을 이용하여 네이버, 구글에서 각 클래스당 약 1,000장씩 확보, 총 15,000장
# 3. 데이터 전처리
![image](https://user-images.githubusercontent.com/110643793/208847805-7fe1c0d6-8f29-480b-8039-0b5545b4cbcc.png)
* 학습에 불필요한 데이터 제거
# 4. 데이터 증폭
![image](https://user-images.githubusercontent.com/110643793/208847984-02ea6a22-ec38-4b63-98e6-416ee7c3de36.png)
* 필요한 사진 데이터는 tensorflow에 ImageDataGenerator를 활용하여 2~3배 개수 증폭
# 5. CNN 모델 설계
![image](https://user-images.githubusercontent.com/110643793/208848683-0e091e68-0134-43e6-b3b5-e66469ecff76.png)
# 6.학습모델 결과
![image](https://user-images.githubusercontent.com/110643793/208848751-1d961906-d0d5-487d-b600-671f083bd9c5.png)
# 7. 웹 페이지 구현
![image](https://user-images.githubusercontent.com/110643793/208848877-435bf247-125f-4200-b0b1-ed8bdd4df5e1.png)
# 8. Flask 서버 구현
![image](https://user-images.githubusercontent.com/110643793/208849050-0be20505-625b-4875-bfb7-a596861b6f9b.png)
![image](https://user-images.githubusercontent.com/110643793/208849285-0b0ca3c0-1865-42c4-997c-f4759d13e5bf.png)
# 9. 시연 영상
