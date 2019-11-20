# React_immer_study
리액트를 다루는 기술(개정판)에서 immer를 공부
## 작성한 코드 
- 폼에서 아이디 / 이름을 입력 시 하단 리스트에 추가.
- 리스트 항목을 클릭하면 삭제
### 기억해야 할 점
- immer는 사용 시 컴포넌트 최상단에 import produce from 'immer';를 작성해야 한다
- produce라는 함수는 두 가지 파라미터를 받는다. 첫 번째 파라미터는 수정하고 싶은 상태, 두 번째 파라미터는 상태를 어떻게 업데이트 할 지
  정의하는 함수이다.
- useState의 함수형 업데이트와 immer를 함께 쓰면 더 편하다.<br>
  ex)<br>       setForm(<br>
        produce(draft => {<br>
          draft[name] = value;<br>
        })<br>
      );<br>
    },<br>
    [form]<br>
  );<br>
<br>
==> 원래는 앞에 변경할 상태인 data를 붙여줘야 하지만 useState의 함수형 업데이트와 함께 사용하면 그냥 업데이트 함수만 써주어도 사용이 가능하다.
<br>
- immer를 사용하려면 리액트 프로젝트를 생성할 때 yarn add immer로 immer를 설치해주어야 한다.
