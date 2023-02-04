# IF I AM A EMOTICON

**프로젝트 소개** : https://rahites.tistory.com/137

**2022 5th D&A BigData Conference**  
Team : 비주얼 어벤져스

## 배경
현대인들은 카카오톡, 인스타그램 등 다양한 SNS에서 이모티콘을 사용합니다. 하지만 현재 사용하는 이모티콘은 작가들이 이미 만들어 놓은 이모티콘으로 나의 본질적인 감정을 표현하는 데 있어 한계가 존재합니다. 따라서 나의 표정을 담은, 내가 원하는 캐릭터의 모습의 이모티콘을 만들어 이모티콘을 사용하는 사람의 재미와 흥미를 더 돋우어 보려합니다.

## PipeLine
**1. 이모티콘 이미지 생성**
- 데이터 수집 및 가공 : '짱구는 못말려'에 나오는 등장인물의 이미지 수집 및 데이터 셋에 알맞은 형태로 가공
(https://github.com/YoongiKim/AutoCrawler)
- 실제 이미지 그림체 변환 : '짱구는 못말려' 그림체로 학습한 모델을 이용하여 실제 사람의 이미지 변환
(https://github.com/happy-jihye/Cartoon-StyleGAN)

![zzang](https://user-images.githubusercontent.com/87299629/216769301-64e291cd-903f-40ab-89b5-d3904b7958a9.gif)

**2. 감정 텍스트 생성**
- 감정분류 : 실제 사람의 얼굴 표정을 보고 7가지의 감정으로 분류
(fer : https://pypi.org/project/fer-pytorch/)
- 감정에 따른 텍스트 생성 : 감정분류를 통해 나온 감정에 어울리는 짱구 말투의 짧은 텍스트 생성
(KoGPT2 : https://github.com/SKT-AI/KoGPT2)

**3. 이모티콘 이미지에 감정 텍스트 삽입 - OpenCV**  
![final_zzang](https://user-images.githubusercontent.com/87299629/216769495-cef3a714-6f2f-4925-8cbb-bf6c1d6882cb.png)

