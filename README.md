# KoreanTTS

Tacotron2 모델과 Vocoder모델(Griffinlim, Wavenet, WaveGan)을 결합하여 한국어  TTS를 구현하는 프로젝트입니다. 

Based on

- https://github.com/TensorSpeech/TensorFlowTTS
- https://github.com/hccho2/Tacotron2-Wavenet-Korean-TTS



## Dataset

1. Koran Single Speaker Speech
   - 전문여자성우(12시간, wav, 44100khz, 12853개, 3GB)

2. 배우 유인나 목소리
   - KBS 라디오 유인나의 볼륨을 높여요(3시간, wav, 16000khz, 3327개, 480.6MB)
   - Google Speech to Text API
   - Kakao Speech API

3. 반려동물 훈련사 강형욱 목소리

   - ETRI 한국어 인식 API

   

## Preprocessing

1. wav 파일을 numpy 파일로 변환

2. ‘audio’, ‘mel’, ‘linear’, ‘text’ 등의 메타데이터를 묶어 저장 

3. Data/kss/＂음성파일이름.npz＂ 생성

4. Mel-spectrogram, Linear-spectrogram 정답셋을 생성



## Project 진행

1. Tacotron2 + GriffinLim + Singlespeaker
2. Tacotron2 + GriffinLim + Multispeaker(Deep Voice 2)
3. Tacotron2 + Melgan + Single Speaker
4. Tacotron2 + Melgan + Multispeaker (Transfer learning)



## 결과 

1. Tacotron2 + GriffinLim + Multispeaker(KSS + 유인나) 중 KSS 데이터 

   - Alignmnet (50000)

   ![image-20201105183045367](../../AppData/Roaming/Typora/typora-user-images/image-20201105183045367.png)

2. Tacotron2 + GriffinLim + Multispeaker(KSS + 유인나) 중 유인나 데이터 

   - Alignment(90000)

   ![image-20201105183118342](../../AppData/Roaming/Typora/typora-user-images/image-20201105183118342.png)

3. Tacotron2 + MelGan + Singlespeaker(KSS)

   - Alignment(90000)

     ![image-20201105183150241](../../AppData/Roaming/Typora/typora-user-images/image-20201105183150241.png)

