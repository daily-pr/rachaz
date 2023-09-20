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
