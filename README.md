# 결론
- 영어에 대한 인식율은 높지만, 한국어나 아랍어 등 다른 나라의 언어에 대한 인식율을 낮았다. 
- 프로젝트에서 주어진 Sample 이미지 외에 추가적으로 2개를 더 돌려서 결과를 비교 분석해 보았다. 

## (1) RNN부분에서 LSTM 모델로 학습한 결과

- 300 epochs으로 학습 시켜서 validation loss를 1.73483까지 줄였다. (200 epochs = 2.06073, 100 epochs = 2.88273)

![LSTM_crnn_result](https://user-images.githubusercontent.com/39249809/100546744-565fa200-32a6-11eb-8ab9-1a8b7f4068b3.png)


## (2) RNN부분에서 GRU 모델로 학습한 결과

- 300 epochs으로 학습 시켜서 validation loss를 1.70062까지 줄였다. (200 epochs = 2.06909, 100 epochs = 2.84003)

![GRU_crnn_result](https://user-images.githubusercontent.com/39249809/100546736-5364b180-32a6-11eb-9a3c-89be09b23476.png)


## 결론적으로 GRU 모델이 성능이 약간 더 좋았다. 

![LSTM_GRU_crnn_result](https://user-images.githubusercontent.com/39249809/100546745-56f83880-32a6-11eb-81be-e085116e9a52.png)


## 첫번째 샘플 이미지!

![sample](https://user-images.githubusercontent.com/39249809/100546753-58c1fc00-32a6-11eb-884b-be4d1509e88b.jpg)

![sample_result1](https://user-images.githubusercontent.com/39249809/100546761-5c558300-32a6-11eb-9ab5-5699a06ddbbf.png)

### (1) RNN부분 LSTM 학습 결과

![LSTM_sample1](https://user-images.githubusercontent.com/39249809/100546748-56f83880-32a6-11eb-863e-76dec7d61e78.png)

### (2) RNN부분 GRU 학습 결과

![GRU_sample1](https://user-images.githubusercontent.com/39249809/100546737-5495de80-32a6-11eb-93f0-ad22a102677f.png)

- 단어간의 간격이 충분이 멀기 때문에, 각 단어의 위치를 잘 찾아내었다.
- 아랍어는 인식하지 못했으나, 영어는 마지막 글자를 하나 덧붙인 것 SLEEPER***E***(LSTM), SLEEPER***S***(GRU) 빼고는 잘 인식하였다. 

## 두번째 샘플 이미지

![sample1](https://user-images.githubusercontent.com/39249809/100546756-59f32900-32a6-11eb-955c-aa183670f9ae.jpg)

![sample2_result](https://user-images.githubusercontent.com/39249809/100546757-5a8bbf80-32a6-11eb-9608-55b7f8a6ab71.png)

### (1) RNN부분 LSTM 학습 결과

![LSTM_sample2](https://user-images.githubusercontent.com/39249809/100546749-5790cf00-32a6-11eb-885a-44c54347af40.png)

### (2) RNN부분 GRU 학습 결과

![GRU_sample2](https://user-images.githubusercontent.com/39249809/100546739-552e7500-32a6-11eb-9ab6-127a6daebc40.png)

- 다양하게 존재하는 작고 큰 단어 영역을 잘 잡아내었다. 아래 왼쪽 벽에 위치하는 작은 단어도 찾아내었다.
- HAIR 같은 경우에는 주변에 있는 둥그런 테두리 부분과 구분하지 못해서 ***E***HARE(LSTM), ***CI***HARE(GRU)로 잘못인식 하였다.
- 왼쪽 아래 벽면에 아주 작게 보이는 JASON이라는 단어를 찾아내긴 했지만, 글자 인식을 잘 하지 못했다. 

## 세번째 샘플 이미지

![sample3](https://user-images.githubusercontent.com/39249809/100546758-5b245600-32a6-11eb-8a7a-3364b4e4b53a.jpeg)

![sample3_result](https://user-images.githubusercontent.com/39249809/100546759-5b245600-32a6-11eb-8a30-3c3d2793bb68.png)

### (1) RNN부분 LSTM 학습 결과

![LSTM_sample3](https://user-images.githubusercontent.com/39249809/100546751-58296580-32a6-11eb-9217-76b63a053867.png)

### (2) RNN부분 GRU 학습 결과

![GRU_sample3](https://user-images.githubusercontent.com/39249809/100546741-55c70b80-32a6-11eb-8a8a-f4f0795a17e0.png)

- 오밀 조밀하게 붙어있는 다양한 단어들을 잘 구분해서 찾아내었다. 
- 하지만 단어들이 많이 기울어져있고, 작아서 그런지 LSTM과 GRU 모두 글자 인식율이 매우 낮았다.



