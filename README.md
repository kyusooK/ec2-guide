# EC2 Guide

## EC2 인스턴스 생성
- EC2 인스턴스 생성을 위해 다음의 URL에 접속(https://aws.amazon.com/ko/console/) > 로그인 > 검색창에 'EC2'를 검색한다.
- 이후 화면에 보이는 인스턴스 시작을 클릭하면 인스턴스 생성 페이지가 나타난다.
- 이름을 설정하고 애플리케이션 및 OS 이미지 - quick start에서 Ubuntu를 선택한다.
- 이때,아래와같은 Amazon Machine Image(AMI)이 선택되었는지 확인한다.
![image](https://github.com/kyusooK/ec2-guide/assets/123912988/fe02d94c-4719-4ee7-8358-ae7e1820446f)

### 인스턴스 유형 
- 인스턴스 유형은 아래와 같이 't3.medium'으로 설정한다.
![image](https://github.com/kyusooK/ec2-guide/assets/123912988/b18c0484-df52-4f71-891c-8e000c531344)

### 키 페어 설정
- 키 페어(로그인) 옵션에서 아래와 같이 '키 페어 없이 계속진행'을 선택한다.
![image](https://github.com/kyusooK/ec2-guide/assets/123912988/50f0f295-5dae-4523-957d-afcf3caa9bde)

### 보안그룹 생성
- 네트워크 설정 > 편집 > 인바운드 보안 그룹 규칙 > 보안그룹 규칙 추가에서 아래과 같이 8080 port에 대한 인바운드 규칙을 추가한다.
    - 유형: 사용자 지정 <br>
    - 원본: 0.0.0.0/0 <br>
    - 포트범위: 8080 <br>
![image](https://github.com/kyusooK/ec2-guide/assets/123912988/c24fd6db-4b01-4817-9efc-f3002c601020)

- 보안그룹까지 생성되었다면 '인스턴스 시작'을 클릭하여 인스턴스를 생성한다.

## 인스턴스 연결
- 인스턴스가 생성되면 아래와 같은 화면이 나타나는데, 아래 옵션 중 '인스턴스에 연결'을 클릭한다.
![image](https://github.com/kyusooK/ec2-guide/assets/123912988/b98c7790-5909-482a-9bc1-8569daf384c4)
- 아래와 같이 인스턴스 연결 설정에 대하여 'EC2 Instance Connect을 사용하여 연결' > 연결을 진행하면 웹 상에서 생성한 인스턴스에 접속할 수 있다.
![image](https://github.com/kyusooK/ec2-guide/assets/123912988/dc77b247-7a1f-4acb-862c-78a289dccaa1)
