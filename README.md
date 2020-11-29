# G12_OCR_Recognition_Model

# 결론
- 300 epochs으로 학습 시켜서 validation loss를 1.74649까지 줄였다. (100 epochs = 2.92478, 200 epochs = 2.06616)
- 영어에 대한 인식율은 높지만, 한국어나 아랍어 등 다른 나라의 언어에 대한 인식율을 낮았다. 
- 프로젝트에서 주어진 Sample 이미지 외에 추가적으로 2개를 더 돌려서 결과를 비교 분석해 보았다. 

## 첫번째 샘플 이미지

![sample](https://user-images.githubusercontent.com/39249809/100537544-d701ac80-326c-11eb-8420-116da3001b58.jpg)
![sample_result1](https://user-images.githubusercontent.com/39249809/100537551-dbc66080-326c-11eb-8c02-e44875506ee8.png)
![sample_result2](https://user-images.githubusercontent.com/39249809/100537552-dc5ef700-326c-11eb-964d-53f21dc5c70f.png)

- 단어간의 간격이 충분이 멀기 때문에, 각 단어의 위치를 잘 찾아내었다.
- 아랍어는 인식하지 못했으나, 영어는 잘 인식하였다. 

## 두번째 샘플 이미지

![sample1](https://user-images.githubusercontent.com/39249809/100537545-d832d980-326c-11eb-9258-f5d7bee79133.jpg)
![sample2_result](https://user-images.githubusercontent.com/39249809/100537546-d8cb7000-326c-11eb-95d4-55e6379b23cf.png)
![sample2_result1](https://user-images.githubusercontent.com/39249809/100537547-d9640680-326c-11eb-8715-4bbe93e48825.png)

- 다양하게 존재하는 작고 큰 단어 영역을 잘 잡아내었다. 아래 왼쪽 벽에 위치하는 작은 단어도 찾아내었다.
- HAIR 같은 경우에는 주변에 있는 둥그런 테두리 부분과 구분하지 못해서 GHAIR로 잘못인식 하였다.
- 왼쪽 아래 벽면에 아주 작게 보이는 JASON이라는 단어를 찾아내긴 했지만, 글자 인식을 잘 하지 못했다. 

## 세번째 샘플 이미지

![sample3](https://user-images.githubusercontent.com/39249809/100537548-d9fc9d00-326c-11eb-925f-388a3aa52002.jpeg)
![sample3_result](https://user-images.githubusercontent.com/39249809/100537549-da953380-326c-11eb-8dd0-7c8e40ad1ae5.png)
![sample3_result1](https://user-images.githubusercontent.com/39249809/100537550-db2dca00-326c-11eb-83f6-e3ab1757bfdb.png)

- 오밀 조밀하게 붙어있는 다양한 단어들을 잘 구분해서 찾아내었다. 
- 하지만 단어들이 많이 기울어져있고, 작아서 그런지 인식율이 매우 낮았다. 




