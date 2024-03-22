# EC2 Guide

## EC2 인스턴스 생성
- EC2 인스턴스를 생성하기 위해 다음의 URL에 접속한다.
  https://eu-west-2.console.aws.amazon.com/ec2/home?region=eu-west-2#Home:

- 이후, 좌측 메뉴 인스턴스 -> 인스턴스 시작을 클릭하면 인스턴스 생성 페이지가 나타난다.
- 이름을 설정하고 애플리케이션 및 OS 이미지 - quick start에서 Ubuntu를 선택한다. 이때, 
  아래와같은 Amazon Machine Image(AMI)이 선택되었는지 확인한다.

![image](https://github.com/kyusooK/ec2-guide/assets/123912988/fe02d94c-4719-4ee7-8358-ae7e1820446f)
- 키 페어 - 새 키 페어 생성을 클릭한 후 아래의 화면에서 키 페어 이름을 설정한 후 키 페어 생성을 클릭한다.
![image](https://github.com/kyusooK/ec2-guide/assets/123912988/b9b60af8-5880-45c2-98dd-e8abdc48fc8b)
- 인스턴스 유형에 아래와 같이 설정되어있는지 확인한다.
![image](https://github.com/kyusooK/ec2-guide/assets/123912988/05156416-d208-419d-855a-3493a12d7eef)
- 이후 인스턴스 시작을 누르면 인스턴스가 생성된다.

## 보안그룹 생성
