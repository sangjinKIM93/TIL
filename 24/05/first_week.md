# 새롭게 배운 내용


## setCustomSpacing
  - stackView에서 특정 뷰 이후부터 spacing이 적용될 수 있게 할 수 있다.

 <br><br><br>

## CompositionalLayout

- **NSCollectionLayoutItem**
    - 가장 작은 단위의 cell
    - container 안에서 width, height를 차지함

- NSCollectionLayoutGroup
    - item을 담는 container
    - 말 그대로 어떻게 lay out 할지 결정
    - item을 상속받기 때문에 item처럼 쓸 수 있다.

- **NSCollectionLayoutSection**
    - group을 담는 container
    - header, footer를 가질 수 있음
    
- NSCollectionLayoutBoundarySupplementaryItem
    - header, footer를 추가하기 위해서 필요한 객체

<br><br>

### 의문

“section이 여러개의 group을 포함할 수 있다면 group으로 다양한 layout을 표현할 수 있을 것 같은데 왜 여러개의 section을 쓰는거야?”

- group을 여러개 → 같은 데이터, 다양한 layout
- section을 여러개 → 다른 데이터

<br><br>

“collectionview layout 안에 collecitonview를 넣을 수 있을까?”

- 가능은 하겠지만 좋은 접근이 아니다.
