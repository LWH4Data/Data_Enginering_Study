# < HDFS summary >
## 1. YARN?
- Spark, Flink, Hive 등이 HDFS를 활용하려 하면 YARN이 적당한 서버에 container를 생성 및 실행한다.
    - YARN container != Docker container
    - YARN의 contianer는 `리소스`를 논리적으로 묶은 실행 단위.
        - 즉, OS 안에서 단순히 자원을 할당하여 프로세스를 격리.
![alt text](images/YARN_docker.png)

## 2. 블록 크기에 따른 효율성 증가.
- 메모리가 크다 -> 블록의 수가 줄어든다 -> NameNode에 저장되는 정보가 적어진다 -> 메모리 낭비가 적다.
- 메모리가 적다 -> 블록의 수가 늘어난다 -> NameNode에 저장되는 정보가 많아진다. -> 메모리 낭비.