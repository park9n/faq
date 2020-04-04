### What should I see first?

- 핸드폰이 어떻게 작동할까? : https://youtu.be/-PybfAJUOYY
- How is wireless communication possible? : https://youtu.be/dK5cRUCTDqE
- https://www.netmanias.com/ko/
- https://www.netmanias.com/ko/?m=view&id=techdocs&no=5138
- https://www.netmanias.com/ko/?m=view&id=blog&no=5344&tag=80&page=8
- https://www.slideshare.net/neelkris/call-processing-and-handovereng
- https://www.samsung.com/global/business/networks/
- https://www.samsung.com/global/business/networks/products/radio-access/access-unit/

### Terminology
- SAE (System Architecture Evolution) : Core network architecture of 3GPP's LTE wireless communication standard.
  - https://en.wikipedia.org/wiki/System_Architecture_Evolution
- 5G NR (New Radio) :
  - https://en.wikipedia.org/wiki/5G_NR

![image](https://user-images.githubusercontent.com/28881330/78424047-d09f3e80-76a5-11ea-9c52-66b4837b18da.png)

- EPS (Evolved Packet System) = EPC + LTE RAN
  - **EPC (Evolved Packet Core, 코어망)** : 무선 인터페이스와는 관련이 없지만 전체적인 광대역 이동통신 (Mobile Broadband) 네트워크를 제공하기 위하여 필요한 기능들, 예를 들면 인증, 과금, End-to-End 연결 형성 등과 같은 기능들을 담당
    - MME (Mobility Management Entity) : 제어 평면 (Control Plane)을 다루는 노드
    - S-GW (Serving Gateway) : 사용자 평면 (User Plane)을 다루는 노드
  - RAN (Radio Access Network, 무선망) = eNB : 무선과 관련된 모든 기능을 담당
    - **eNB (evolved Node-B, 기지국)** : 논리적인 노드, 한 개 셀 혹은 여러 개 셀의 모든 무선 관련된 기능들을 담당, EPC와 연결 (https://en.wikipedia.org/wiki/ENodeB)
      - DU (Digital Unit) = CDU (Cabinet DU, 19-inch shelf) : Can be mounted into indoor or outdoor 19-inch commercial rack (https://cy.cyworld.com/home/23611704/post/3677651)
      - RU (Radio Unit) = RRH (Remote Radio Heads) : Transceiver, Power Amplifier, and Filter. It transmits and receives traffic, clock information, and alarm/control messages to and from the CDU. The RRH has 4Tx/4Rx, 2Tx/4Rx or 2Tx/2Rx configurations supporting optic CPRI and can be installed on outdoor wall or pole.

- UE (User Equipment) ↔ eNB ↔ EPC
- BTS (Basestation Transceiver System) : 기지국
  - OAM (Operations, Administration and Management) : https://en.wikipedia.org/wiki/Operations,_administration_and_management
    - OSAB (OAM SON Agent Block)
    - PM (Performance Management)
    - FM (Fault Management)
    - CM (Configuration Management)
    - SNMP (Simple Network Management Protocol)
    - SwM (Soft Ware Management)
    - TM (Test Management)
    - Web-EMT (Web-based Element Maintenance Terminal)
    - CLI (Command Line Interface)
  - CPS (Call Processing Software) : Performs resource management of LTE eNB and call processing function in eNB
    - ECB (Control Subsystem) : Responsible for network access and call control functions
      - SCTB (Stream Control Transmission protocol Block)
      - ECMB (eNB Common Management Block)
      - ECCB (eNB Call Control Block)
      - CSAB (CPS SON Agent Block)
      - TrM (Trace Management)
      - EMCB (eNB MBMS Control Block)
    - EDB (Data Subsystem) : Responsible for user traffic handling
      - GTPB (GPRS Tunneling Protocol Block)
      - PDCB (PDCP Block)
      - RLCB (Radio Link Control Block)
      - MACB (Medium Access Control Block)

![image](https://user-images.githubusercontent.com/28881330/78451353-2254c280-76c0-11ea-8476-052ccd53f05b.png)

- NMS (Network Management System, 망 관리 시스템) : 장애 관리 및 운용 관리를 위한 장비
  - **LSM (LTE System Manager)** : Provides man-machine interface; manages the software, configuration, performance, and failures
- DSP + System S/W (OAM + CALL) = DU
- DSP : https://en.wikipedia.org/wiki/Digital_signal_processing
- KDDI : Japanese telecommunications operator https://www.kddi.com/english/
  - Japan’s mobile market is dominated by three major operators – NTT DoCoMo, KDDI and Softbank Mobile.
  - https://www.google.co.kr/search?newwindow=1&hl=en&sxsrf=ALeKk00dBh3Qdyl3L0CR7fNsWORqetFfAw%3A1585575987648&ei=M_iBXt2NJ5r6wQO0t4CgAQ&q=Japanese+Telecommunications+Companies&oq=Japanese+Telecommunications+Companies&gs_lcp=CgZwc3ktYWIQAzIECCMQJzIFCAAQzQI6BAgAEEc6BwgjELACECdQ0_8CWKejA2DxpgNoAHABeACAAZkBiAHoBZIBAzAuNZgBAKABAaoBB2d3cy13aXo&sclient=psy-ab&ved=0ahUKEwid84fsqsLoAhUafXAKHbQbABQQ4dUDCAs&uact=5
- UQ : https://namu.wiki/w/UQ%20%EB%AA%A8%EB%B0%94%EC%9D%BC
- Handover :
