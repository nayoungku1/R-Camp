# Winter 2026 Big Data Analysis using R  
---
* Date: Jan 5, 2026 - Jan 14, 2026
* Instructor: [Prof. Sohn](mailto:jsohn@handong.edu)
* Venue: Handong Global University HDH 403
---

## R & R Studio 설치

### 직접 설치
* Cran을 통해 R 설치 (한국 서버): https://cran.yu.ac.kr/
* R studio: https://posit.co/download/rstudio-desktop/

### Conda에서 (Jupyter Notebook/Lab)에서 사용
1. Miniconda / Anaconda 설치: https://www.anaconda.com/docs/getting-started/miniconda/install#windows-command-prompt
2. 환경 만들기
    ```bash
    conda create -n r_env -c r r-essentials
    conda activate r_env 
    jupyter lab --no-browser
    ```

## 기본 코드 알아보기
### 패키지 불러오기
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