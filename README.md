# 제주 방언 번역기 만들기.


## 주제
 제주 사투리를 위한 음성인식 방언 번역기 만들기  
 
## 목적 
 2022년 현재, 방언 음성인식은 정확하지 않고, 특히 표준어와 차이가 큰 제주 방언은 인식이 더욱 힘들기에,  
다양한 모델을 활용하여 방언 음성 인식 번역기를 제작한다.


---
 
 
  
  
## 기간 : 22. 09. 02 ~ 22. 09. 20  

## 팀원 및 역
    - 김규인 : Transformer, Bart, KoBart
    - 석민재 : Transformer, LED, Longformer
    - 양병진 : Transformer, Bart, KoBart, M2M100
    - 이재혁 : Transformer, DeepSpeach2, Tacotron2
    - 최현호 : Transformer, koSpeach, Electra
    
---

 
## 사용한 데이터
1. 음성데이터 1 : [kaggle - Jeju Single Speaker Speach Dataset](https://www.kaggle.com/datasets/bryanpark/jejueo-single-speaker-speech-dataset)

![Figure-02](https://user-images.githubusercontent.com/114709607/202993982-bcbde1c0-701f-4a75-8f24-6319cc2fa2bb.png)


2. 텍스트 데이터 : [AiHub - 한국어 방언 발화(제주도)](https://www.aihub.or.kr/aihubdata/data/view.do?currMenu=116&topMenu=100&aihubDataSe=ty&dataSetSn=121)

![Figure-03](https://user-images.githubusercontent.com/114709607/202994085-d97b1408-dc6a-428f-983e-9c3310783ae9.png)    
  
    
      
      

## 과정  
![Figure-01]( https://user-images.githubusercontent.com/114709607/202992169-8e2ef161-c018-48f4-ba8e-e202d7c0d262.png)  

1. 음성 데이터를 DeepSpeach2를 이용해 STT 수행  
2. 변환한 방언 텍스트를 TransFormer 모델을 사용해 표준어로 번역  
3. 번역된 텍스트를 Tacotron2, Naver CLOVA 를 사용해 오디오 파일로 변환


### STT 과정
![Figure-05](https://user-images.githubusercontent.com/114709607/202997707-5752b46a-4bad-4ad6-b63f-2a959c16af8d.png)


### 번역 과정
![Figure-04](https://user-images.githubusercontent.com/114709607/202996982-837382a2-ccb7-4725-a82c-bcfbdf1f1a96.png)
Transformer 4층의 결과가 제일 좋은 것을 알 수 있다.

###  TTS 과정

![Sample Audio](https://github.com/keorantribe/jeju_translation/issues/6#issue-1457531182)


## 결과
위의 과정을 통해 제주 방언을 표준어로 충분히 번역하는 모델 생성에 성공  
하지만 단조로운 데이터를 사용하고, 데이터의 양을 추가하고, 더 적합한 모델을 찾는다면 더 좋은 성능으로 개선이 가능할 것으로 보임
         
