# CAN 통신 방식

## 1. CAN 이란?
 : Controller Area Network의 줄임말으로,  
 차량 내에서 호스트 컴퓨터 없이 마이크로 컨트롤러나 장치들이 서로 통신하기 위해 설계된 표준 통신 규격이다.

## 2. CAN의 장점
<li> 각 디바이스마다 각각의 입출력 선들이 연결되어 있는 것이 아닌
하나의 CAN 인터페이스만 보유하여 전체 비용과 용량 절감</li>
<li> 경제적이고 안정적인 네트워크 제공

## 3. CAN 통신 방법
<li> peer-to-peer(P2P) 네트워크 : 서버 클라이언트 개념이 아닌 동등한 계층 노드들이
서로 클라이언트와 서버 역할을 네트워크 위에서 동시에 하는 통신 방식이다.
<li> 하나의 CAN BUS에 여러 개의 디바이스들이 연결되어 있고, 이를 노드라 지칭한다.
<li> CAN 노드에서 데이터 전송 준비가 되면 CAN프레임을 네트워크에 작성한다.
<li> 다중의 노드가 으로 네트워크에 접근하는 경우
우선순위가 높은 디바이스(더 낮은 ID번호)가 먼저 네트워크에 접근해 메시지를 전송할 수 있다.
<li> 각각의 노드들은 자신이 원하는 ID값의 메시지만 받아들이고, 아니면 무시한다.

## 4. CAN 메시지구조
<li> ID (11bit 또는 29bit) : 각각의 노드를 식별할 수 있도록 함
<li> Data Length Code (4bit) : 데이터의 길이
<li> Data (8bit 이상, DLC에 명세된 만큼) : 데이터

## 출처
  <li> http://www.ni.com/white-paper/2732/ko/
  <li>http://www.fescaro.com/2016/10/can-%ED%86%B5%EC%8B%A0%EC%9D%98-%EC%9D%B4%ED%95%B4/
