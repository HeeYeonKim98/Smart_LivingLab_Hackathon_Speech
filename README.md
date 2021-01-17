# 2020년 스마트 리빙랩 해커톤 - 사운드 분야 (with Tensorflow) :computer: 
---
+ <http://www.ideaboom.net/page/competition_main.php?seq=115>
+ 본 대회 사운드 분야에서는 __딥러닝기반 패턴인식기술을 이용한 소음데이터 분류__ 를 목표로 합니다.
+ 모델의 성능 평가 요소 중 __정확도__ 는 __./utils/test.py__ 파일을 이용해 평가합니다.

---
### :pushpin: Dependencies

실험을 수행하는데 필요한 패키지를 정리한 파일입니다.

```console
pip install -r requirements.txt
```

___
### :open_file_folder: Database

해당 강좌에서 다운로드 후 ./data 폴더에 추가하여 사용

+ 16KHz 16bit mono PCM
+ Train : 6589개
+ Test : 18개

- Ctrl File List Form
  > us8k_ish_ __class__ _파일번호
___
### :zero: 특징 추출 단계 수행

+ MFCC(.mfc) 특징을 추출하여 파일로 저장합니다.
+ 해당 단계 수행은 ./utils/feature_extractor.py 에서 수행됩니다.

- run. py

```console
python run.py --step 0
```

---
### :one: 모델 훈련 단계 수행

+ 해당 단계 수행은 ./utils/train.py 에서 수행됩니다. 
+ 훈련/검증 데이터는 ./utils/dataloader.py 를 통해 얻을 수 있으며 수정하여 사용하시면 됩니다.
+ 모델은 반드시 __전체 모델__ 을 저장하십시오.

- run.py

```console
python run.py --step 1
```
___
### :two: 모델 평가 단계 수행

+ 해당 단계 수행은 ./utils/test.py 에서 수행됩니다.
+ 평가 데이터는 ./utils/dataloader.py 를 통해 얻을 수 있습니다.
+ 본 해커톤은 해당 스크립트를 이용해 평가를 진행하므로 __수정없이__ 사용할 것을 강력히 권장합니다.

- run.py

```console
python run.py --step 2
```

---
### License
```
Copyright (c) 2021-IMPRESS.