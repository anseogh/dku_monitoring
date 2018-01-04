OpenSSH server

ls -a
user group

ssh-copy-id

내 키 생성
ssh-keygen -t rsa
.ssh가 생성 된다

ls -a

cd .ssh
id_rsa
id_rsa.pub
확인

퍼블릭키 서버로 보내기
ssh-copy-id mundaeho@220.149.227.106

ssh mundaeho@220.149.227.106
패서워드 로그인이 되었기 때문에 쉽게 퍼블릭 키 전송이 가능하다

패스워드 로그인 오프
sudo nano /etc/ssh/sshd_config
앞에 샵을 제거하고
PasswordAuthenticication no

시스템 재시작
sudo systemctl restart sshd.service
이제 접속 못함


nano authorized_keys
ls
cp authorized_keys authorized_keys_temp
rm authorized_keys_templs
sudo nono /etc/ssh/sshd_config
systemctl restart sshd.service
ls
mv authorized_keys_temp authorized_keys_temp
systemctl restart sshd.service
ls





# 서버 설정
## node.js 설치
1. curl 설치
sudo apt install curl     url데이터 읽어오는 명령

2. nvm으로 nodejs설치, https://github.com/creationix/nvm#install-script, node version manager
```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh | bash

export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh" # This loads nvm

source ~/.bashrc

nvm --version
```
3. node.js 설치, 홈페이지에서 최신 버전 확인
nvm install 8.9.4


node.js 문서 확인, 예제도 다 있음
Buffer 메모리 관리, 바이너리 데이터 사용하기 때문, 바이트 잘라거 데이터 받을 수 있음
buf.readFloatLE
Child Processes
실행파일 실행
리눅수는 C 코드를 빌드시켜 실행함
Console
console.log  데이터를 어떻게 쓰고 있는지 확인
const data=300;
console.log(data)

fs.access   file system 관리


## github

cd ~/.ssh

- rsa authentication 키 확인
```cat id_rsa.pub```


