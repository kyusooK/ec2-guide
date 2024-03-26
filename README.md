# EC2 Guide

## EC2 인스턴스 생성
- EC2 인스턴스 생성을 위해 다음의 URL에 접속(https://aws.amazon.com/ko/console/) > 로그인 > 검색창에 'EC2'를 검색한다.
- 이후 화면에 보이는 인스턴스 시작을 클릭하면 인스턴스 생성 페이지가 나타난다.
- 이름을 설정하고 애플리케이션 및 OS 이미지 - quick start에서 Ubuntu를 선택한다.
- 이때,아래와같은 Amazon Machine Image(AMI)이 선택되었는지 확인한다.
![image](https://github.com/kyusooK/ec2-guide/assets/123912988/fe02d94c-4719-4ee7-8358-ae7e1820446f)
- 키 페어 - 새 키 페어 생성을 클릭한 후 아래의 화면에서 키 페어 이름을 설정한 후 키 페어 생성을 클릭한다.
![image](https://github.com/kyusooK/ec2-guide/assets/123912988/b9b60af8-5880-45c2-98dd-e8abdc48fc8b)
- 인스턴스 유형에 아래와 같이 설정되어있는지 확인한다.
![image](https://github.com/kyusooK/ec2-guide/assets/123912988/05156416-d208-419d-855a-3493a12d7eef)
- 이후 인스턴스 시작을 누르면 인스턴스가 생성된다.

## 보안그룹 생성
- 생성한 인스턴스를 클릭하면 인스턴스의 세부정보가 나타난다. 여기서 보안 -> 보안그룹을 클릭하여 인스턴스와 연결된 보안그룹으로 이동한다.
- 이동 후, 인바운드 규칙 > 인바운드 규칙 편집 > 규칙 추가를 통해 아래와 같이 8080 port에 대한 인바운드 규칙을 추가한다.

  유형: 사용자 지정 TCP <br>
  포트 범위: 8080 <br>
  소스: 0.0.0.0/0 <br>
![image](https://github.com/kyusooK/ec2-guide/assets/123912988/d59356ae-4f5c-42ea-8ac3-8858f9490c8b)

## EC2 접속
- 로컬 터미널로 생성된 키 페어의 경로로 이동한다.
- 다음의 명령어를 입력하여 EC2에 접속한다. 이때, ec2-dns-주소는 생성한 인스턴스의 세부정보에서 확인할 수 있다.
```
$ ssh -i {your-pem-file.pem} ubuntu@{your-ec2 dns 주소}
```
* Permission Denied이 출력된 경우 키 페어 경로로 이동하였는지 확인하고 이동하였다면 다음의 명령어를 통해 권한을 부여한 후 다시 접속 명령어를 입력한다.
```
chmod 600 {your-pem-file.pem}
```
접속이 완료되면 'ubuntu@ip-프라이빗 IPv4 주소'로 터미널 프롬프트가 변경된 것을 확인할 수 있다.
