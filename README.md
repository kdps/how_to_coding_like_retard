# 저능아같이 코딩하는 방법





### 동사를 일관성 없이 사용한다.

```
del_comment, delete_document
```



### 값의 유형을 표기하지 않는다.

어떠한 이름을 사용하였는지 어떠한 값을 반환하는지 예측하기 어렵게 하여 모든 업무에 명세서를 활용할 수 있도록 하여라 줄인 이름을 사용해도 되고 실제 의미와 전혀 관계가 없는 단어를 사용해도 된다. 코드 짜기도 바쁜데 변수 이름 짜는데 시간을 쓰는것은 바보같은 방법이다. memo, content, title을 적극 사용하여라 'as 위치'를 의미하는 변수 이름을 지어보자. 'as_content' 어떤가? 얼마나 심미있고 직관적인가? 그 누가 봐도 as센터 위치를 의미하는 변수 이름이다.



### 변수 이름에 반환값들을 집어 넣는다.

변수 이름에 반환값들을 넣으면 변수이름만 보고 무슨값이 나오는지 알기 쉬워진다, 예로 두개를 보여주도록 하겠다. `use_truefalse, use_yn` 심미적으로도 아름답고 간결하다. 반환값의 유형이 바뀌면 어떠한 값이 나올지 예측하는데 방해요소로 되기는 하겠지만 무슨 상관인가? 변수 값은 use_yn인데 반환값은 true, false가 되는 상상을 해보자. 당연히 반환값이 y, n으로 생각하고 코드를 짰지만 반환값은 true, false라서 두번을 작업했는가? 아니면 무슨 값이 나오는지 확인하기 위하여 동료에게 계속 묻거나 일일이 반환값을 확인하는 작업을 해야하는가? 그게 프로그래밍이다.



### 캡슐화를 피한다.

Ctrl+C, Ctrl+V를 하면 되는데 뭐하러 클래스를 만들어서 사용하는가? 같은 기능을 하는 함수의 기능을 수정할 시 수정할 코드의 범위가 기하급수적으로 늘어나 기능을 수정하는데 장애가 생기지만 캡슐화를 하는데 버리는 시간은 누가 갚는가?



### 들어오는 모든 파라미터들을 생성자나 파일에서 한번에 받아온다.

생성자에서 모든 입력값을 받아와서 사용하면 코드길이도 줄어들고 변수 이름에 일관성이 생긴다. 함수에서 어떤 파라미터를 사용하는지 파악하기가 힘들어지지만 코드길이가 줄어든다. 함수에 일일이 요청 예제 URL을 붙이고 얼마나 재미있는가?



### use, has와 같은 동사를 피하고 is만 사용한다.

어떠한 값을 담는지, 무슨 뜻을 내포하고 있는지 알기 어려워진다. 쉽게 코딩하면 그게 코딩인가? 그냥 명세서에 무슨 역할을 하는 변수인지 의미를 적으면 된다 서류보고 코드보고 서류보고 코드보고 얼마나 쉬운가? has_video와 같은 바보같은 변수 이름은 피해라 is만 사용하면 된다 is_video를 보면 무슨 의미로 생각되는가? 비디오인지 판단하는 변수이름으로 생각될 것이다. 사실은 비디오를 포함하는지를 확인하는 변수 이름이다. 변수가 무슨열할을 하는지 확인하는 행위들은 마치 멘사 문제를 푸는것과 동일한 기분을 들게 할 것이다. 이것은 놀이이고 탐구행위이다. `시간을 엄청나게 소비하는` 놀이이고 탐구행위
'


### 모든 반환값을 숫자로 정의하고 숫자에 대칭되는 의미를 명세서에 작성한다.

나는 PHP를 사용하지만 반환값은 꼭 숫자로 한다, 내 코드는 특별해서 남이 못알아보게 해야한다. 영어 단어를 사용하면 직관적으로 확인할 수 있지만 숫자를 사용하면 내 프로그램은 특별해진다.



### 캡슐화 대신 if문을 중첩해서 사용하라.

뭐하러 클래스나 함수를 사용하는가? 중첩 if문을 사용하면 코드가 한눈에 보인다. 가독성도 안좋아지고 유지보수도 힘들어지지만 한눈에 보이는게 더 중요하다.
