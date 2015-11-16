## Markdown 기본 문법 정리

#### 참고 링크

- [Markdown Basic on GitHub Help page](https://help.github.com/articles/markdown-basics/)
- [GitHub Flavored Markdown](https://help.github.com/articles/github-flavored-markdown/)
- [Writing on GitHub](https://help.github.com/articles/writing-on-github/)

### Markdown Basic on GitHub help page
---
아래 부분은 단순히 GitHub 에 있는 Markdown 도움 페이지를 단순 번역한 것에 불과하다. 보다 자세한 정보를 얻고 싶으면 해당 페이지에 가서 직접 보는 것을 추천한다. 이 페이지는 Markdown 언어에 익숙해 지고자 연습을 위해 작성된 페이지에 불과하다.

#### 기본 쓰기

##### 단락 만들기

단락을 만들고자 할 땐 그냥 Enter 로 행을 입력하면 된다.

```
이 문장은 A 입니다.

이 문장은 B 입니다.
```

##### 제목(크기) 표시하기

하나 또는 그 이상의 `#` 을 원하는 텍스트 앞에 붙임으로서 만들 수 있다. HTML Tag 와 같이 열고 닫을 필요는 없다. `#` 의 갯수에 따라 제목의 크기가 결정된다.

```
# 가장 큰 제목 (<h1> tag)
## 두번째로 큰 제목 (<h2> tag)
...
###### 여섯번째로 큰 제목 (<h6> tag)
```
제목의 경우 아래와 같이 모두 6 단계로 사용 가능하다.
# h1
## h2
### h3
#### h4
##### h5
###### h6

##### 인용문(Blockquotes) 사용하기

[인용문](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote)은 '>' 을 사용하여 나타낼 수 있다. 예를 들어 >test 는 아래와 같다.
>test

##### 텍스트 꾸미기

아래와 같이 흔히 말하는 **볼드** 와 *이탤릭* 효과를 만들 수 있다. 이탤릭체는 `*` 하나를 사용하여 감싸면 되고, 볼드는 `**` 와 같이 두개로 감싸면 된다. 예제는 아래와 같다.

```
*이것은 이탤릭체 입니다.*
**이것은 볼드 입니다.**
```

`*` 외에도 `_` 으로도 동일한 효과를 나타낼 수 있다. 이를 통해 볼드와 이탤릭을 모두 나타낼 수 있다. 만약 '** 모든 직원은 _반드시_ 5시 미팅에 참석해야 합니다.**' 와 같이 나타내고 싶다면 아래와 같이 사용하면 된다.
```
** 모든 직원은 _반드시_ 5시 미팅에 참석해야 합니다.**
```

#### 목록 사용하기

##### 순서없는 리스트
순서없는 리스트([unordered list](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul))는 `*` 또는 `-` 를 통해 나타낼 수 있다.

```
* Item1
* Item2
* Item3

- Item1
- Item2
- Item3
```
그러나 개인적인 테스트 결과 `*` 는 동작하지 않고 오직 `-` 만 동작하였다. 이는 나중에 다시 확인해볼 필요가 있다.(on Sublime Text2 w/Markdown Editing plug-in)

##### 순서있는 리스트
순서있는 리스트([ordered list](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol))는 숫자로 바로 표현이 가능하다.

```
1. Item1
2. Item2
3. Item3
```
그냥 Plain Text 로 쓰는 것과 별다른 차이가 없다.

##### 리스트 속의 리스트 표현하기
문서에 따르면 기본적으로 두칸의 공백을 통해 표현할 수 있다고 한다. 다만 나는 현재 Sublime Text2 상에서 [MarkdownEditing](https://github.com/SublimeText-Markdown/MarkdownEditing) Plug In 을 사용중인 상태라 그런지 공백을 통한 리스트 속의 리스트를 작성하기 어려운 점이 있었다.
또한 `Tab` 을 통해 들여쓰기가 가능하지만 숫자를 사용한 순서리스트의 경우 사용은 가능하나 자연스러운 동작은 되지 않았다.
자동화된 일반적인 텍스트 편집기의 경우 작성된 리스트에서 다음 리스트 입력을 위해 엔터를 입력하면 다음 리스트가 만들어 지고 그 상태에서 `Tab` 을 입력할 경우 하위 리스트를 만들 수 있었는데, 나의 경우 커서를 리스트 행의 맨 앞으로 이동 후 입력해야만 정상적으로 동작했다.(순서리스트만 해당) 

```
* 리스트 1
* 리스트 2
    - 리스트 2-1
    - 리스트 2-2
* 리스트 3
```

#### 코드 나타내기

##### 인라인 포맷
하나의 뒷따옴표(`` ` ``)를 사용하여 표현이 가능하다. 예제는 위에서 보아온 것과 같다. 하나의 줄은 뒷따옴표로 감싸주면 작성이 가능하다.
`이것은 하나의 뒷따옴표로 감싸진 문장입니다.`

##### 여러줄의 행을 가진 포맷
이는 세개의 연속된 뒷따옴표(`` ``` ``)를 사용하여 표현이 가능하다. 예제 역시 위에서 보아온 것과 같다. 단, 앞뒤로 문장을 감싸는 것이 아닌 반드시 개행(Enter)를 통한 문장을 위아래로 감싸주어야 한다.

```
이것은 세개의 뒷따옴표로 감싸진 문장입니다.
```

### GitHub Flavored Markdown
---
이 부분은 GFM(GitHub Flavored Markdown)의 문법이 기본 Markdown 과 얼마나 다른지를 설명하고 있다. 이 역시 서두에 밝혔듯 자세한 정보는 해당 페이지에 가서 확인하길 바란다. Markdown 문서를 작성하기 위한 하나의 공통된 표준으로 개인적으로 GFM 을 선택한 바, 이를 연습하기 위함에 불과하다. 그냥 예뻐서 선택했을 뿐, 난 당신이 이 페이지를 찾을거라곤 상상하지 않는다.

GitHub 는 GitHub 사이트내의 이슈, 코멘트, pull request 에 GFM 을 사용한다. Standard Markdown(SD)와는 조금 다르며, 몇몇의 추가적인 기능을 가지고 있다. 이 문서를 통해 이슈, 코멘트, pull request descriptions, task list 에 대해 더 자세히 알 수 있다.

#### 전통적인 Markdown 과의 다른 점

##### 단어내에 여러개의 언더스코어 `_` 가 있을 때
기본적인 Markdown 의 경우 언더스코어 (`_`)를 이탤릭체로 변경한다. 그러나 GFM 은 단어내에서 이를 아래와 같이 무시한다.

- wow_great_stuff
- do_this_and_do_that_and_another_thing.

만약 문장내에서 강조를 하고 싶다면, 언더스코어(`_`) 대신 `*` 를 사용하길 바란다. 혹은 단어와 단어사이를 언더스코어로 바로 연결하지 말고 한칸의 공백을 줄 경우 사용이 가능한 것을 확인했다.

- 공백이_ _있는_ _경우
- 공백이_없는_경우 
- 별표(`*`)를 *사용한* 경우
    - wow_*great*_stuff

위의 실제 Markdown 코드는 다음과 같다.

```
- 공백이_ _있는_ _경우
- 공백이_없는_경우 
- 별표(`*`)를 *사용한* 경우
    - wow_*great*_stuff
```

##### URL 자동연결
GFM 의 경우 표준 URL 을 자동으로 연결한다. 따라서 텍스트에 링크를 연결하려 하지 않는 이상 그냥 URL 을 입력하면 자동으로 링크가 연결된다.

```
http://github.com
```

##### 취소선(Strikethrough) 사용하기
표준 Markdown 에선 존재하지 않는 취소선이 GFM 에서 추가 되었다. 아래와 같이 사용할 수 있다.

```
~~취소선 사용하기~~
```

이는 곧 아래처럼 표시된다.
~~취소선 사용하기~~

##### 코드 블럭 나타내기
표준 Markdown 은 각 행별 앞의 4칸의 공백을 코드블럭으로 변환한다. GFM 역시 이를 지원하며 단지 `` ``` `` 로 감싸주면 된다. 이를 이용하면 별도의 들여쓰기(4칸)은 필요하지 않다. GFM 을 사용할 경우 코드블럭을 표시하기 위해 빈 줄이 필요하진 않지만, 더 쉽게 Markdown 언어를 보다 쉽게 읽기 위해 코드 블럭 전에 하나의 빈줄을 삽입할 것을 권고한다. 실제로 코드블럭 전에 빈줄이 있는 것과 없는 것은 결과에 차이가 없다.

    예제 코드:
    ```
    function test() {
      console.log("notice the blank line before this function?");
    }    
    ```   

목록을 사용하기 위해선 반드시 코드블럭으로 감싸져 있지 않은 8칸의 공백이 필요하다...라는데 어떻게 써먹는 건지 감이 오지 않는다.

##### 코드 강조하기(Syntax highlighting)
코드 문법의 강조는 아래에서 볼 수 있듯 위와 같은 코드블럭을 사용하되 첫번째 코드블럭의 끝에 어떤 언어의 코드인지를 명시해주면 된다.

    ```ruby
    require 'redcarpet'
    markdown = Redcarpet.new("Hello World!")
    puts markdown.to_html
    ```

이는 곧 아래와 같이 나타난다.

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

실제 이 Markdown 문서의 웹 미리보기에선 Ruby 코드로 적용되진 않지만, GitHub 에 추가한 후엔 정상적으로 보일 것으로 판단된다.
GitHub 는 [Linguist](https://github.com/github/linguist)를 언어의 감지 및 코드 강조에 사용하고 있다. 어떤 키워드로 어떤 언어를 지원하느지를 확인하려면 [the languages YAML file](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml)을 확인하면 된다.

##### 테이블 작성하기
단어의 나열을 통해 테이블을 만들 수 있으며 하이픈(`-`)을 첫번째 행에 두고, 나머지는 파이프(`|`)로 각각의 열을 구분한다.
예제 코드는 아래와 같다.

```
First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell
```

이를 실제로 적용하면 아래와 같다.

First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell

보다 아름다운 테이블을 위하여 추가적인 파이프를 각각의 끝에 추가해도 된다.

```
| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
```

결과는 위와 동일하다.
참고로 맨위에 있는 대쉬들은 헤더의 길이와 정확히 일치할 필요가 없다.

```
| Name | Description          |
| ------------- | ----------- |
| Help      | Display the help window.|
| Close     | Closes a window     |
```

또한 테이블 내에 링크, 볼드, 이탤릭, 취소선과 같은 Inline Markdown 적용이 가능하다.

```
| Name | Description          |
| ------------- | ----------- |
| Help      | ~~Display the~~ help window.|
| Close     | _Closes_ a window     |
```

이를 적용하면 아래와 같다.

| Name | Description          |
| ------------- | ----------- |
| Help      | ~~Display the~~ help window.|
| Close     | _Closes_ a window     |

마지막으로 콜론(`:`)을 통해 텍스트의 정렬을 맞출 수 있다. 콜론이 왼쪽에 있으면 왼쪽 정렬을, 오른쪽에 있으면 오른쪽 정렬을, 양쪽 사이드에 있으면 중앙 정렬을 의미한다.

```
| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |
```

이를 적용하면 아래와 같다.

| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |

#### HTML 사용하기

READMEs 와 issues, pull request 에 HTML Subsets 의 사용이 가능하다. 지원 가능한 모든 태그 리스트들은 [github/markup repository](https://github.com/github/markup)에서 확인할 수 있다.

### Writing on GitHub
------
Issues, comments, and pull request descriptions 들은 GitHub 에 보다 쉽게 내용을 작성하기 위해 몇몇의 추가적인 기능들과 함께 GFM 을 사용한다.

#### Markup

##### Newlines
GitHub 에 글을 쓰는 것의 가장 큰 차이점은 개행을 조정하는 것이다. Markdown 에선 하나의 단락을 만들기 위해선 감싸는 것이 어렵다. 우리는 이것을 통해 발생한 엄청난 수의 고의가 아닌 포맷 에러를 찾았다. GitHub 의 코멘트에선 당신이 보통 사용하는 실제의 개행과 거의 유사하다. 그냥 엔터치란 소리다.
아래의 두 개의 문장은 두 개의 단락으로 나뉘어져 표시된다.

```
장미는 빨간색입니다.
제비꽃은 파란색입니다.
```

실제는 아래와 같다.

장미는 빨간색입니다.
제비꽃은 파란색입니다.

##### Task lists




