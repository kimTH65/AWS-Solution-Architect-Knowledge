# EC2 (Elastic Compute Cloud)

<h3>기본 사항</h3>

<a href="https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/ec2-instances-and-amis.html">인스턴스 및 AMI(Amazon Machine Image)</a> : 인스턴스 = 가상 컴퓨팅 환경 / AMI = 서버에 필요한 OS, 소프트웨어를 구성된 상태로 제공되는 템플릿
<h6>
&emsp;&emsp;&emsp;&emsp;PV(반가상화) AMI : guest OS가 Hypervisor(가상머신을 생성하고 실행하는 프로세스)를 통해 Hardware를 제어
<br><br>
&emsp;&emsp;&emsp;&emsp;HVM(하드웨어 가상 머신) AMI : guest와 완전히 독립되고 OS 수정이 없이 사용이 가능
</h6>
<br><br>
<a href="https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/Using_Tags.html">태그</a> : 사용자가 생성하여 Amazon EC2 리소스에 할당할 수 있는 메타데이터
<br><br>
<a href="https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/instance-types.html">인스턴스 유형</a> : 인스턴스를 위한 CPU, 메모리, 스토리지, 네트워킹 용량 여러가지 구성 제공
<br><br><a href="https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/using-regions-availability-zones.html">리전(Region) 및 가용영역(AZ)</a> : 인스턴스와 EBS볼륨 등의 리소스를 다른 물리적 장소에서 액세스할 수 있는 리전 및 가용영역
<h6>&emsp;&emsp;&emsp;&emsp;AZ(Availability Zone) : 각 리전 내의 격리된 위치, 개별 데이터 센터로 구성되어 있음</h6>
<hr>
<h3>네트워킹 및 보안</h3>
<br>
<a href="https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/ec2-key-pairs.html">키 페어</a>로 
인스턴스 로그인 정보 보호(AWS는 퍼블릭 키 저장, 사용자는 개인 키 안전장소에 보관)
<br><br>
<a href="https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/ec2-security-groups.html">보안 그룹</a>
을 사용해 인스턴스에 연결할 수 있는 프로토콜, 포트, 소스 IP 범위를 지정하는 방화벽 기능
<br><br>
<a href="https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html">탄력적 IP 주소(EIP)</a> : 동적 클라우드 컴퓨팅을 위한 고정IPv4 주소
<br><br>

<a href="https://github.com/kimTH65/AWS/blob/main/aws/VPC.md">VPC(Virtual Private Cloud)</a> : AWS 클라우드에서 논리적으로 격리되어 있지만 원할 때 마다 고객의 네트워크와 연결 가능한 가상 네트워크

<hr>
<h3>스토리지</h3>
<br>인스턴스 스토어 볼륨 : 임시 데이터 저장하는 스토리지 볼륨, 인스턴스 중단, 최대 절전모드/종료 시 삭제됨
<br><br>EBS(Elastic Block Store) : Amazon EBS 볼륨을 사용해 영구 스토리지 볼륨에 데이터 저장

<hr>
<h3>Linux 인스턴스 작업</h3>
<br>AWS Systems Manager Run Command : PowerShell같은 것 이용해서 명령 보내는 것

<br>LAMP(Linux, Apache, MYSQL/MairaDB, PHP/Perl/Python같은 언어) 웹서버,LAMP 스택 :
<br>&emsp;&emsp;&emsp;&emsp;Amazon Linux 2 인스턴스에 PHP및 MariaDB 지원을 포함하는 Apache 웹서버

<br>Secure Sockets Layer/Transport Layer Security(SSL/TLS): 웹 서버와 웹 클라이언트 간 암호화된 채널을 만들어 데이터 도청 방지

<hr>
<h3>Amazon EC2 액세스</h3>
<br>CLI(AWS Command Line Interface) 
<br><br>AWS Tools for Windows PowerShell

<hr>
<h3><a href="https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/instance-purchasing-options.html">Amazon EC2 가격</a></h3>
<br>프리티어 : 무료
<br><br>On-Demand instances : 약정 결제없이 초 단위로 사용한 인스턴스 요금을 지불
<br><br>Savings Plans : 1/3년 기간 동안 시간당 USD로 일괄된 사용량을 약정하여서 비용 절감
<br><br>예약 인스턴스 : 1/3년 기간 동안 인스턴스 유형/지역을 포함해 특정 인스턴스 약정하여서 비용 절감
<br><br>Spot Instances : 미사용 EC2 인스턴스 요청하여서 비용 대폭 절감

