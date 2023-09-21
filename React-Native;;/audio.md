**[🎤 리액트에서 오디오 재생바 다루기](https://www.skypack.dev/view/react-native-simple-audio-player)** <br>

```
$ npm i react-native-simple-audio-player --save
$ npm i react-native-video --save
$ npm install @react-native-community/slider --save
```
<br>

```
import {AudioPlayer} from 'react-native-simple-audio-player';
```

<br>

```
import React from 'react';
import {View} from 'react-native';
import {AudioPlayer} from 'react-native-simple-audio-player';

const App = () => {
  return (
    <View
      style={{
        flex: 1,
        backgroundColor: '#313131',
        justifyContent: 'center',
      }}>
      <AudioPlayer
        url={'https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3'}
      />
    </View>
  );
};

export default App;
```
