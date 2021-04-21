# TIL
오늘 새롭게 배우고 학습한 내용을 정리해두는 저장소 입니다.

# React

- env FAST_REFRESH=false

      → 맥북에서는 리액트 refresh 플러그인 사용 불가능,  항상 false 해야 에러 없이 실행된다.

- 맥북 M1칩에서는 node는 15버전 이상인 걸로 받아서 진행해야 create-react-app을 만들 수 있다.
- render가 될 때는 props나 status가 바뀌었을 때 렌더링이 된다.
- PureComponent를 사용하면 shouldComponentUpdate 함수를 자동으로 구현해주어 불필요한 렌더링을 막아준다.
- PureComponent의 단점은 배열이나 새로운 객체 생기면 진짜 바뀌었는 지 확인 하는데 어려워한다.
- PureComponent에서 알아차릴 수 있게 새로운 배열을 만들어주거나 새로운 객체인 경우는 옛날 내용을 펴서 나타낸다.

    ```jsx
    //PureComponent 예제
    import React, {PureComponent} from 'react';

    class Test extends PureComponent {
    	state = {
    		counter: 0,
    		string : 'hello',
    		number : 1 ,
    		boolean : true, 
    		object : {a: 'b' , c: 'd'},
    		array : [5,3,6]
    	}
    	
      //옛날 객체를 가져오지 말고 새로운 객체를 만들어라.
    	onClick = () => {
    		const obj = this.state.array[0].inside;
    		obj.push(4);
    		this.setState ({
    			object : {...this.state.object},
    		});
    	}
    }
    ```

- PureComponent 를 사용하면 성능 최적화 하기 좋다.
- Hooks 를 사용할 때에는 memo를 사용하여 성능 최적화를 한다.
