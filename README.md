# 최호용

## <span style="color:yellow">**2023-05-04**</span>

<br>

## **그래프**

```
month <- 1:12
late <- c(5,8,7,9,4,6,12,13,8,6,6,4)
late2 <- c(4,6,5,7,8,10,2,8,4,12,3,20)
plot(month,
     late,
     main='지각생 통계',
     type='b',
     lty=1,
     col='red',
     lwd=,
     xlab="Month",
     ylab='Late cnt')
lines(month,
      late2,
      type='b',
      col='blue')

```

![1111](https://user-images.githubusercontent.com/102167336/236180697-5cacff96-385f-41f9-8d6f-48a291e6980c.JPG)


<br>

## **상자그림**

### 사분위수를 시각화하여 그래프 형태로 나타낸 것으로, 하나의 그래프로 데이터의 분포 등 다양한 정보 전달하여 단일변수 수치형 자료를 파악하는 데 자주 사용

<br>

## **예시1**

```
dist <- cars[, ]
boxplot(dist, main='자동차 제동거리')
```

![image](https://user-images.githubusercontent.com/102167336/236182217-774db837-cd1d-4982-b890-0eb459871046.png)

<br>

## **예시2**

```
boxplot(Petal.Length~Species,
        data=iris,
        main='품종별 꽃잎의 길이',
        col=c('green', 'yellow', 'blue'))
```

![image](https://user-images.githubusercontent.com/102167336/236183944-d72aec20-2a47-44b7-8061-8153be1cc98b.png)

<br>

## **산점도**

### 다중변수 데이터에서 두 변수에 포함된 값들을 2차원 그래프 상에 점으로 표한하여 분포를 관찰할 수 있도록 하는 도구

<br>

## **예시**

```
wt <- mtcars$wt
mpg <- mtcars$mpg
plot(wt,
     mpg,
     main='중량-연비 그래프',
     xlab='중량',
     ylab='연비',
     col='red',
     pch=19)
```

![image](https://user-images.githubusercontent.com/102167336/236186315-5084be7f-3b33-42bb-b5d8-8acdab936068.png)

<br>

## **그룹 정보가 2개 변수의 산점도**

```
iris.2 <- iris[,3:4]
levels(iris$Species)
group <- as.numeric(iris$Species)
color <- c('red', 'green', 'blue')
plot(iris.2,
     main='Iris plot',
     pch=c(group),
     col=color[group])

```

![image](https://user-images.githubusercontent.com/102167336/236191456-f699bcc9-8178-4f51-9092-e8857a588749.png)

<br>

## **데이터 분석 절차**

### 문제 정의/계획 -> 데이터 수집 -> 데이터 정제/전처리 -> 

### 데이터 탐색 -> 데이터 분석 -> 결과 보고

<br>



<br>

---
---

## <span style="color:yellow">**2023-04-27**</span>

### 19:51 도착 후 내용을 정리했습니다.

<br>

## **그래프**

### 데이터 입력

### ex) age.A <- c(1, 2, 3, 4, 5) age.B <- c(5, 4, 3, 2, 1)

<br>

### **합치기**

### ds <- rbind(age.A, age.B)

<br>

### **그래프 작성**

### barplot(ds, main = "제목", col=rainbiw(숫자), beside=T)

<br>

### **그래프 속성 (필요할 때 찾아서 쓰도록)**

### col=rainbow(), besode=True, legend.text=T, mfrow 

<br>

## **히스토그램**

### 히스토그램은 외관상 막대그래프와 유사합니다. 일반적으로 막대 사이에
간격이 있으면 막대그래프, 간격이 없이 막대들이 붙어 있으면 히스토그램이다.

### **data생성**

set.seed(1)

data=rnorm(100,170,5)

<br>

### **히스토그램 그리기**

hist(data)

<br>

### **히스토그램 그리기**

### a=hist(data

 ,breaks=seq(150,190,by=2)

 ,col="red"

,main="my histogram"

 ,xlab="height(cm)"

 ,axes=FALSE)

 <br>

 ### 

<br>

---
---

<br>

## <span style="color:yellow">**2023-04-05**</span>

강의 도착 전에 내용은 적지 못하였습니다.

<br>

## **데이터셋의 기본 정보 알아보기**

### dim(iris) - 행과 열의 개수 보이기
### nrow(iris) - 행의 개수 보이기
### ncol(iris) - 열의 개수 보이기
### colnames(iris) - 열 이름 보이기, names() 함수와 결과 동일
### head(iris) - 데이터셋의 앞부분 일부 보기
### tail(iris) - 데이터셋의 뒷부분 일부 보기
### str(iris) - 데이터셋 요약 정보 보기
### iris(,5) - 품종 데이터 보기
### levels(iris[,5]) - 품종의 종류 보기(중복 제거)
### table(iris[, "special"]) - 전체 보기

<br>

## **행별, 열별로 합계와 평균 계산하기**

### colSums(iris[,-5]) - 열별 합계
### colMeans(iris[,-5]) - 열별 평균
### rowSums(iris[,-5]) - 행별 합계
### rowMeans(iris[,-5]) - 행별 평균

<br>

## **함수들**

### t() - 행과 열 방향 전환
### subset(n, Speecies == 'm') - n중에 m만 출력

<br>

## **매트릭스와 데이터프레임의 자료구조 확인하기**

### class(iris) - iris 데이터셋의 자료구조 확인
### is.matrux(iris) - 데이터셋이 매트릭스인지 확인하는 함수
### is.data.frame(iris) - 데이터셋이 데이터프레임인지 확인하는 함수

<br>

## **매트릭스를 데이터프레임으로 변환**

### st <- data.frame(iris)
### head(st)
### class(st)

<br>

## **R에서의 입력과 출력**

### 프로그램 내에서 직접 데이터를 입력하는 경우, 화면에서 사용자로부터 입력받는 경우, 컴퓨터에 저장된 파일이나 인터넷상에 존재하는 데이터를 가져오는 경우 등이 있음.

<br>

## **print, cat**

### print는 하나의 값, 데이터 프레임, 2차원 배열 출력 

### cat은 여러 개의 값을 연결하여 출력. 2차원 배열은 출력 불가

## **작업 폴더**

### 자신이 읽거나 쓰고자 하는 파일이 위치하는 폴더

### R에서 어떤 파일을 읽으려면 그 파일이 위치한 폴더의 경로와 이름을 지정해야 함.

### setwd() - 쓰기

### 사실 어떤 언어든지 파일 읽고 쓰기는 똑같음.

<br>

---
---

## <span style="color:yellow">**2023-03-30**</span>

## **저장된 값을 보여주고 지우는 함수**

### ls() <- 저장된 변수를 모두 보여줌

### rm() <- 변수 하나를 지움

### rm(list) <- 변수 리스트를 지움

<br>

## **1차원, 2차원 자료**

### 1차원 자료 : 전 세계 국가의 GNP 같이 단일 주제에 대한 값들을 모아 놓은 자료 

### 2차원 자료 : 특수 주제에 대한 값을 모아놓은 자료

<br>

## **벡터 연산**

### 벡터와 벡터의 연산은 길이가 같아야 하고, 값의 종류가 같아야 가능하다. 

<br>

## **벡터에 적용 가능한 함수들**

### sum(), mean(), median(), max(), min(), var(), sd(), sort(), range(), length()

<br>

## **팩터**

### 범주형 변수에 사용되는데, 범주형 변수란 가질 수 있는 값이 미리 고정되고 또 알려진 변수를 말한다.

<br>

## **리스트**

### 자료형이 다른 값들을 한 곳에 저장하고 다룰 수 있도록 해주는 수단

<br>

## **2차원 자료의 저장**

### 매트릭스와 데이터프레임은 2차원 자료를 저장하기 위한 대표적인 자료구조

### 매트릭스와 데이터프레임의 차이점은 매트릭스에 저장되는 모든 자료의 종류가 동일하다


<br>

---
---

## <span style="color:yellow">**2023-03-23**</span>

## **도움말**

### 원하는 함수 앞에 ?sort를 입력하고 실행한다.

<br>

## **package Road**

### Packages 에서 원하는 패키지를 찾아서 install한다.

### 수업시간에는 cowsay를 사용

<br>

### **Sys.time()** <- 현재 시간 나오는 함수

### "2023-03-23 19:48:10 KST"

<br>

## **변수의 개념**

### <- 로 저장 
ex) a <- 10

### print(a)

### 10

### 산술연산은 파이썬과 비슷함.

## **변수명의 작명 규칙**

- 첫 글자는 영문자나 마침표로 시작하는데, 일반적으로 영문자로 시작

- 두 번째 글자부터는 영문자, 숫자, 마침표, 밑줄을 사용 가능

- 변수명에서 대문자와 소문자는 별개의 문자 취급

- 변수명 중간에 빈 칸을 넣을 수 없습니다.

- 저장될 수 있는 값은 숫자형, 문자형, 논리형, 특수 값이 있다.

## **벡터의 개념**

### 변수 <- (시작 숫자, 끝 숫자)

### **중요!** 1부터 시작함.

### R에서 제공하는 여러 개의 값을 한꺼번에 저장하는 기능으로,

### 일반적인 프로그래밍 용어로는 1차원 배열이라고도 함.

## **함수의 매개변수**

- 프로그래밍에서 함수의 입력값을 받는 변수를 매개변수라 함.

- 함수의 정의에 맞추어 매개변수를 입력하면 정의된 결과값을 얻을 수 있음.

<br>

함수는 외울 필요가 없다. 필요할 때 찾아서 쓸 수 있으면 괜찮다!!

<br>

---
---

## <span style="color:yellow">**2023-03-16**</span>

## **R언어의 특징**

- Python과 다르게 <span style="color:green">데이터 분석</span>에 특화

- 다양한 패키지 제공

- 무료 사용

- R Studio로 편리한 툴 제공

<br>

## **R을 배우는 이유**

- 4차 산업혁명: 인공지능과 빅데이터의 핵심 기술로 인식

- 시대적으로 점점 중요해질 스펙이며 우위를 점해야함.

- 데이터를 처리하고 가공하는 능력을 가져야 한다.

<br>

## **R Studio 설치**

### Chocolatey 이걸 활용하면 패치 버전을 한 번에 받을 수 있음.

### choco 명령어로 terminal에서 땡길 수 있음.

### 나중에 하고 지금은 R 다운로드함. easy

<br>

## **R Studio 화면 구성**

### 시계 방향으로 소스 영역 -> 환경 영역 -> 파일 영역 -> 콘솔영역으로 구성

## **About R**

### ctrl + enter : Current Line Run

### ctrl + Alt + R : All Run

### ctrl + Alt + B : To Current Line Run

### Working Delectory 설정

<br>

## **연산**

### n:m -> n+1 ~m 까지 (배열)

### print() 

### 

<br>

## **패키지**

부터 다음주에

### 각종 메뉴, 창에 대해 설명해주셨음. ppt 참고



<br>

---
---

## <span style="color:yellow">**2023-03-09**</span>

### 일요일까지 정리를 해서 올리면 월요일에 확인을 할 것이다.

### README파일을 정리해서 수행평가를 할 것이다.

### 3년 전에 만들어둔 설명 영상이 있는데 시간 나면 한 번씩 봐라.

### <span style="color:green">**VSCode Git Repository Create/Delete, Git Push**</span> 초반엔 방법 등에 대하여 설명하심.

### 노트를 깃에 넣는다는 느낌이다. 습관을 들여라. 잔디밭을 목표로 열심히 해라.

<br>

## **프로그래밍이란?**

### 컴퓨터에게 작업을 시키려면 작업의 순서와 방법을 논리적으로 

### 제시해야 하는데 이게 프로그래밍임.

<br>

## **단순 명령어, 복잡 명령어**

### 노트북을 예시로 들며 애플의 m1을 소개하며 복잡 명령어랑 단순 명령어 설명

### 열을 잡은 것에서 혁신적.

### <span style="color:green">**R**</span>언어는 데이터 관리의 특화되어 있다.

<br>

### **Pro Git 설명법이 있는데 pdf로 저장해서 모를 때 이걸 봐라** 

<br>