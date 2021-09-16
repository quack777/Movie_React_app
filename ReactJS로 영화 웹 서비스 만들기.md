# ReactJS로 영화 웹 서비스 만들기

## #2 JSX & PROPS

### #2.0 Creating your first React Component

​	**componet**는 HTML을 반환하는 함수

​	**jsx**는 js안의 HTML. Component를 만들고 어떻게 사용하는지에 대한 것

​	react application은 한 번에 하나의 component만 rendering할 수 있다



### #2.1 Resuable Componets with JSX + Props

​	**jsx**는 component에 정보를 보낼 수 있다

​	react는 재사용 가능한 component를 만들 수 있다

​	component에서 component로, children component로 정보를 보내는 방법을 배울거야!

​	application에서 food component로 정보를 보내고 그런 다음에 food component에서 그 정보를 어떻게 사용하지에 대해서 배울거야

​	food component에 kimchi라는 value로 prop name을 줬어

​	food component에 fav라는 이름의 property를 kimchi라는 value로 준거야

​	father가 children에게 data를 어떻게 보낼까?

​	props란 이렇게 뭔든지 component에 넣게되는 것들

​	props는 어디로 갈까? argument로 가, food의 첫번째 argument



### #2.2 Dynamic Component Generation

​	웹사이트에 동적 데이터를 추가하는 방법

​	어떻게 object의  list를 가져오는지 보여줄거야, 오직 js의 object들만

​	그리고 funtion component, food component를 동적으로 rendering할거야

​	map이 하는 것은 rendering이야 하지만 array로부터 너에게  array를 줘

​	map은 array의 각 item에서 funtion을 실행하는 array를 가지는 js funtion이며, 그 funtion의 result를 갖는 array를 너에게 줘

​	map은 funtion을 취해서 그 funtion을 array의 각 item에 적용해

```react
friends.map(current => {
    console.log(current);
    return 0
})

/* 
dal
mark
lynn
japan guy
[0, 0, 0, 0]
```

 map은 array를 취하고 우리가 정확히 원하는 array를 반환해



### #2.3 map Recap

​	map은 각각 item 별로 funtion을 호출해

### #2.4 Protection with PropTypes

