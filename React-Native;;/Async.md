#### Async란? [참고](https://springfall.cc/article/2022-11/easy-promise-async-await)

async function 선언은 AsyncFunction객체를 반환하는 하나의 비동기 함수를 정의 <br>
비동기 함수는 이벤트 루프를 통해 비동기적으로 작동하는 함수로, 암시적으로 `Promise` 를 사용하여 결과를 반환 <br>

`01` setTimeout 은 인자로 들어온 콜백 함수를 예약하기만 하고 바로 끝난다. <br>
`02` setTimeout 에 의해 기다리는 동작은 본래의 코드 흐름과는 상관 없이 따로따로 독립적으로 돌아간다. <br>
`03` 이렇게 따로따로 독립적으로 돌아가는 작업을 비동기 작업이라고 한다. <br>

