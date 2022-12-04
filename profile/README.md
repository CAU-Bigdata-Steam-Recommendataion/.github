# 진행상황 공유
- 현재 모델 수정해서 테스트 중인데, 램이 약 10기가 정도 들어서 테스트하기 아슬아슬함. 
- 기존 7개의 데이터로 훈련시킨(정확히는 7개의 80%) 모델에서 전체 데이터셋으로 확장해서 훈련시킴(전체 데이터의 80% 사용)
- user_features로 playtime_forever 추가
- item_features는 None으로 설정

-> 하지만 precision@k 방법으로 평가했을 때 현재 정확도가 매우 낮음

![image](https://user-images.githubusercontent.com/103106183/205478506-d73c1552-9784-4cf9-9cb4-79e4eee300e2.png)


# 회의록

### 2022-11-19

- 추천시스템에 사용할 attribute 결정
    
    ![image](https://user-images.githubusercontent.com/103106183/202835220-25bda64c-41e5-46af-81f8-ea401e0b831c.png)
    
    - `playtime_forever`
    - `voted_up`
    - `votes_up`
- 역할 분담
    - 데이터셋 추출 : `@fender2758`
    - LightFm 기반 추천 시스템 엔진 개발 : `@DoDoron`
    - ndcg 평가 기법 적용 성능 평가 및 개선점 도출 : `@jycforest29`
- 개발 계획
    
    
    | 기한 | 내용 | 그 외 |
    | --- | --- | --- |
    | 2022-11-19 ~ 2022-11-21 | 데이터셋 추출 | .pickle로 추출 |
    | 2022-11-21 ~ (최대)2022-11-30  | 추천 시스템 엔진 개발 |  |
    | 2022-11-30 ~ 2022-12-02 | ndcg 기법 기반 평가 |  |
    
    이후 미정
