# 저능아처럼 코딩하는 방법

## 1. 일관성 없는 변수 이름

### 1.1. 동사를 일관성 없이 사용한다.

```
del_comment, delete_document
```

### 1.2. 값의 유형을 표기하지 않는다.

`R: 코드 짜기도 바쁜데 변수 이름 짜는데 시간쓰기는 싫다`

`A: 어떠한 값을 내보내는지를 알 수 가 없으므로 명세서와 같은 문서를 작성하고 확인해야 한다`

```
discount -> 할인율
```

### 1.3. 변수 이름에 반환값들을 집어 넣는다.

`R: 변수 이름에 반환값을 넣으면 변수이름만 보고 무슨값이 나오는지 알기 쉬워진다`

`A: 반환값의 유형이 바뀌면 혼란을 부른다, 변수 이름은 ~YN인데 반환값은 true, false가 나오면 정상적인 변수 이름인가?`

```
use_yn, 반환값 = "Y, N"
```

### 1.4. 캡슐화를 피한다.

`R: Ctrl+C Ctrl+V를 하면 되는데 뭐하러 클래스를 만들어서 사용하냐?`

`A: 같은 기능을 하는 함수의 기능을 수정할 시 수정할 코드의 범위가 기하급수적으로 늘어난다`


### 1.5. 들어오는 모든 파라미터들을 생성자나 파일에서 한번에 받아온다.

`함수에서 어떤 파라미터를 사용하는지 파악하기가 힘들어진다`

### 1.6. use, has와 같은 동사를 피하고 is만 사용한다.

`어떠한 값을 담는지, 무슨 뜻을 내포하고 있는지 알기 어려워진다`

```
is_user, is_time
```

### 1.7. 모든 반환값을 숫자로 정의하고 숫자에 대칭되는 의미를 명세서에 작성한다.

`로우 언어를 하는것도 아니고 기밀자료라도 만드는가? 그냥 의미를 알 수 있도록 그냥 영어 단어로 된 값을 사용하여라`

```
if(return == -1) {
  msg("신청 기간이 아닙니다")
} else {
  msg("신청 기간입니다")
}
```

### 1.8. 캡슐화 대신 if문을 중첩해서 사용하라.

`캡슐화보다는 if문을 6개를 쓰는게 나아보이는가? 가독성도 안좋아지고 유지보수도 힘들어진다`
