#Redux

![image](https://user-images.githubusercontent.com/57666307/124376648-fcfb9d80-dce2-11eb-9457-f0fb159427e4.png)


Redux는 모든 state를 store에 저장합니다. 컴포넌트끼리 데이터 교류를 하지 않고, store을 통해 데이터 교류가 이루어집니다. dispatch로 state를 업데이트 하고, subscribe로 state 변동 시 view를 업데이트 시켜줍니다.

![image](https://user-images.githubusercontent.com/57666307/124376662-0e44aa00-dce3-11eb-94bf-9190922b16d3.png)


또한 View에서 Dispatcher로 Action을 보낼 수도 있습니다. Action이 Dispatcher로 데이터를 저리하는 동안 다른 Action이 들어오게 된다면, 새로 들어면 Action은 처리하고 있던 Action의 작업이 끝날 때 까지 대기하게 됩니다.

Model과 View가 양방향으로 데이터 교류가 되는 MVC 디자인 패턴과 달리 FLUX는 단방향입니다. 그렇기 때문에 더욱 명료하게 개발 할 수 있게 됩니다.

# Redux의 3가지 원칙

## Single Source of Truth (하나의 진실의 근원)

Redux는 state를 저장하기 위해 한개의 store만 사용합니다. (이것이 FLUX 디자인 패턴과의 차이입니다. FLUX는 여러개의 store을 사용합니다.) 단일 state tree를 구성하게 되는데, 단일 state tree는 어플리케이션을 디버그하기 쉽게 만듭니다.

## State is read-only (state는 읽기 전용)

state를 변경할 수 있는 유일한 방법은 action을 넘겨 주는 방법입니다.

어플리케이션은 직접 state를 변경 할 수 없고, state를 변경하기 위해서는 action을 dispatch 해야 합니다.

## Change are made with Pure Functions (변화는 순수 함수로 만들어야 한다)

action을 dispatch하여 state를 변경합니다. action으로 state를 업데이트 하는 함수를 Reducer이라고 합니다. 즉, action을 어떤 변화가 있는지 정의하는 객체라고 한다면, Reducer은 action을 가지고 state를 변경시켜 줍니다.
