# Tahnsiri
## 장애인 상담챗봇 프로젝트, consultation chatbot for the disabled NLP

- 'Tahnsiri' [제9회 투빅스 컨퍼런스](http://www.datamarket.kr/xe/index.php?mid=board_pdzw77&page=2&document_srl=63534)(2020.01.16)에서 진행한 상담 챗봇 프로젝트입니다.

![발표 ppt](https://user-images.githubusercontent.com/87759826/149263884-f381c26d-18b0-43ba-9bda-a338cec3e53b.jpg)

## Description 📖

- 본 프로젝트에서는 네이버 지식인, 다음 등 검색창의 데이터를 직접 수집하여, 장애인 상담 질문에 대한 답변 챗봇을 구현하였습니다.

1. **[Model]** 

## Result (Mobile) 

- 챗봇에 주요 질문을 검색한 결과 화면

![시현화면](Presentation/탄시리_시현.PNG)

![시현영상](Presentation/탄시리_시현영상.mp4)

## Presentation 🙋

컨퍼런스 발표 자료입니다.
* [![GoogleDrive](https://drive.google.com/file/d/10J3h0k6MF2T2SXyh2lUGeRAboJWPNlZH/view)

## Contributor 🧑‍🤝‍🧑

- 본 프로젝트에는 [빅데이터 분석 및 인공지능 대표 연합동아리 ToBig's](http://www.datamarket.kr/xe/) 멤버들이 참여하였습니다.

|기수|이름|
|:-----:|:-----:|
|10기|[이준걸]|
|10기|[임진혁]|
|11기|[권혜민]|
|12기|[김효은]|
|12기|[배유나]|
|12기|[신윤종]|
|12기|[이유진]|

## File Directory 📂

```shell
Tahnsiri
├── 1. crawler
│   ├── make_song_meta_and_playlist.ipynb       # 노래, 플레이리스트 데이터 전처리
│   ├── make_mel_data.ipynb                     # 멜 데이터 전처리
│   └── make_mel_batch_data.ipynb               # 멜 데이터 배치 단위로 전처리
│
├── 2. preprocessig
│   ├── genre_embedding_model.ipynb             # Music2Vec
│   ├── mel_embedding_model.ipynb               # Time Convolutional Autoencoder
│   └── genre_and_mel_embedding_model.ipynb     # CosineEmbeddingLoss Multimodal
│
├── 3. model
│   └── embedding_visualization_tsne.ipynb      # t-SNE를 활용한 각 임베딩별 시각화
│
├── 4. model opt
│   ├── make_ranking_data_preprocessig.ipynb    # 각 임베딩별 코사인 유사도 Top50 데이터 셋 제작 
│   ├── make_ranking_data_multiprocessig.py     # make_ranking_data_preprocessig의 multiprocessig을 위한 함수
│   ├── make_ranking_data.ipynb                 # 순위별 가중치 ranking, 각 임베딩 별 상위 Top3 ranking
│   └── cos_sim_music_serving.ipynb             # 각 임베딩, ranking 별 결과
│
└── 5. presentation
    ├── crawling                                # 결과창 구현을 위한 데이터 수집
    │   └── melon_crawling.py 
    │ 
    │
    └── requirements.txt                        # 필요 패키지 목록
      
```
