# 고양이/강아지 구분하는 AI
- 3만장의 사진으로 티처블머신으로 훈련시킴.
- 왠만한 고양이/강아지 구분함. 


## 설치법 및 사용법 
1. VSCode에서 'Go Live'를 사용하여 로컬웹서비스로 사용할 수 있음. 
2. netlify, cloudtype 등 공짜로 웹서비스 할 수 있는 서버에 파일과 my_model 을 통째로 올리기
3. 깃허브의 앱서비스를 사용해 볼 것 


## 추가 미션
- 부트스트랩 등의 UI 프레임웍을 추가하여 더 멋진 UI로 꾸미기 
- 모바일브라우저에서 테스트해 보고 어울리는 UI로 꾸미기 
- 모바일 버전을 내 주변에 알려서 사용해 보게 하기 

<hr>
## 이미지 참조  

-  https://www.kaggle.com/competitions/dogs-vs-cats/overview



# index.html VS index_adv.html
* index는 기본 TM 버전
* index_adv는 얼굴상의 가능성을 그래프로 표현하기 위한 버전
  * style.css에서 그래프를 위한 css 추가 
  * 화면 reload 할 경우 발생하는 캔버스 겹치는 버그 해결 등
  ![버그화면](%EC%BA%94%EB%B2%84%EC%8A%A4%EA%B2%B9%EC%B9%98%EB%8A%94%EB%B2%84%EA%B7%B8%ED%99%94%EB%A9%B4.png)
  * 동적으로 변하는 닮음상의 확률을 그래프로 표현하기 위한 css의 이해를 위해... '여우'의 그래프를 화면의 하단에 고정값으로 표시되게 하였음. 참조 바람. 

  ```js
  <div class="result-box">
            <div id="label-container"></div>
        </div>
        <div class="result-box">
            <div id="label-container-ex">
                <div>
                    <div class="animal-label d-flex align-items-center">
                        <span class="label-title">여우</span></div>
                    <div class='bar-container position-relative container'>
                    <div class='fox-box'></div>
                    <div class='d-flex justify-content-center align-items-center fox-bar' style='width: 65%'>
                        <span class='d-block percent-text'>65%</span>
                    </div>
                </div>
            </div>
        </div>
  ```

