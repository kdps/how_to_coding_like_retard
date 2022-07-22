# 저능아같이 코딩하는 방법 (Shit-code-art)

https://dev.to/seek4samurai/art-of-shit-coding-4f5p

https://www.reddit.com/r/PHP/comments/1lpgqk/worst_practices/

### 모든 변수명을 is와 조합하여 사용하라.

is와 조합하여 변수명을 완성하면 가독성이 엄청나게 개선된다. (isImageSize isMulti isMore) has contains to와 같은 겉치레는 필요없다.
구글링으로 안나오는 이름이면 더욱 환상적이다.


### 머릿글자를 딴 값을 사용하라.

머릿글자를 딴 값을 사용하면 당신의 프로그램의 데이터를 난독화 시킨것과 동일한 효과를 가져올 것이다. 그 누구도 알 수 없는 값들을 다시 설명하기 위하여 저능한 명세서 위주의 업무 프로세스를 필요로 하게 될것이고 당신의 업무는 몇배 이상 느려지게 될 것이다. `C P R CWO CRO CPQ` 이 단어들을 보고 무슨 뜻인지 알 수 있는가? 그 누구도 알 수 없다.


### Flag를 적극 활용하라.

모든 if문 사이에 flag의 Boolean 값을 변경하는 코드를 삽입하여 가독성을 더욱 떨어뜨리고 프로그램이 체계적으로 구조화 될 가능성을 배제시키게 될 것이다. flag를 더욱 훌륭하게 사용하는 방법은 반환값의 유효여부(TREU FALSE)와 메시지를 flag로 사용하는것이다. 행위의 종류 (게시글의 데이터를 가져오거나 댓글 목록을 가져오는것 따위의 행위들)를 판단하는데 flag를 사용해도 좋다. flag로 인하여 수십 수백개의 if문들에 수십개의 중첩된 if문으로 만들어진 아름답고 간결한 코드를 보게 될 것이다. 이제 당신은 죽어도 좋다. 이렇게 아름다운 코드를 작성했으니 살아있을 가치도 없다.


### 동사를 일관성 없이 사용한다.

```
del_comment, delete_document
```


### 값의 유형을 표기하지 않는다.

어떠한 이름을 사용하였는지 어떠한 값을 반환하는지 예측하기 어렵게 하여 모든 업무에 명세서를 활용할 수 있도록 하여라 줄인 이름을 사용해도 되고 실제 의미와 전혀 관계가 없는 단어를 사용해도 된다. 코드 짜기도 바쁜데 변수 이름 짜는데 시간을 쓰는것은 바보같은 방법이다. memo, content, title을 적극 사용하여라 'as 위치'를 의미하는 변수 이름을 지어보자. 'as_content' 어떤가? 얼마나 심미있고 직관적인가? 그 누가 봐도 as센터 위치를 의미하는 변수 이름이다.


### 변수 이름에 반환값들을 집어 넣는다.

변수 이름에 반환값들을 넣으면 변수이름만 보고 무슨값이 나오는지 알기 쉬워진다, 예로 두개를 보여주도록 하겠다. `use_truefalse, use_yn` 심미적으로도 아름답고 간결하다. 반환값의 유형이 바뀌면 어떠한 값이 나올지 예측하는데 방해요소로 되기는 하겠지만 무슨 상관인가? 변수 값은 use_yn인데 반환값은 true, false가 되는 상상을 해보자. 당연히 반환값이 y, n으로 생각하고 코드를 짰지만 반환값은 true, false라서 두번을 작업했는가? 아니면 무슨 값이 나오는지 확인하기 위하여 동료에게 계속 묻거나 일일이 반환값을 확인하는 작업을 하였는가? 그것이 바로 프로그래밍이다. 반환값을 대소문자 상관없이 사용해도 좋다. 반환값 이름이 areyoucrazy_yn인데 실 반환값은 Y, N이면 더욱 좋다. 그냥 areyoucrazy_YN_fucker로 쓰는게 좋지 않은가?


### 캡슐화를 피하고 복사하고 수정해서 사용한다.

Ctrl+C, Ctrl+V를 하면 되는데 뭐하러 클래스를 만들어서 사용하는가? 같은 기능을 하는 함수의 기능을 수정할 시 수정할 코드의 범위가 기하급수적으로 늘어나 기능을 수정하는데 장애가 생기지만 캡슐화를 하는데 버리는 시간은 누가 갚는가? 확인할 필요가 없는 코드때문에 코드 길이가 길어져 코드 리딩에 방해가 된다면 접어서 보아라. 


### 들어오는 모든 파라미터들을 생성자나 파일에서 한번에 받아온다.

생성자에서 모든 입력값을 받아와서 사용하면 코드길이도 줄어들고 변수 이름에 일관성이 생긴다. 함수에서 어떤 파라미터를 사용하는지 파악하기가 힘들어지지만 코드길이가 줄어든다. 함수에 일일이 요청 예제 URL을 붙이고 얼마나 재미있는가? 아니면 아예 반환값 전체를 extract하여 사용하여도 좋다. 이러한 행위는 많은 보안이슈를 가지고 오겠지만 편리성이 중요하다.


### use, has와 같은 동사를 피하고 is만 사용한다.

변수의 동사를 is만 사용하면 어떠한 값을 담는지, 무슨 뜻을 내포하고 있는지 알기 어려워진다. 쉽게 코딩하면 그게 코딩인가? 그냥 명세서에 무슨 역할을 하는 변수인지 의미를 적으면 된다 서류보고 코드보고 서류보고 코드보고 얼마나 쉬운가? has_video와 같은 바보같은 변수 이름은 피해라 is만 사용하면 된다 is_video를 보면 무슨 의미로 생각되는가? 비디오인지 판단하는 변수이름으로 생각될 것이다. 사실은 비디오를 포함하는지를 확인하는 변수 이름이다. 변수가 무슨 역할을 하는지 확인하는 행위들은 마치 멘사 문제를 푸는것과 동일한 기분을 들게 할 것이다. 이것은 놀이이고 탐구행위이다. `시간을 엄청나게 소비하는` 놀이이고 탐구행위


### 모든 반환값을 숫자로 정의하고 숫자에 대칭되는 의미를 명세서에 작성한다.

나는 PHP를 사용하지만 반환값은 꼭 숫자로 한다, 내 코드는 특별해서 남이 못알아보게 해야한다. 영어 단어를 사용하면 직관적으로 확인할 수 있지만 숫자를 사용하면 내 프로그램은 특별해진다. 숫자가 싫다면 단 한자리 영단어를 사용하자 Community는 C로 Process는 P로 사용하듯이 사용하면 된다.


### Boolean 값으로 표현할 수 있는 모든것을 String 값으로 표현하라

True, False 값으로 표현할 수 있는 모든것을 String (T, F, true, false)로 표현하라. 반환값에 일관성이 없을수록 좋다.
어떤곳에서는 반환값을 true로 다른 어떤곳에서는 TRUE 다른 어떤곳에서는 t 다른 어떤곳에서는 True로 하는식이면 더욱 더 좋다.


### 캡슐화 대신 if문을 중첩해서 사용하라.

뭐하러 클래스나 함수를 사용하는가? 중첩 if문을 사용하면 코드가 한눈에 보인다. 가독성도 안좋아지고 유지보수도 힘들어지지만 한눈에 보이는게 더 중요하다.

### 어디에 쓰는 변수인지 기입한다

버튼에 쓰면 button으로 쓰고 텍스트에 쓰면 text로 사용하라. 그냥 변수명을 사용하는 의미 자체가 없지만 어디에 사용하는지는 알 수 있으니 그 자체로 변수명을 쓰는 의미가 있지 않는가? 이런 변수를 사용하는 사람들에게 추천하는 변수명이다. dead_mother는 어떤가? 사망한 애미한테 사용할 수 있는 변수다.
