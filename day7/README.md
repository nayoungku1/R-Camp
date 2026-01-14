# KoNLP설치하기

순서대로 따라하기! 

---

```r
install.packages("rJava")
install.packages("multilinguer")
multilinguer::install_jdk()
```

→ `multilinguer::install_jdk()` 실행 시, 1,2,3 중 `3` 입력 + enter

```r
install.packages("remote")
install.packages(c("hash", "tau", "Sejong", "RSQLite", "devtools", "bit", "rex", "lazyeval", "htmlwidgets", "crosstalk", "promises", "later", "sessioninfo", "xopen", "bit64", "blob", "DBI", "memoise", "plogr", "covr", "DT", "rcmdcheck", "rversions"), type = "binary")
remotes::install_github('haven-jeon/KoNLP', upgrade = "never", INSTALL_opts=c("--no-multiarch"),force = TRUE )
```

`scala-library-2.11.8.jar` 파일 다운로드 후, `C:\Users\user\AppData\Local\R\win-library\4.5\KoNLP\java`폴더로 옮기기

```r

library(KoNLP)
useNIADic()
extractNoun('데이터분석 교육 중입니다.')
```