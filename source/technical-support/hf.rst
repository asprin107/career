Hyperledger Fabric
==================

CA, intermediate CA, Orderer, Peer등 Hyperledger Fabric 구성 담당. Blockchain에 대한 infra architecture 설계.

* CA : Root 인증서 생성(openssl) 후 각 노드에서 사용할 cert와 key를 생성. 필요한 경우 intermediate CA 구성.
* Orderer : Single / Multi-node 구성. Multi node의 경우 zookeeper, kafka base의 구성, raft-etcd를 이용한 leader election 구조의 Orderer 자체 구성 두 종류 지원.
* Peer : Organization, 권한 등에 대한 기본적인 설정, couchdb / leveldb 설정 지원.
* TLS : Hyperledger를 구성하는 각 요소들이 tls 통신하도록 설정.
* Explorer : Blockchain의 현재 블록과 상태를 한눈에 확인할 수 있는 서비스인 Hyperledger Explorer 서비스 구성 지원.
* prometeus/grafana : hyperledger node의 state를 확인 할 수 있도록 다양한 메트릭 정보를 제공하는 모니터링 구성.
