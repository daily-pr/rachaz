#### ✅ React Native에서 Animation을 구현할 때에는 Animated라는 객체 사용!

```
import React, {useRef} from 'react';
import {Animated} from 'react-native';

function Sample() {
  const animation = useRef(new Animated.Value(1)).current;
}
```

Value를 만들 때는 **`useRef`** 를 사용해야 한다. <br>

**특정 값을 컴포넌트 생성 시에 설정**하고, 
**컴포넌트가 사라질 때까지 재사용**하고 싶은 경우에도 이와 같이 `useRef` 사용!
<br>

Value의 생성자 함수 인자에는 초깃값을 넣어준다.<br>
그리고 이 값을 리액트 컴포넌트의 스타일에 적용할 때는 아래와 같이 사용한다. 

`<Animated.View style={{opacity: animation}}></Animated.View>`

Animated. 뒤에 사용하고 싶은 리액트 네이티브 컴포넌트의 이름을 넣어주면 된다.

컴포넌트의 투명도 값을 animation이 가리키고 있는 값으로 설정했다.<br>
추후 이 값을 변경할 때는 **`Animated.timing`** 이라는 함수를 사용한다.

```
Animated.timing(animation, { 
  toValue: 0, // 어떤 값으로 변경할지 - 필수
  duration: 1000, // 애니메이션에 걸리는 시간(밀리세컨드) - 기본값 500
  delay: 0, // 딜레이 이후 애니메이션 시작 - 기본값 0
  useNativeDriver: true, // 네이티브 드라이버 사용 여부 - 필수
  isInteraction: true, // 사용자 인터랙션에 의해 시작한 애니메이션인지 지정 - 기본값 true
  easing: Easing.inOut(Easing.ease), // 애니메이션 속서 변경 함수 - 기본값 Easing.inOut(Easing.ease)
}).start(() => {
  // 애니메이션 처리 완료 후 실행할 작업
})
```
