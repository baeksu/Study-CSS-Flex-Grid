## 개요

인프런 1분코딩님의 [CSS Flex와 Grid 제대로 익히기](https://www.inflearn.com/course/css-flex-grid-%EC%A0%9C%EB%8C%80%EB%A1%9C-%EC%9D%B5%ED%9E%88%EA%B8%B0/dashboard) 강의를 보면서 Flex, Grid 를 학습하며 나오는 유용한 CSS 속성들을 기록해두고 다음에 활용하자.

구현한 내용을 README.md 에 정리해두고, 상세코드는 깃허브로 확인하자

---

## 💡메뉴 만들기

### 메뉴의 기능

1. 4개의 Item 이 각각 25%의 width 를 차지하고 있음
2. 임의의 Item 에 마우스를 올려두면 해당 Item 의 width 가 35%로 증가함
    - 이때 transition 속성을 통해 부드럽게 늘어나도록 애니메이션 적용
3. **&lt;/a&gt;** 에 **block** 속성을 적용하여 해당 Item 의 어느 영역을 클릭해도 링크 이동이 가능

<p align="center">
<img width="400" alt="image" src="https://github.com/baeksu/saveImage/assets/37931758/0ca2c1cd-dea8-46fd-9e6b-ba5fd7cdc123">
</p>

## 💡입력창 만들기

입력창과 제출버튼이 flex 로 묶여있는 상황이다.

1. **flex-item** 들은 container 의 height 를 따라간다.

2. 입력창의 경우 화면을 늘리면 함께 늘어나는데, 이 때 사용하는 속성이 **flex: 1;** 이다. 만약에 버튼-item 에도 같은 속성을 적용해주면 균등한 너비를 차지하면서 늘어나게 된다.

<p align="center">
<img width="400" alt="image" src="https://github.com/baeksu/saveImage/assets/37931758/b9e50a6a-ba10-401e-aef1-395924ebc9fd">
</p>
