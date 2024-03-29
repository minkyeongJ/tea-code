# Scroll-to-bottom 기능

## 주제

채팅 환경에서 채팅 내용을 최하단으로 스크롤링 하는 기능을 구현합니다.

## 목표

Scroll to bottom의 원리를 이해하고, 기능 명세를 보면서 기능을 구현할 수 있습니다.

## 내용

채팅장을 화면에 2개를 두어 상호 채팅이 이루어지는 것 처럼 구현합니다.

## 역할

- 네비게이터: 민경
- 드라이버: 승미, 서희

## 기능 구현 명세

### 조건

- 채팅을 입력하면 포커스가 제일 최근에 보낸 채팅으로 이동합니다.

### 프로세스

1. 채팅 내용을 저장할 state를 선언합니다. 데이터타입은 아래와 같습니다.

```js
type chatList = {
  chatRoomName: string,
  content: string,
}[];
```

2. 채팅 전송 시 chatList에 입력한 값을 저장하는 함수를 작성합니다.

3. ChatRoom 컴포넌트에 채팅방 제목과, 채팅 데이터, 채팅 전송시 동작할 함수 3개를 props로 넘겨줍니다.

4. ChatRoom 컴포넌트에서 채팅방 제목 데이터와, 채팅데이터의 chatRoomName 데이터를 사용하여, 채팅방 주인일때와 아닐때 보여질 스타일을 구분합니다.

5. 채팅내용을 작성하고 전송 버튼을 누를 시 동작할 기능을 구현해주세요.
   5-1. input에 있는 값을 저장할 state를 작성해주세요.
   5-2. handelChatData 함수를 사용해 채팅 내용을 저장해주세요.

6. 최신 글에 스크롤되도록 기능을 구현해주세요.
   6-1. 채팅방의 높이를 알기위해 useRef를 사용해 DOM에 접근해주세요.
   6-2. ref와 useEffect를 사용하여 chatList가 새로 업데이트될때 스크롤을 최하단으로 이동하도록 구현해주세요.
