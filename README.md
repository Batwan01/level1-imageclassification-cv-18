<div align="right">
  <a href="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https://github.com/boostcampaitech7/level1-imageclassification-cv-18&count_bg=%23C6D2FF&title_bg=%23555555&icon=&icon_color=%23FFFFFF&title=hits&edge_flat=false"/></a>
</div>

# 딥하조
![대회 타이틀](https://github.com/user-attachments/assets/a3a97f02-1e01-4ea0-85cc-4d6f204df5cd)

- 2024.09.11 ~ 2024.09.26
- ImageNet Sketch 이미지 데이터 분류
- 1st Prize 🏆
- Naver Connect & Upstage 주관 대회
- [프로젝트 리포트 (README)](./Sketch%20Data%20Multi-Classification%20Project%20Report.pdf)

## Leaderboard
![리더보드](https://github.com/user-attachments/assets/05f98560-85fb-43b7-b272-bef54f9a97e1)



## 팀원 소개

| [![](https://avatars.githubusercontent.com/chan-note)](https://github.com/chan-note) | [![](https://avatars.githubusercontent.com/Donghwan127)](https://github.com/Donghwan127) | [![](https://avatars.githubusercontent.com/batwan01)](https://github.com/batwan01) | [![](https://avatars.githubusercontent.com/taehan79-kim)](https://github.com/taehan79-kim) | [![](https://avatars.githubusercontent.com/nOctaveLay)](https://github.com/nOctaveLay)  | [![](https://avatars.githubusercontent.com/Two-Silver)](https://github.com/Two-Silver)  |
| ---------------------------------------------------- | ------------------------------------------------------ | --------------------------------------------------- | ------------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| [임찬혁](https://github.com/chan-note)                  | [서동환](https://github.com/Donghwan127)                  | 🦇[박지완](https://github.com/batwan01)          | [김태한](https://github.com/taehan79-kim)                  | 🐈[임정아](https://github.com/nOctaveLay)                  | 🐡[이은아](https://github.com/Two-Silver)                  |

## 대회 소개
![image](https://github.com/user-attachments/assets/e889ae72-c64f-48bb-95f0-ce7c73d56e4c)

Sketch 이미지 분류 경진대회는 주어진 데이터를 활용하여 모델을 제작하고 어떤 객체를 나타내는지 분류하는 대회입니다.

Computer Vision에서는 다양한 형태의 이미지 데이터가 활용되고 있습니다. 이 중, 비정형 데이터의 정확한 인식과 분류는 여전히 해결해야 할 주요 과제로 자리잡고 있습니다. 특히 사진과 같은 일반 이미지 데이터에 기반하여 발전을 이루어나아가고 있습니다.

****하지만 일상의 사진과 다르게 스케치는 인간의 상상력과 개념 이해를 반영하는 추상적이고 단순화된 형태의 이미지입니다. 이러한 스케치 데이터는 색상, 질감, 세부적인 형태가 비교적 결여되어 있으며, 대신에 기본적인 형태와 구조에 초점을 맞춥니다. 이는 스케치가 실제 객체의 본질적 특징을 간결하게 표현하는데에 중점을 두고 있다는 점을 보여줍니다.****

이러한 스케치 데이터의 특성을 이해하고 스케치 이미지를 통해 모델이 객체의 기본적인 형태와 구조를 학습하고 인식하도록 함으로써, 일반적인 이미지 데이터와의 차이점을 이해하고 또 다른 관점에 대한 모델 개발 역량을 높이는데에 초점을 두었습니다. 이를 통해 실제 세계의 복잡하고 다양한 이미지 데이터에 대한 창의적인 접근방법과 처리 능력을 높일 수 있습니다. 또한, 스케치 데이터를 활용하는 인공지능 모델은 디지털 예술, 게임 개발, 교육 콘텐츠 생성 등 다양한 분야에서 응용될 수 있습니다.

## 사용된 데이터셋 정보

- **데이터셋 이름**: Sketch Data (ImageNet Sketch)
- **출처**: [Sketch Data 다운로드 링크](https://aistages-api-public-prod.s3.amazonaws.com/app/Competitions/000307/data/data.tar.gz)

### 데이터셋 설명

원본 **ImageNet Sketch** 데이터셋은 50,889개의 이미지 데이터로 구성되어 있으며, 1,000개의 객체에 대해 각각 대략 50개의 이미지를 포함하고 있습니다. 이 데이터셋은 일반적인 객체들의 핸드 드로잉 이미지로 구성되어 있으며, 실제 객체를 대표하는 다양한 스타일과 특징을 보여줍니다.

이번 Sketch 이미지 분류 경진대회에서 제공되는 데이터셋은 **네이버 커넥트재단 부스트캠프 AI Tech**에서 원본 데이터를 직접 검수하고 정제한 것입니다. 1,000개의 클래스 중 이미지 수량이 많은 상위 500개의 객체를 선정하였으며, 총 25,035개의 이미지 데이터가 포함되어 있습니다. 해당 이미지 데이터는 다음과 같이 구성됩니다.
- **학습 데이터**: 15,021개
- **Private & Public 평가 데이터**: 10,014개

```bash
data/
│
├── sample_submission.csv
├── test.csv
├── train.csv
│
├── test/
│   ├── 0.JPEG
│   ├── 1.JPEG
│   ├── 2.JPEG
│   ├── ...
│
├── train/
│   ├── n01443537/
│   │   ├── sketch_0.JPEG
│   │   ├── sketch_1.JPEG
│   │   ├── sketch_2.JPEG    
│   │   ├── ...
│   │
│   ├── n01484850/
│   │   ├── sketch_0.JPEG
│   │   ├── sketch_1.JPEG
│   │   ├── sketch_2.JPEG    
│   │   ├── ...
│   │   
│   ├── ... 
```

### License
이 데이터셋은 [Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)에 따라 사용됩니다. 자세한 내용은 [라이선스 링크](https://creativecommons.org/licenses/by/4.0/)에서 확인할 수 있습니다.

이 라이선스 하에서, 여러분은 다음과 같은 권리를 가집니다:
- **공유** — 어떤 매체나 형식으로도 데이터를 복사, 배포할 수 있습니다.
- **변경** — 데이터를 리믹스, 변형, 수정하고 상업적 목적으로도 사용할 수 있습니다.
단, 다음의 조건을 준수해야 합니다:
- **저작자 표시** — 적절한 출처를 제공하고, 라이선스 링크를 명시하며, 변경 여부를 표시해야 합니다.
자세한 내용은 [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/)에서 확인할 수 있습니다.

## Project Timeline
![프로젝트 타임라인](https://github.com/user-attachments/assets/82d524f8-79c1-4bbb-ab78-44b9220b8d8b)


## Models
- ResNet50
- eva02_large
- eva_giant

![image](https://github.com/user-attachments/assets/0302c586-42ae-492f-be48-292009b86f77)


## Augmentations
- HorizontalFlip
- VerticalFlip
- Rotate

![image](https://github.com/user-attachments/assets/4f66aaaf-e1ca-4800-98a1-6efdb86561e1)


## Voting
- Soft Voting
- Hard Voting
  
![image](https://github.com/user-attachments/assets/34e6350e-a600-451f-a148-ab25359eb4bc)


