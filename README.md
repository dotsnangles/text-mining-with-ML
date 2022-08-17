# text-mining-with-ML

### Objectives
- 웹툰 독자의 경향을 파악하기 위해 수치 데이터를 웹 크롤링 후 분석 및 시각화를 진행한다.
- 우크라사태가 한국 경제에 미치는 영향을 파악하기 위해 웹 크롤링한 신문기사에 워드 클라우드, 토픽 모델링 기법을 활용한다.
- 로지스틱 리그레션을 활용해 우크라사태 이전/이후 신문기사 내용의 감성 분석을 진행한다.

### Models and Data
- TF-IDF / LDA / Logistic Regression
- 네이버 웹툰 장르별 회차별 독자 참여 수치 19622건
- 우크라사태 이전/이후 신문기사 제목 및 본문 2912건

### Envs and Requirements
- Colab
- BeautifulSoup, Pandas, RE, KoNLPy, Scikit-Learn, Gensim, Matplotlib, Seaborn

### Progress
- 웹 크롤링 및 텍스트 데이터 정제
- 데이터 분석 및 시각화
- 토큰화 및 코퍼스 사전 구축
- 불용어 사전 및 사용자 사전 구축
- TF-IDF 워드 클라우드
- LDA 토픽 모델링
- 바이그램 / 트라이그램 적용
- 응집도 / 복잡도 기준 최적 에폭 및 토픽 갯수 설정
- 로지스틱 리그레션을 활용한 감성 분석

### Retrospective
- 웹 크롤링과 ML 기초를 배운 후 유의미한 적용을 위해 진행한 프로젝트
- BeautifulSoup을 사용해 목표 범위의 데이터를 크롤링하는 코드를 작성
- 웹 크롤링을 기법으로 단기간에 방대한 데이터 확보가 가능함을 알게 되었고, 재사용 가능한 코드 작성의 중요성에 대해 배울 수 있었음
- 정규표현식을 활용해 불필요한 문자 및 패턴이 있는 노이즈를 찾아 제거
- Gensim/wordcloud 사용으로 구현 난이도는 높지 않았으나 처음부터 만족스러운 결과를 얻을 수 없었음
- 수행하려는 태스크가 이미 패키지로 구현되어 있는 경우라도 다양한 조건으로 실험을 진행해야 보다 완성도 있는 결과물을 산출할 수 있음을 배움
- KoNLPy의 Komoran, Mecab, Okt의 성능을 직접 시험해보고 사용자 사전 등록이 가능한 Komoran을 토크나이저로 선택
- `18년 논문인 “텍스트마이닝을 위한 한국어 불용어 목록 연구”를 참조해 불용어 사전 구축을 시작하고 고유명사 중심으로 사용자 사전을 구축
- 사용자 사전 없이 바이그램 / 트라이그램 결과 시험을 해봤으나 유의미한 성과는 없었음
- 사전 구축에 최대한의 노력을 기울였으며 이후 최적 에폭 및 토픽 갯수 설정을 위한 실험을 진행
- 실험 결과 보존이 되지 않은 상황에서 재현조차 불가능한 경우가 있었는데 답이 정해져 있지 않은 만큼 경험적으로 접근하며 기록을 남겨야 함을 깨달음
- 같은 하이퍼 파라미터 설정으로 다른 결과가 도출되는 것을 방지하기 위해 랜덤스테이트(Seed)를 고정해야 함을 알게 됨

### References
- 텍스트마이닝을 위한 한국어 불용어 목록 연구 - 길호현
- https://www.crummy.com/software/BeautifulSoup/
- https://pandas.pydata.org/
- https://konlpy.org/
- https://radimrehurek.com/gensim/
- https://scikit-learn.org/
- https://www.pythoncheatsheet.org/
