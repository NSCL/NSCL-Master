# NSCL Repository

Dept. of Mechanical system design engineering, Seoul National Univ. of Science and Technology, Hightech 239, 172 Gongneung 2-dong, Nowon-gu, Seoul 139-743, Korea.

## 2018

### Project - Mobile robot repository

#### ROS Source : 

> https://github.com/Geonhee-LEE/mobile_robot.git

#### OpenCR :

> https://github.com/Geonhee-LEE/opencr.git

### Project - Manipulator repository
> https://github.com/changhee-Jung/manipulator_6dof.git


### Project - MR Damper repository
> https://github.com/moamoamoa/mr_damper.git



### Capstone - Dual arm service robot repository
> https://github.com/NSCL/dual-arm-service-robot.git


## 2019

### 2019 - Project - Manipulator repository 

> https://github.com/NSCL/jinyoung-manipulator








---------

# How to use the github using commands in Ubuntu

## git 설치

git 설치

> $ sudo apt-get install git-core



Github 개인 정보 등록

> $ sudo git config --global user.name "본인 계정 입력"

> $ sudo git config --global user.email "본인 메일 주소 입력"

> $ sudo git config --global color.ui "auto"


github 저장소 복제
> $ sudo git clone https://git@github.com:Geonee/Geonhee.git <- (your repository URL)



원격 저장소 등록

> $ sudo git remote add origin https://git@github.com:Geonee/Geonhee.git <- (your repository URL)

> $ sudo git fetch origin



변경된 모든 파일 추가 (커밋 전에 필수 실행)

> $ sudo git add -A



아래의 명령어를 입력후 엔터 치고 변경목록이 보이면 Ctrl+o 그리고 엔터 그리고 Ctrl+x 종료한다.

> $ sudo git commit



커밋 메세지를 입력 (하지 않으면 안됨)

> $ sudo git commit -m "메세지입력"



저장소에 올리기 (계정과 암호 물어보면 입력)

> $ sudo git push



저장소 업데이트 (내려받기)

> $ sudo git pull



git 상태 확인

> $ git status

reference : "http://dejavuwing.tistory.com/entry/Ubuntu-GitHub-%EC%82%AC%EC%9A%A9%EB%B2%95"




# How to add the Github SSH Key

### 4.1 Github SSH Key 추가하여 이용하기

 키 생성
```
ssh-keygen -t rsa -C "your_git_ID@github.com"
```
passphrase(암호)를 넣어준다.
사용하지 않을 시 엔터로 Pass
```
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
```
 새로운 키를 에이전트에 추가한다.
```
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
ssh-add -l
```
생성된 ssh-Key 복사
```
cat ~/.ssh/id_rsa.pub
```
깃허브 Setting-SSH and GPG Keys 접속 [Link](https://github.com/settings/keys) 후 복사한 ssh-key 추가


아래의 명령어를 넣고
```
ssh -T git@github.com
```
"You've successfully authenticated, but GitHub does not provide shell access."
라는 문구가 나오면 완료

이후 
```
"git clone git@github.com:저장소 경로"
```
명령어를 통해 인증 없이 Push & Pull 가능


