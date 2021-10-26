#### 🎪 css3 animation과 모션에 대해 스터디

- 참고 : 웹스토리보이즈
- mouse hover 연습 : https://ginny-choi.github.io/animation/html/mouseHover.html
- animation 연습 : https://ginny-choi.github.io/animation/html/animation.html

---

### mouse hover effect

- 첫번째 섹션. 이미지 안에 figcaption 수직 수평 정렬을 flex를 이용해서 맞춰줌
- 이미지를 담고 있는 박스에 배경색을 지정해두고 , 이미지에 투명도를 0으로 주면 그 배경색이 보인다.
- 가상 요소를 만들어서 텍스트를 담는 배경을 만들었듯이 가상요소를 활용하겠다는 생각을 잘 해볼것.

---

### animation

- css 속성이 많이 생겼으니 잘 참고할 것!
- nth-of-type() : 유형이 똑같은 자식들 선택 // nth-of-child() : 유형 상관없이 자식들 선택
- alternate : 방향을 앞으로 갔다가 뒤로 갔다가 순서대로 움직여줌 (normal & reverse 를 합친 상태) 계속 이어지는 효과.
- animation 은 속성이나 ease in 값만 조금 변경줘도 크게 다른 효과가 나기에 조금씩 조정 해보는 것이 좋다!

- animation: loading ease-in-out 1s 100; -> 1초동안 움직임. 100번만 실행
  - 🎯 animation-iteration-count(반복횟수설정) : number | infinite | inherit; 숫자 넣기도 가능하다 !
    숫자, 소수점 | 무한 반복(infinite) | animation-iteration-count : 2, 0, infinite; 처럼 다중 속성 가능
- 3d 효과를 내려면 원근점(perspective)을 표시하고 적용할 요소에 3d를 쓰겠다고 설정 해줘야한다.(transform-style: preserve-3d;)
- (애니메이션 움직임의 속도) : animation-timing-function:linear; 처음 속도와 마지막 속도가 일정

#### 3d cube animation

- translateZ 값이나 scaleY 값을 조정하여 박스가 늘어나는 효과를 줌
- 큐브 박스 top & bottom: X축 | left & right : Y축 | front & back : Z축
- 박스 위치에 맞는 축에 맞게 rotate 시켜서 3d cube를 만듬
- animation: bottom 4s 8s ease-in-out infinite; -> 4s : 움직임 시간 / 8s: delay 시간. 순서 기억하기🎭

---

#### wave animation

- 가운데 정렬을 할 때, position 으로도 가능하고 flex로도 가능한데, 차이점은 position은 영역이 안 잡혀서 백그라운드가 안들어간다.
- animation을 지정한 요소에 딜레이 값을 줘야하는데 다른 곳에 지정해서 원하는대로 안나왔다! 잘 보고 지정하기
- scss를 쓰는거면 css 문법보다 scss 문법을 사용하도록 ,, ex) .row:nth-child() -> .row{ &:nth-child(){} }

---

#### bar animation

🎯 컨텐츠 요소를 가운데 정렬하는 방법 중 하나는 포지션을 이용하는 방법이 있다 - left:0, top:0, bottom:0, right:0, margin:auto를 쓰면 가운데로 온다 - 🧩포지션을 사용하면 영역이 사라지는 단점이 있다.

- 높이를 살짝 조정 해줘도 다른 효과가 나니, 여러 곳 수정해보면 좋음
