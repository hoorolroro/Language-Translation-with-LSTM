# LSTM 기반 번역기
## LSTM(Long Short-Term Memory)의 구조  
● RNN의 한계(Long-term dependency) : 중요한 정보가 recurrent step이 계속됨에 따라 희석되는 문제가 있다.

● LSTM에서는 Cell이란 구조를 만들어 gate에 의해서, 중요한 정보만 선택하고 다음 state에 전달하는 구조로 RNN의 문제점을 개선하였다.

<img src="https://user-images.githubusercontent.com/98728682/153707834-2ae2ae2d-3a19-4ce7-ba83-c38967ad4dff.png" width="450" height="350">  

## Basic NMT(Neural Machine Translation)의 구조  
● Encoder  
- 입력으로 들어오는 문장을 LSTM을 이용해 잘 압축한다.  
- 입력의 마지막 단어를 통해 나온 hidden state가 최종적으로 사용될 encoded layer이다.  

● Decoder  
- Encoding된 정보 vector를 이용해 출력 문장으로 하나하나 풀어낸다.  
- 입력의 마지막 hidden state를 초기값으로 사용한다.  


<img src="https://user-images.githubusercontent.com/98728682/153708836-a425b499-08de-4125-8074-7f3616e96217.png" width="500" height="350">

## 프로그램 시현  
● 영어와 프랑스어 쌍으로 이루어진 sequence to sequence dataset을 학습한다.  

● 아래와 같은 결과가 나왔다.  
<img src="https://user-images.githubusercontent.com/98728682/153710157-92860926-5c56-4591-bb28-2cc8e8b22bf7.png" width="500" height="200"><img src="https://user-images.githubusercontent.com/98728682/153710167-bbb695be-d0f3-4e06-bd76-dfed9a4aac88.png" width="500" height="200"><img src="https://user-images.githubusercontent.com/98728682/153710178-0dbb1d81-da1c-4d86-b66e-9297f4fda3fd.png" width="500" height="200">
