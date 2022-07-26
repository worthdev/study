# react 중점study 영역
JavaScript 는 typescript 를 적용하고
react 에서는 class 상속 받지 않고 hook 을 사용하므로 해당 사항을 공부해야함 (by 연구소장 최재웅 2022-07-21)
-> 인프런 처음만난 리액트에 있음

npm start

# Hooks
- useStatus
        // status  를 사용하기 위한 훅
        // 함수내에서 특정 변수의 값을 변경하여도 랜더링이 되지 않으므로 useStatus 를 사용하여 재랜더링해야함

- useEffect
   useEffect(() => {
        // 컴포넌트가 마운트 된 이후,
        // 의존성 배열에 있는 변수들 중 하나라도 값이 변경되었을 때 실행됨
        // 의존성 배열에 빈 배열([])을 넣으면 마운트와 언마운트시에 단 한번 씩만 실행됨
        // 의존성 배열 생략시 컴포넌트 업데이트 시마다 실행됨
        
        return () => {
                // 컴포넌트가 마운트 해제되기 전에 실행됨
        }
   }, [의존성 변수1, 의존성 변수2, ... ]);  

- useMemo
    const memoizedValue = useMemo( () => {
        return  
        }, [의존성 변수1, 의존성 변수2]
    );
        // 많은 처리가 필요한 결과를 저장(메모)후 필요시 사용
        // 랜더링이 일어나는 동한 실행함

- useMemo  는 값을 정의하고, useCallback 은 함수가 정의됨 