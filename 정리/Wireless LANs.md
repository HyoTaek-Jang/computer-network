# IEEE 802.11 Architecture

Elements of wireless network
무선 랜에 접속하는 단말 : wireless hosts

base station(BS), access point라고 표현하기도 함 AP
무선으로 전송하는 신호를 모아서 전달하는 base station.

wireless link
무선을 통해 전달되는 링크.
유선은 전기적 신호가 가서 심플한데, 와이어리스는 다양한 형태가 있음.

## two types of wireless network

### infrastructure mode

호스트가 직접 소통하는게 아니라 AP를 통해 정보를 주고받는 구조.
다른 호스트에 전달하는것도 중앙에 base station을 통해 외부에 접속하는 구조.
handoff : 다른 쪽 서브넷으로 이동하는 것. BS나 AP를 중심으로 핸드오프가 진행됨.

### ad-hoc mode

임시로 갑작스럽게 생기는 현상 ad hoc
중앙에서 BS가 없는거임. 그래서 통신하려면 단말끼리 직접 전달. 혹은 노드가 릴레이 해주고 ㅇㅇ!
MANET 이동하면서 ad hoc!

## wireless networks

### ISM bands

multiple access prob : 두개 이상의 스테이션이 동시에 신호를 보내서 신호가 서로 충돌이 생겨서 알아볼 수 없는
무선랜 프리퀀시 영역을 나누고 각 구역마다 사용자를 지정해둠.
충돌없이 쓰도록 방통위에서 프리퀀시 밴드의 사용자를 지정해놓음.
매번 허가 받는게 복잡함. 그래서 공공이 아니고 특별한 용도면 허락 안받고 쓸 수 있음.

프리퀀시 밴드가 높아지면 반말이 더 많은 파워를 써야햠. 코스트도 비싸지고

왜 비싼 높은 프리퀀시를 쓰나!
낮은 프래퀀시 밴드는 자연과 비슷해서 간섭이 많은데 높으면 비싼대신 깔끔함.

적당한 2GHz (전자레인지랑 비슷함.)

유선에 비해 속도가 떨어짐. 802.11 a,b 이렇게 죽쭉 발전함.

Wi-Fi 5 -> 802.11ac
보통 11ac까지 지원함.

하나의 ap를 통해 구성되는 무선 wireless station의 집합 : Basic service set (BSS)
ap에서 인터넷 접속은 유선랜으로 빠르게!!

무선랜 기능이 많아도 LLC로 변환이 가능함.
우리는 AP를 통해 무선 유선을 넘어감.

ISM에서 프리퀀시가 겹칠 수 있음. 무선신호 충돌의 가능성.
AP는 중복안되게 만들어야함. 최대 AP 3개가 가능함.
AP가 채널 중에서 품질 좋은 놈을 하나 고름. 그리고 겹치지 않으면서 품질 좋은걸 또 고름..! 이런식으로 3개까지 ㅇㅇ!

채널 여러개 하는 이유. 다 주파수가 다름. 깔끔한 주파수를 찾으려고 ㅇㅇ!

---

와이파이 잡으면 뜨는게 AP가 운영하는 BSS의 이름임!
AP는 한번 동작하면 Beacon frame을 보냄
중간 단말이 비콘 신호를 받는거임.
패스워드를 부여했으면 입력하고 AP에 접속해서 메시지 받는거임.

association!!!
passive scanning : AP가 제공하는 정보를 수동적으로 받는!, 비콘 프레임을 보내는 주기를 기다려야함.
active scanning : BSS에 대한 정보를 다 받고 싶으면 probe packet을 보내고, AP가 받으면 비콘 프레임을 바로 받음. 이게 되려면 AP가 지원해야하는데 대부분 패시브 스캐닝이 사용됨.
