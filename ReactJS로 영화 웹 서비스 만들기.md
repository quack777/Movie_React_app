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

​	각각 list내의 child는 unique한 key prop을 가져야 한다

​	이 말은 모든 react의 element들은 유일해야하고

​	너가 이들을 list 안으로 집어넣을때, 이녀석들은 유일성을 잃어버려

​	다시 한 번 말하면, react의 모든 element들은 다르게 보일 필요가 있어

​	image element는 alt prop이 반드시 있어야 함

​	우리가 원하는 props이 우리가 갖고 있는 props인지. 체크하는 방법이 필요



### #2.4 Protection with PropTypes

​	항상 점검할 필요가 있어, father componet로 부터 전달받은props가 우리가 예상한 props인지



## #3 State

### #3.0 Class Components and State

​	react componet는 어떻게 동작할까?

​	**class react component**는 return을 가지고 있지 않아, function이 아니기 때문이야, 보다시피 **render method**를 가지고 있다

​	class vs funtion

​	funtion component는 function이고 뭔가를 return해 그리고 screen에 표시돼, 

​	class component는 class야 하지만 react component로 부터 확장되고 screen에 표시돼 너는 그걸 render method 안에 넣어야만 해 

​	react는 자동적으로 너의 class component의 render method를 실행해

​	funtion component는 쉬웠는데, 왜 class component에 대해 이야기 해야하는거야?

​	class component가 가진 우리가 원하는 state라고 불리는 녀석 때문

​	state는 object이고 component의 data를 넣을 공간이 있고 이 데이터는 **변해**

​	react에서는 자동적으로 주어진 onClick을 가지고 있어 이것은 react masic이다

​	

### #3.1 All you need to know about State

​	만약에 우리가 setState funtion을  호출하면, react는 매우 똑똑해서 우리가 언제 setState를 호출할 지를 알고 또한 내가 view를 refresh하길 원하는걸 알고 render function을 refresh하길 원하는걸 알아

​	만역 너가 setState를 호출하면 react는 state를 refresh하고 또한 render function을 호출할거야

​	우리가 setState를 사용하지 않으면 새 state와 함께 render funtion이 호출되지 않을거야

​	매 순간 너가 set State를 호출할 때 마다 react는 새로운 state와 함께 render function을 호출할거야



### #3.2 Component Life Cycle

​	life cycle method는 기본적으로 react가 component를 생성하는 그리고 없애는 방법이야



### #3.3 Planning the Movie Component

​	

## #4 Making the movie

### #4.0 Fetching Movies from API

​	axios는 마치 fetch위에 있는 작은 layer야

​	async await을 하는 것은 우리가 기본적으로 javaScript에게 getMovies function에게 조금 시간이 필요하고 우리는 그걸 기다려야만 한다는 것을 말하는거야



### #4.1 Rendering the Movies

​	movies component는 state를 필요로 하지 않아 그래서 만약에 component가 state가 필요 없을 경우에는 이게 class component가 될 필요는 없어



### #4.2 Styling the Movies

### #4.3 Adding Genres

### #4.4 Styles Timelapse

### #4.5 Cutting the summary



## #5 Conclusions

### #5.0 Deploying to Github Pages

​	1.npm i gh-pages
​	2.package.json에 homepage 추가하기
​	3.scripts에
​	▷"deploy" : "gh-pages -d build"
​	▷"predeploy" : "npm run build"
​	→deploy를 호출하면 먼저 호출된다
​	4.npm run deploy
​	★Published

### #5.1 Are we done?

​	

## #6 Routing bonus

### #6.0 Getting Ready for the Router

​	네비게이션 -> react-router dom



### #6.1 Building the Router 

​	exact={true} 이면 오직 그 url일때만 렌더링 해줘 

​	exact는 이거 아니면 렌더링 안한다는 뜻



### #6.2 Building the Navigation

### #6.3 Sharing Props Between Routes

### #6.4 Redirecting 