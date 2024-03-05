# React Hooks

## useState

``
const [state, setState] = useState(초기값);
``

setState를 사용해 state를 변경할때마다 컴포넌트는 랜더링

useState를 사용해 초기값을 받아올때 무거운 일을 해야할때 useState에 콜벡함수를 넣어주면 맨처음 랜더링 될때만 실행되게 할 수 있음

``
useState(()=>{ return heavyWorks();})
``


## useEffect

컴포넌트가 Mount, Update, Unmount 될때 특정작업을 처리할 코드를 실행시켜주고싶을때 시용

```
useEffect(()=>{
  //작업...

  return ()=>{
    // clean up 
  }
}, [value]);
```

## useRef

`` const ref = useRef(value)
``

변경시 렌더링을 다루지 말아야 하는 값을 다룰 때 사용

### 저장공간

State의 변화 -> 렌더링 -> 컴포넌트 내부 변수들 초기화

Ref의 변화 -> No 렌더링 -> 변수들의 값이 유지됨

State의 변화 -> 렌더링 -> 그래도 Ref의 값은 유지됨


