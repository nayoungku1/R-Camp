# Winter 2026 Big Data Analysis using R  
---
* Date: Jan 5, 2026 - Jan 14, 2026
* Instructor: [Prof. Sohn](mailto:jsohn@handong.edu)
* Venue: Handong Global University HDH 403
---
## Directory 구조
```bash
├── cheat-sheets/   # R studio와 ggplot2의 명령어, 단축키, 공식 등을 담은 치트시트 (요약자료)
├── data/           # 참고 데이터셋 (csv파일)
├── day*/           # 각 강의 날짜에서 사용한 데이터셋과 도움이 될만한 자료
├── environment.yml # Conda environment
└── README.md       # Overview와 기초적인 documentation
```
## R & R Studio 설치

### 직접 설치
* Cran을 통해 R 설치 (한국 서버): https://cran.yu.ac.kr/
* R studio: https://posit.co/download/rstudio-desktop/

### Conda에서 (Jupyter Notebook/Lab)에서 사용
1. Miniconda / Anaconda 설치: https://www.anaconda.com/docs/getting-started/miniconda/install#windows-command-prompt
2. 환경 만들기
    * 직접 만들기
        ```bash
        conda create -n r_env -c conda-forge r-base=4.4 r-irkernel -y
        conda activate r_env 
        ```
    * 또는 yaml파일로 세팅
        ```bash
        conda env create -f environment.yml
        ```
3. R 실행하기
    ```bash
    R
    ```
4. Jupyter로 실행
    ```bash
    conda install jupyter
    jupyter
    ```

## 기본 코드 알아보기
### 패키지 불러오기
* 자주 사용하는 패키지: `ggplot2`, `dplyr`
```R
install.packages("패키지이름")
library(패키지이름)
update.packages(ask = F) # 추가 질문없이 모든 패키지 버전 업데이트
remove.packages("패키지이름") # 패키지 삭제
```
### Directory 위치
```R
getwd() # 현재 내가 사용하고 있는  Directory 확인
dir.create("Day1") # 새로운 하위 Directory 만들기
setwd("Day1") # 새 Directory에서 작업하기
```
### 패키 또는 함수 사용 도움말
```R
help(패키지명/함수명) # 또는
?패키지명/함수명

## 예시
help(stats)
?barplot
```
