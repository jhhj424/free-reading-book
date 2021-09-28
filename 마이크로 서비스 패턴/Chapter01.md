# 1장 모놀리식 지옥에서 벗어나라

육각형 아키텍처

- 헥사고날 아키텍처, 포트와 어댑터 아키텍처 라고도 불림
- 비즈니스 로직을 표현하는 내부 영역과 인터페이스 처리를 담당하는 외부 영역으로 나뉨
- 비즈니스 로직을 표현하는 내부 영역이 어댑터에 의존하지 않고 오직 내부 영역이 제공하는 포트에 의존하여 구현함

마이크로서비스의 볼륨을 어떻게 나누고 가져가야할지에 대한 고민

- 비즈니스적으로 중요한 도메인을 나눠라
- 비즈니스적으로 중요하다는 건 돈과 관련되어 있을 가능성이 높다

서비스 분리 시 DB 도 분리 해야하는 이유

- 서비스만 분리하고 같은 DB를 사용하면 결국 장애 격리가 안된다
    - B 서비스에서 큰 트래픽을 받아서 DB 에 장애가 나면 A 서비스도 먹통
- [https://sebalopezz.medium.com/monolith-to-microservices-event-driven-architecture-ff4284bf4ecf](https://sebalopezz.medium.com/monolith-to-microservices-event-driven-architecture-ff4284bf4ecf)