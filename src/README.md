Markdown 문법 정리
================

## Markdown 문법

1. Header

2. BlockQuote
> This is a first blockquote
> > This is a second blockquote
> > > This is a third blockquote

3. 목록
  * first
    * second
      * third

4. 코드
```java
public class HelloWorld{
    public static void main(String[] args){
        System.out.println("Hello World");
    }
}
```

5. 수평선
* * *
***
*****
- - -
--------

6. 링크
Link: [Google][googlelink]
[googlelink]: https://google.com "Go google"

7. 강조
*single asterisks*    
_single underscore_    
**double asterisks**    
__double underscore__    
~~cancleline~~    

8. image
<img src="/path/to/img.jpg" width="40%" height="30%" title="px(픽셀) 크기 설정" alt="RubberDuck"></img>

9. 줄바꿈
 * 줄바꿈 하기 위해선 문장 마지막에서 3칸이상 띄어쓰기    
   해야함

## 정리

마크다운은 기본문법만 알고있다면 일반 텍스트편집기에서도 손쉽게 작성이 가능한 마크업언어다.

## 충돌 해결하기

- 겁먹지 않기
- 에러코드 잘 읽기

## 되돌리기

### reset 이용
- reset
- good point: very easy
- bad point: disappear commit, push --force

### branch 사용해서 되돌리기
- commit 사라지지 않는다.
- good point: easy
- bad point: messy

### revert 사용
- good point: commit 사라지지 않는다.
- bad point: little hard

#### revert 여러개 되돌리기
- 최신 순서대로 revert를 반복 적용
- CLI -> git revert HEAD HEAD~1

### temporary storage of work in progress
- 브랜치1에서 일단(임시) 커밋을 한다
- 브랜치2로 체크아웃하고 볼 일을 본다
- 다시 브랜치1로 되돌아 온다
- 1의 작업을 이어서 마무리 짓는다
- 커밋 덮어쓰기 (commit --amend)를 한다
- (옵션) 필요하다면 (push --force)를 한다

#### stash 이용해서 같은 작업하기
- stash를 만든다
- 이때 새로운 파일이 있었다면 일단 인덱스에 추가한다
- 체크아웃 한다
- 되돌아온다
- stash를 pop한다
- 보통 커밋을 새로 생성한다

### rebase

#### 장점
- 깔끔한 트리

#### 단점
- 충돌 가능성이 더 높다
- 위험하다
- 이미 원격에 있는 브랜치를 rebase 하면 안된

### rebase test
rebase branch 추가

### etc
etc branch 추가
