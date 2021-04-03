# EDA 1 - NAVER WEBTOON

- 네이버 웹툰 EDA 프로젝트

    가설 1) 별점이 낮은 회차의 이미지갯수의 상관도 찾기 (분량이 작을수록 낮은가?)

    가설 2) 

    ## 👉🏻 가설 1 검정

1) 현재 연재중인 웹툰 데이터 프레임

```python
with open('data/weekly_dataframe.pkl', 'rb') as f:
    load_datas = pickle.load(f)

len(load_datas)
load_datas
```

![EDA%201%20-%20NAVER%20WEBTOON%20e121e8a960ce4f19a9df68e009566cf9/Untitled.png](EDA%201%20-%20NAVER%20WEBTOON%20e121e8a960ce4f19a9df68e009566cf9/Untitled.png)

2) 별점의 평균과 이미지 갯수간의 상관관계를 파악

```python
df = load_datas[["star","img"]]
sns.heatmap(df.corr(), cmap="YlGnBu", annot=True)
plt.show()
```

![EDA%201%20-%20NAVER%20WEBTOON%20e121e8a960ce4f19a9df68e009566cf9/Untitled%201.png](EDA%201%20-%20NAVER%20WEBTOON%20e121e8a960ce4f19a9df68e009566cf9/Untitled%201.png)

0에 가까운 결과로 상관도가 낮음을 알 수 있었다.