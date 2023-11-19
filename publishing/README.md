## 이걸 만들어보면서 정리할 만한 내용들

### header

1. <strong>position: fixed, absolute;와 right: 0;</strong>을 함께 쓰면 해당 요소를 화면 width에 꽉차게 만들 수 있다.
2. rem은 root의 폰트사이즈에 따라 상대적으로 변하는 단위이다. root는 일반적으로 html을 의미한다고 한다.
3. width를 적용시키려고 하는 것 보다는 padding을 사용하는 것이 더 깔끔하게 css를 짤 수 있는 방법인 것 같다.
4. 텍스트를 구성하는 영역은 실제 텍스트와 leading영역이라는게 있는데, line-height는 leading영역을 조절하는 css이다.
5. 인라인 속성을 가지는 요소들을 미리 inline-block으로 만들어 놓고 쓰는 것은 대부분의 경우 편한 것 같다.
6. box-sizing은 요소의 전체 너비와 높이를 설정하는 css다. 박스의 크기를 어떤 기준으로 계산 할지에 대한 css라고 설명하면 더 쉬운 것 같다.
  - 기본값인 content를 사용하면 border를 제외한 크기가 요소의 크기가 된다. 따라서 border가 10이고 실제 width가 300이라면 화면에 표시되는 요소의 크기는 320이 된다. 그리고 화면에 그려지는 박스의 크기는 300이 된다.
  - border-box를 사용하면 border를 포함한 값이 요소의 크기가 된다. 따라서 border가 10이고 실제 width가 300이라면 화면에 표시되는 요소의 크기는 300이 된다. 그리고 화면에 그려지는 박스의 크기는 280이 된다.
7. @media는 반응형을 만드는데 많이 사용된다. max-width를 적용하면 작은 사이즈에 대한 값을 지정하는 것이고 min-width에 적용하면 큰 값에 대해 값을 적용하는 것이다.
8. :focus, :hover 를 사용하면 js없이 동적인 ui를 아주 쉽게 구현 할 수 있다.
9. transition은 보통 all .2s ease;와 같이 3가지 속성을 적용해서 사용한다. all을 적용하면 width, height 등 모든 속성이 변경 됐을 때 트랜지션이 일어나게 된다.
10. background: #fff url(./search_30.svg) 0.6rem 0.5rem no-repeat; 처럼 사용해서 이미지를 요소에 적용하는 방법도 있다.
11. .nav-links .nav-item:first-child와 같이 여러개의 형제 요소들 중 특정 요소에만 값을 적용하는 방법이 있다. 이것도 js 없이 많은 문제를 해결할 수 있도록 해준다.
12. border-top: 6px solid #ccc; border-left: 4px solid transparent; border-right: 4px solid transparent;을 통해 세모 모양을 만들 수 있다. 이런식으로 css만을 이용해서 특정 모양을 만들어 내는 것도 가능하다.
13. vh, vw는 화면에 보이는 크기의 비율을 의미한다. hegith가 1000px이라고 했을 때 100vh는 1000px이다. calc(100vh - 2.7rem)과 같이 사용하는 것도 가능하다.
14. <strong>.a:hover .b</strong>과 같이 사용하면 a에 hover가 됐을 때 b에 적용될 css를 적용시켜 줄 수 있다. 이게 진짜 개꿀 인듯.
 - 툴팁같은거 만들 떄 정말 유용하다. 태그의 구성은 a태그 안에 b태그를 넣어주면 위치도 바로 아래 쪽에 표시되도록 만들어 줄 수 있다.
15. white-space는 줄 바꿈과 관련된 속성이다. 기본인 normal은 무조건 줄바꿈을 넣고 줄바꿈 태그 같은게 안먹음. nowrap은 줄바꿈 태그 같은게 안먹는건 동일하지만 기본적으로 줄바꿈이 적용되지 않게 해서 쭉 길게 이거지게 만듦
16. &nbsp는 줄바꿈이 일어날 때 줄바꿈이 예쁘게 될 수 있도록 공백을 넣어줄 수 있는 문자다.
17. :not()을 사용하면 특정 클래스, css속성을 가지지 않는 요소에 css를 적용시킬 수 있다. 이것도 잘 쓸 수 있을 듯.


### sidebar

1. ul 같은거는 line-height를 전역으로 잡아 놓고 쓰면 좋다.
2. 여기서는 화면 크기에 따라서 media 쿼리를 사용해 크기를 조절해줬다. 이런거는 좋은 듯?
3. border-left: 0.25rem solid transparent;를 주고 active 클래스에는 border-left-color: black; 이런식으로 하는거 굉장히 좋은 것 같았다.