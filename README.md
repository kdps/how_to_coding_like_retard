## 1. 일관성 없는 변수 이름

### 1.1. 동사를 일관성 없이 사용한다.

```
del_comment, delete_document
```

### 1.2. 값의 유형을 표기하지 않는다.

어떠한 이름을 사용하였는지 어떠한 값을 반환하는지 예측하기 어렵게 하여 모든 업무에 명세서를 활용할 수 있도록 하여라 줄인 이름을 사용해도 되고 의미와 전혀 관계가 없는 단어를 사용해도 된다. 코드 짜기도 바쁜데 변수 이름 짜는데 시간을 쓰는것은 바보같은 방법이다.

```
discount -> 할인율
```

### 1.3. 변수 이름에 반환값들을 집어 넣는다.

변수 이름에 반환값들을 넣으면 변수이름만 보고 무슨값이 나오는지 알기 쉬워진다, 예로 두개를 보여주도록 하겠다. `use_truefalse, use_yn` 심미적으로도 아름답고 간결하다. 반환값의 유형이 바뀌면 어떠한 값이 나올지 예측하는데 방해요소로 되기는 하겠지만 무슨 상관인가? 변수 값은 use_yn인데 반환값은 true, false가 되는 상상을 해보자.

```
use_yn, 반환값 = "Y, N"
```

### 1.4. 캡슐화를 피한다.

`R: Ctrl+C Ctrl+V를 하면 되는데 뭐하러 클래스를 만들어서 사용하냐?`

`A: 같은 기능을 하는 함수의 기능을 수정할 시 수정할 코드의 범위가 기하급수적으로 늘어난다`


### 1.5. 들어오는 모든 파라미터들을 생성자나 파일에서 한번에 받아온다.

`R: 생성자에서 모든 입력값을 받아와서 사용하면 코드길이도 줄어들고 변수 이름에 일관성이 생긴다. 하지만 코드 캡슐화는 하기 싫다.`

`A: 함수에서 어떤 파라미터를 사용하는지 파악하기가 힘들어진다, 이러한 코드들이 어떻게 작동하는지 확인하기 위해서는 요청 URL 예제가 필요할 것이다.`

### 1.6. use, has와 같은 동사를 피하고 is만 사용한다.

`R: 그냥 명세서에 적으면 되지 서류보고 코드보고 서류보고 코드보고 얼마나 쉬워?`

`A: 어떠한 값을 담는지, 무슨 뜻을 내포하고 있는지 알기 어려워진다`

```
is_user, is_time
```

### 1.7. 모든 반환값을 숫자로 정의하고 숫자에 대칭되는 의미를 명세서에 작성한다.

`R: 나는 PHP를 사용하지만 반환값은 꼭 숫자로 한다, 내 코드는 특별해서 남이 못알아보게 해야한다`

`A: 로우 언어를 하는것도 아니고 기밀자료라도 만드는가? 그냥 의미를 알 수 있도록 그냥 영어 단어로 된 값을 사용하여라`

```
if(return == -1) {
  msg("신청 기간이 아닙니다")
} else {
  msg("신청 기간입니다")
}
```

### 1.8. 캡슐화 대신 if문을 중첩해서 사용하라.

`R: 뭐하러 클래스나 함수를 사용해? 한눈에 보이니까 중첩 if문이 오히려 쉽잖아?`

`A: 캡슐화보다는 if문을 6개를 쓰는게 나아보이는가? 가독성도 안좋아지고 유지보수도 힘들어진다`

```
if (return == 1) {
  if (tar == 1) {
    if (gz == 1) {
    } else if (gz == 2) {
    }
  } else if (tar == 2) {
  }
}
```
