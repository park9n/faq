- https://www.netmanias.com/ko/
- https://www.netmanias.com/ko/?m=view&id=techdocs&no=5138
- https://www.netmanias.com/ko/?m=view&id=blog&no=5344&tag=80&page=8
- https://www.slideshare.net/neelkris/call-processing-and-handovereng

### Terminology
- SAE (System Architecture Evolution) : Core network architecture of 3GPP's LTE wireless communication standard.
  - https://en.wikipedia.org/wiki/System_Architecture_Evolution
- EPS (Evolved Packet System) = EPC (Evolved Packet Core, 코어망) + LTE RAN (Radio Access Network, 무선망)
  - EPC : 무선 인터페이스와는 관련이 없지만 전체적인 광대역 이동통신 (Mobile Broadband) 네트워크를 제공하기 위하여 필요한 기능들, 예를 들면 인증, 과금, End-to-End 연결 형성 등과 같은 기능들을 담당
    - MME (Mobility Management Entity) : 제어 평면 (Control Plane)을 다루는 노드
    - S-GW (Serving Gateway) : 사용자 평면 (User Plane)을 다루는 노드
  - RAN : 무선과 관련된 모든 기능을 담당
    - eNBs (evolved Node-B, 기지국) : 논리적인 노드, 한 개 셀 혹은 여러 개 셀의 모든 무선 관련된 기능들을 담당, EPC와 연결 (https://en.wikipedia.org/wiki/ENodeB)
      - OAM (Operations, Administration and Management) : https://en.wikipedia.org/wiki/Operations,_administration_and_management
      - CPS (Call Processing Software)
        - ECB (Control Subsystem) :
        - EDB (Data Subsystem) :
- UE (User Equipment) ↔ eNB ↔ EPC

- BTS (Basestation Transceiver System) : 기지국
  - DU (Digital Unit) : https://cy.cyworld.com/home/23611704/post/3677651
  - RU (RF Unit)
- LSM (LTE System Manager)
- NMS (Network Management System, 망 관리 시스템) : 장애 관리 및 운용 관리를 위한 장비
- DSP + System S/W (OAM + CALL) = DU
- KDDI : Japanese telecommunications operator https://www.kddi.com/english/
  - Japan’s mobile market is dominated by three major operators – NTT DoCoMo, KDDI and Softbank Mobile.
  - https://www.google.co.kr/search?newwindow=1&hl=en&sxsrf=ALeKk00dBh3Qdyl3L0CR7fNsWORqetFfAw%3A1585575987648&ei=M_iBXt2NJ5r6wQO0t4CgAQ&q=Japanese+Telecommunications+Companies&oq=Japanese+Telecommunications+Companies&gs_lcp=CgZwc3ktYWIQAzIECCMQJzIFCAAQzQI6BAgAEEc6BwgjELACECdQ0_8CWKejA2DxpgNoAHABeACAAZkBiAHoBZIBAzAuNZgBAKABAaoBB2d3cy13aXo&sclient=psy-ab&ved=0ahUKEwid84fsqsLoAhUafXAKHbQbABQQ4dUDCAs&uact=5
- Handover :
