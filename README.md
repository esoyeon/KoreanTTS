# KoreanTTS

Tacotron2 모델과 Vocoder모델(Griffinlim, Wavenet, MelGan)을 결합하여 한국어  TTS를 구현하는 프로젝트입니다. 

![name](https://img.shields.io/badge/-이소연-black) ![https://img.shields.io/badge/-%EC%9D%B4%EC%86%8C%EC%97%B0-black](https://img.shields.io/badge/-김도연-black) ![name](https://img.shields.io/badge/-신재영-black) ![name](https://img.shields.io/badge/-김지예-black)

Based on

- https://github.com/TensorSpeech/TensorFlowTTS
- https://github.com/hccho2/Tacotron2-Wavenet-Korean-TTS

- https://carpedm20.github.io/tacotron/

## Dataset

1. Koran Single Speaker Speech
   - 전문여자성우(12시간, wav, 44100khz, 12853개, 3GB)

2. 배우 유인나 목소리
   - KBS 라디오 유인나의 볼륨을 높여요(3시간, wav, 16000khz, 3327개, 480.6MB)
   - Google Speech to Text API
   - Kakao Speech API

3. 반려동물 훈련사 강형욱 목소리

   - ETRI 한국어 인식 API




학습에 진행한 오디오 데이터는 저작권 문제로 공유하지 않습니다. 각 데이터 출처에서 확인해주세요. 

- KSS: https://www.kaggle.com/bryanpark/korean-single-speaker-speech-dataset

- KBS 라디오: http://program.kbs.co.kr/2fm/radio/uvolum/pc/index.html

  

## Preprocessing

1. wav 파일을 numpy 파일로 변환

2. ‘audio’, ‘mel’, ‘linear’, ‘text’ 등의 메타데이터를 묶어 저장 

3. Data/kss/＂음성파일이름.npz＂ 생성

4. Mel-spectrogram, Linear-spectrogram 정답셋을 생성



## Project 진행

총 4가지의 학습을 진행하였습니다. 

1. Tacotron2 + GriffinLim + Singlespeaker

2. Tacotron2 + GriffinLim + Multispeaker(Deep Voice 2)

3. Tacotron2 + Melgan + Single Speaker

4. Tacotron2 + Melgan + Multispeaker (Transfer learning)

   

## 결과 

1. Tacotron2 + GriffinLim + Multispeaker(KSS + 유인나) 중 KSS 데이터 

   - Alignmnet (50000)

   ![50000_kss](https://user-images.githubusercontent.com/67999107/98225804-8b732000-1f98-11eb-8c4b-bc9a52a7443f.png)

2. Tacotron2 + GriffinLim + Multispeaker(KSS + 유인나) 중 유인나 데이터 

   - Alignment(90000)

   ![90000_유인나](https://user-images.githubusercontent.com/67999107/98225863-9a59d280-1f98-11eb-8dd1-e2955402e825.png)

3. Tacotron2 + MelGan + Singlespeaker(KSS)

   - Alignment(90000)

  ![melgan_90000](https://user-images.githubusercontent.com/67999107/98225892-a2b20d80-1f98-11eb-850b-0ce0d192696f.png)



- 자세한 학습과정과 결과 오디오는 발표자료에서 확인하실 수 있습니다. 
   Project Paper.pptx

  

