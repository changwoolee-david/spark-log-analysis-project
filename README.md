Spark Log Analysis 프로젝트
===========================

### 프로젝트 개요
* Spark, Kafka, NiFi 등 Data Engineering 기술들을 이용하여 Log API (Twitter 등) 로부터 Log 를 받아 Extract, Transform 하고 HDFS(, MongoDB 등의 데이터 저장 서비스로 Load 하는 Data Pipeline 을 구현한다.
* Local 컴퓨터 위에 Docker 로 구현한 분산 환경에서 프로젝트를 진행한다
* 장애 발생을 대비한 고가용성(High Availability) 기능을 추가한다.
* Spark 로 데이터를 전처리하고 Hadoop 으로 데이터를 분석 처리한다.
* Grafana 등을 사용하여 데이터 Monitoring Dashboard 를 제작한다.
* 프로젝트 완료 후에는 실제 업무에 사용한다는 가정 하에 장애/부하 테스트를 진행하고, 기능 최적화를 한다.
* 사용한 코드 및 기술을 Github 에 모두 업로드하고 설명을 덧붙인다.

### 목적
* Bigdata Engineer 로서 전문성을 키운다.
* 다양한 Bigdata Platform 을 익힌다.

### 절차
![Project Architecture](https://raw.githubusercontent.com/david-changwoolee/spark-log-analysis-project/main/project%20architecture.jpg)
![test](/project architecture.jpg)
![test2](david-changwoolee/spark-log-analysis-project/project architecture.jpg)

* Spark Streaming 을 이용하여 Log API 로부터 Log 를 읽는다.
* Spark 에서 Log 를 전처리한다.
* 전처리한 데이터를 Kafka 에 넣는다.
* Kafka 데이터를 NiFi 로 읽어온 후 HDFS 및 기타 데이터 저장 서비스(MongoDB etc) 에 저장한다.
* Hadoop(Pig) 을 이용하여 데이터를 분석한다.
* 분석한 데이터는 HDFS 에 저장한다.
* Hive 를 통해 Grafana 에서 Query 할 수 있도록 하고 모니터링한다.

### To-Do
* 구체적인 Log API 찾기
* 구체적인 데이터 분석 방법 정하기
* 데이터별로 Kafka Topic 구별하여 사용하기
* 유용한 Hadoop Eco System 들 적용하기
* Kubernetes 를 이용하여 Container 들 관리하기
* AWS(Amazon Web Services) 로 해당 프로젝트 옮겨 구현하기

### 참고
* Spark Streaming with Twitter References [Reference1](https://www.toptal.com/apache/apache-spark-streaming-twitter) [Reference2](https://bahir.apache.org/docs/spark/current/spark-streaming-twitter/) [Reference3](https://github.com/rajrohan/spark-streaming-twitter) [Reference4](https://velog.io/@shinychan95/Twitter-API%EB%A5%BC-%ED%99%9C%EC%9A%A9%ED%95%98%EC%97%AC-%EC%8B%A4%EC%8B%9C%EA%B0%84-tweet%EC%9D%84-kafka%EB%A1%9C-%EB%B3%B4%EB%82%B4%EA%B8%B0)
