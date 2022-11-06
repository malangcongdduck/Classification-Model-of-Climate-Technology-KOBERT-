# Classification-Model-of-Climate-Technology-KOBERT-
- 기후기술분류체계로 분류하는 AI
- 녹색기후기술센터에서 제공하는 기후기술분류체계, 국가연구개발사업 Data 사용
- SKTBrain에서 제공하는 KoBERT 사용

  
## Model
  - SKT Brain Team에서 제공하는 KoBERT
  - KoBERT 학습 셋과 학습 환경, 성능은 아래의 링크를 확인.
  - https://github.com/SKTBrain/KoBERT
  - Model summary
  ![image](https://user-images.githubusercontent.com/76987629/200157682-025d6493-7d45-4e74-9a87-dd252313ed30.png)

  
## Experiment-environment
  - train: 174,304
  - test: 217,879
  - feature: 사업명 + 사업_부처명 + 과제명 + 요약문_한글키워드
  - label: 기후기술분류체계에 따른 46개의 label
  - label info는 아래를 참조 ↓
  - Label One_Hot Encoding
  - Validation_split = 0.2
  - Earlystopping
  - Epoch = 100
  - patience = 3
  - Min_delta =0.0001
  - Optimizer = Adam(lr=1e-4)
  - Batch_size = 32
  - loss = categorical_crossentropy
  

## data analysis
  - '과제명 최소 길이 : 1'
  - '과제명 25% 길이 : 6.0'
  - '과제명 최대 길이 : 17'
  - '과제명 75% 길이 : 11.0'
  - '과제명 평균 길이 : 8.603091106969064’

  - '요약문_한글키워드 최소 길이 : 1'
  - '요약문_한글키워드 25% 길이 : 5.0'
  - '요약문_한글키워드 최대 길이 : 17'
  - '요약문_한글키워드 75% 길이 : 9.0'
  - '요약문_한글키워드 평균 길이 : 7.467393887839478'
<br>

  ![image](https://user-images.githubusercontent.com/76987629/200157749-d473ddd3-37a1-4794-8e0e-c10353aab892.png)
<br>
  
<사업_부처별 진행 연구 개수(train_data)>
  ![image](https://user-images.githubusercontent.com/76987629/200157754-56db9d1f-103e-4c7a-be11-c44c8f37d392.png)


    
    
## *Label info*
  |label|내용|
  |:------:|:---:|
  |00|NaN|
  |01|원자력 발전|
  |02|핵융합 발전|
  |03|청정화력발전·효율화|
  |04|수력|
  |05|태양광|
  |06|태양열|
  |07|지열|
  |08|풍력|
  |09|해양에너지|
  |10|바이오에너지|
  |11|폐기물|
  |12|수소 제조|
  |13|연료전지|
  |14|전력 저장|
  |15|수소 저장|
  |16|송배전 시스템|
  |17|전기 지능화 기기|
  |18|수송 효율화|
  |19|산업 효율화|
  |20|건축 효율화|
  |21|CCUS|
  |22|Non-CO2저감|
  |23|유전자원·유전개량|
  |24|작물재배·생산|
  |25|가축 질병관리|
  |26|가공·저장·유통|
  |27|수계·수생태계|
  |28|수자원 확보 및 공급|
  |29|수처리|
  |30|수재해 관리|
  |31|기후 예측 및 모델링|
  |32|기후 정보 경보 시스템|
  |33|해양생태계|
  |34|수산자원|
  |35|연안 재해 관리|
  |36|감염 질병 관리|
  |37|식품 안전 예방|
  |38|산림 생산 증진|
  |39|산림피해저감|
  |40|생태·모니터링·복원|
  |41|신재생에너지 하이브리드|
  |42|저전력 소모 장비|
  |43|에너지 하베스팅|
  |44|인공광합성|
  |45|기타 기후변화 관련 기술|
