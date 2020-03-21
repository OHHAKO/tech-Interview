## 하둡(Hadoop) 이론 정리

### 하둡 정의 
- 방대한 데이터를 분산처리하여 저장할 수 있도록 해주는 소프트웨어 프레임워크 입니다.
- 즉 하드웨어가 아닌 소프트웨어를 지칭합니다. 
- Java기반의 오픈소스 프레임워크 입니다.

### 하둡 분산처리 시스템의 특징
1. Data Recoverability(데이터 회복성): 일부 컴퓨터 동작 이상에도 시스템이 정상 동작한다. 
예전 분산처리 모델의 PF문제를 해결한다. Fault-tolerant라고도 부른다.
2. Component Recovery(구성요소 회복): 시스템 일부 구성요소에 이상이 생기고 다시 복구된 경우 
재시작 없이 시스템에 바로 관여해 작업을 수행한다.
3. Consistency(지속성): 시스템에서 작업이 수행되는 동안 시스템 컴포넌트에 문제가 생겨도 작업에는 영향을 주지 않는다.
4. Scalable(확장성): . 저장할 용량이 늘어나면 컴퓨터 추가 

### 하둡 구성 요소
- 사진 삽입

### 하둡 동작원리
- MapReduce, HDFS 두 가지 요소가 하둡 동작의 핵심입니다.
    - MapReduce: 대용량 데이터를 처리하는 분산 프로그래밍 모델 프레임워크 입니다.
    - HDFS: 하둡 네트워크에 연결된 기기에 데이터를 저장하는 분산형 파일 시스템 입니다.

### 하둡 탄생 배경 
- 기존의 분산 처리 시스템에는 확장성, PF문제가 있었다.
- 구글의 연구로 개발 시작
- GFS , MapReduce 기술 등장
- Apache 오픈소스 파운데이션 위에 GFS,MapReduce 기술을 끌어와 소프트 프레임워크를 만들었다. 그것이 하둡이다.

**용어 정리**
- 분산 처리 시스템: 여러개의 머신과 하나의 작업 사이 MPI를 사용하는 시스템
- MPI: Message Passing Interface
- Partial Failures: 분산 처리 시스템이 여러개의 컴퓨터를 사용하는 경우 일부 컴퓨터에서 동작 이상이 발생하면
분산처리 시스템이 동작 하지 않는 것
- GFS: Google File System
- HDFS: Hadoop Distributd File System. 
하둡 네트워크에 연결된 기기에 데이터를 저장하는 분산형 파일 시스템으로 안정적인 공유저장소, 데이터 저장소 이다. 
- MapReduce: 분산 프로그래밍 프레임워크, 분산 시스템
- 분산 프로그래밍: 
- Top-level
- Core Concept : 핵심개념

<br>

## 하둡 핵심 구성요소
### 1. HDFS (하둡 분산형 파일 시스템)
- 정의: 하둡 네트워크에 연결된 기기에 데이터를 저장하는 분산형 파일 시스템
- 저장 방식 특징:
    - 파일 등 데이터를 저장하면 다수의 노드에 복제 데이터를 함께 저장해 데이터 유실을 방지한다.
    - 저장하려는 파일은 특정 사이즈 블록으로 나뉘어 동일한 서버가 아닌, 분산된 서버 여러개에 저장된다. 
    - 블록사이즈는 기본적으로 64MB
    - 파일을 저장하거나 저장된 파일을 조회하려면 스트리밍 방식으로 데이터에 접근해야 한다.
    - 스트리밍 방식 데이터 접근이란, 파일을 순차적 스트리밍 방식으로 읽는 것이다.
    - 한번 저장된 데이터는 수정할 수 없으며 읽기만 가능하다. (데이터 무결성)
    - 수정은 불가능 하지만 파일이동, 삭제, 복사 하는 인터페이스를 제공한다.
- 아키텍처 사진 첨부 
- 설명

### 2. MapReduce 
- 정의: 대용량 데이터를 처리하는 분산 프로그래밍 모델 프레임워크
- 아키텍처 사진 첨부 
- 설명

--
**아래 사이트의 내용을 참고하여 작성된 글 입니다.**
- https://www.opentutorials.org/course/2908/17055
- https://m.blog.naver.com/PostView.nhn?blogId=acornedu&logNo=220957220179&proxyReferer=https%3A%2F%2Fwww.google.com%2F
- https://blog.acronym.co.kr/329
- https://12bme.tistory.com/70
- http://www.incodom.kr/%ED%95%98%EB%91%A1
- https://12bme.tistory.com/71?category=737765
- https://insightcampus.co.kr/hadoop01/
- https://eehoeskrap.tistory.com/219
- http://www.openwith.net/?p=597
- [HDFS 구조1](https://www.google.com/search?q=HDFS+%EC%95%84%ED%82%A4%ED%85%8D%EC%B2%98&sxsrf=ALeKk00XjKl06WayAyZThLsV8GRU7baKLw:1584778839953&source=lnms&tbm=isch&sa=X&ved=2ahUKEwiw9bWekavoAhWVZt4KHcMRCmgQ_AUoAXoECA0QAw&biw=526&bih=421#imgrc=u630ikwuwxbBHM&imgdii=DgMBWL8a8YJAwM)
- [HDFS 구조2](https://kimyhcj.tistory.com/181)




