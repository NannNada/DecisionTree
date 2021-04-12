# 영어 영화리뷰 감성분석
자세한 설명은 주피터 노트북 안에
## 라이브러리
- CountVectorizer : 단어들의 카운트(출현 빈도(frequency))로 여러 문서들을 벡터화
- LogisticRegression
- make_pipeline : 서로 다른 매개 변수를 설정하면서 함께 교차 검증 할 수있는 여러 단계를 조합
- pandas
- load_files: 파일을 읽어들이는 함수(머신러닝 용)
- numpy
- matplotlib.pyplot

## 1. 문제정의
- 영화리뷰 데이터셋을 활용해 긍정리뷰와 부정리뷰를 구분하는 감성분석
- 긍정/부정 리뷰에서 자주 사용되는 단어를 확인

## 2. 데이터 수집 
- Large movie dataset 사용 
<img width="927" alt="스크린샷 2021-04-12 오후 6 54 59" src="https://user-images.githubusercontent.com/42399580/114376448-99207780-9bc0-11eb-8164-9e2a3495463c.png">

## 3. 데이터 전처리
- 일반 정형화 데이터 : 결측치, 스케일링, 특성공학, 이상치....
- 텍스트 데이터
    - 오탈자 제거
    - 띄어쓰기 교정
    - 이모티콘 수정
    - 불필요한 글자 제거(stop word)
    - 데이터 정형화 : 토큰화, 수치화
