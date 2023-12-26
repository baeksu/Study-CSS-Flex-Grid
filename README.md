## 개요

인프런 1분코딩님의 [CSS Flex와 Grid 제대로 익히기](https://www.inflearn.com/course/css-flex-grid-%EC%A0%9C%EB%8C%80%EB%A1%9C-%EC%9D%B5%ED%9E%88%EA%B8%B0/dashboard) 강의를 보면서 Flex, Grid 를 학습하며 나오는 유용한 CSS 속성들을 기록해두고 다음에 활용하자.

구현한 내용을 README.md 에 정리해두고, 상세코드는 깃허브로 확인하자

---

## 💡유용한 링크

-   [특수문자 복사 링크](https://copychar.cc/)

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

---

## 💡입력창 만들기

입력창과 제출버튼이 flex 로 묶여있는 상황이다.

1. **flex-item** 들은 container 의 height 를 따라간다.

2. 입력창의 경우 화면을 늘리면 함께 늘어나는데, 이 때 사용하는 속성이 **flex: 1;** 이다. 만약에 버튼-item 에도 같은 속성을 적용해주면 균등한 너비를 차지하면서 늘어나게 된다.

<p align="center">
<img width="400" alt="image" src="https://github.com/baeksu/saveImage/assets/37931758/b9e50a6a-ba10-401e-aef1-395924ebc9fd">
</p>

---

## 💡bullet 리스트

**&lt;/li&gt;** 태그에 flex 를 적용하면 맨앞에 **∙**(닷) 이 사라지게 된다. 이때 원하는 bullet 리스트 이미지를 넣어준다.

이때 가상요소 **( ::before )** 의 **content** 속성을 이용하여 쉽게 bullet 리스트를 만들어 줄 수 있다.

<p align="center">
<img width="400" alt="image" src="https://github.com/baeksu/saveImage/assets/37931758/393a94b5-b513-423c-a064-0f9a78db1123">
</p>

---

## 💡message 리스트

메신져방에서 프로필과 메세지를 적을때 유용하게 사용할 수 있을듯!

-   flex-shrink 설정을 한 이유는 메세지 길이에 따라서 프로필 영역이 찌그러질 수 있는데, 이걸 방지하려고
-   img 태그 대신에 figure 태그와 background-image 속성을 이용하는 이유는 개발 요구사항에 따라 나뉘는듯, figure를 사용하면 디자인적으로 좀 더 다양한 요소를 활용할 수 있는듯 (캡쳐본처럼 이미지 위에 글자를 쓴다거나)

<p align="center">
<img width="400" alt="image" src="https://github.com/baeksu/saveImage/assets/37931758/5e48047c-0385-4e72-b68c-cca9d01bedae">
</p>

---

## 💡user 리스트 (프로필)

카톡 프로필 화면처럼 프로필과 상태메세지가 함께 나오는 화면에 유용할 듯. 너무 긴 글자는 **"..."** 으로 생략할 수 있게

세가지 css 속성만 기억해두자

```
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
```

<p align="center">
<img width="300" height="300" alt="image" src="https://github.com/baeksu/saveImage/assets/37931758/4d2aeb04-1582-49a9-aba3-0dcd352fd47d">
</p>

---

## 💡modal 창

여긴 뭐... 가장 바깥 div 에 flex를 주고 아래 두가지 속성 걸어줘서 중앙에 배치하는거 기억해두면 될듯. 그리고 **vw** 단위 활용하면 창 크기 변화에 따른 모달창 변화도 자연스럽게 해주는거도 기억하면 좋을듯

-   align-items: center;
-   justify-content: center;
<p align="center">
<img width="300" height="300" alt="image" src="https://github.com/baeksu/saveImage/assets/37931758/c06b252a-4c35-4e55-8ddf-169d13ebf1cd">
</p>

## 💡카드 list

여기서 기억해둘거는 **flex-wrap: wrap;** 속성을 통해서 카드 아이템들을 여러줄에 걸쳐서 보여주도록 하고

**box-sizing: border-box;** 이걸 기억을 좀 해두자, 컨텐츠 영역 + 패딩 + 테두리 영역을 모두 포함해서 배치를 해주는게 디자인 할 때 판한듯

> 이걸 안해주니까 공간이 애매하게 잡혀서 원하는 배치가 안되서 한참 고민했음... 어렵다 어려워 css의 세계

<p align="center">
<img width="300" height="300" alt="image" src="https://github.com/baeksu/saveImage/assets/37931758/5d8deffb-ae91-4f92-adad-4bb07371795b">
</p>
