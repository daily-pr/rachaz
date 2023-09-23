#### Async란?

async function 선언은 AsyncFunction객체를 반환하는 하나의 비동기 함수를 정의 <br>
비동기 함수는 이벤트 루프를 통해 비동기적으로 작동하는 함수로, 암시적으로 `Promise` 를 사용하여 결과를 반환

```
function b() {
  console.log("b called!");
}

function a(another) {
  console.log("a started!");
  another();
  console.log("a ended!");
}
console.log(1);
console.log(2);
a(b);
console.log(3);
console.log(4);

----------------------------------------------------------------------


1
2
a started!
b called!
a ended!
3
4


```
