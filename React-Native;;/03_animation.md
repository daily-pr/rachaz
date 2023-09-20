#### React Native에서 Animation을 구현할 때에는 Animated라는 객체 사용!

```
import React, {useRef} from 'react';
import {Animated} from 'react-native';

function Sample() {
  const animation = useRef(new Animated.Value(1)).current;
}
```

Value를 만들 때는 useRef를 사용해야 한다. <br>

특정 값을 컴포넌트 생성 시에 설정하고, 
컴포넌트가 사라질 때까지 재사용하고 싶은 경우에도 이와 같이 useRef 사용!
