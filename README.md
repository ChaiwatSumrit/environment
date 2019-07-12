# Environment
environment begin for developer 
**บางตัวสามารถหาวิธี install วิธีอื่นได้ครับ**
## 1.Install Curl
```
sudo apt-get update
sudo apt-get install curl
```

## 2.Install Docker and Docker Compose 
**ในwindow ต้องให้สิทธิ์ แชร์envของไดร์ให้dockerต้องใส่user&passเดียวกับตอนลงwindow และ window ต้องลง docker desktop เพิ่มด้วย**
	- https://docs.docker.com/install/linux/docker-ce/ubuntu/#install-docker-ce-1
	- https://docs.docker.com/compose/install/#install-compose
```
sudo usermod -a -G docker $USER
//check
docker -version 
```

## 3.Install GOLANG
	- https://golang.org/doc/install?download=go1.10.2.linux-amd64.tar.gz
```
sudo tar -C /usr/local -xzf go1.10.2.linux-amd64.tar.gz
```

## Set go root in "home/.bashrc" 
**ตั้งค่า path ใน ubuntu ของ window & mac ต้อง google เพิ่มหน่อยนะครับ**
```
export GOPATH="$HOME/GO-PATH"
export GOROOT="/usr/local/go"
export PATH="$GOPATH/bin:$GOROOT/bin:$PATH"
```
## Create GO-PATH folder 
**in ubuntu** 
```
create "bin", "src", "pkg" folder
create "github.com folder" in src folder
create "hyperledger" folder in "github.com" ( into "hyperledger" folder)
```
## clone lib hyperledger repositorie 
```
git clone https://github.com/hyperledger/fabric.git 
```

## 4.Install Node.js Runtime and NPM and NVM  //SDK ใช้คุยกับ Blockchain
	- https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-16-04
	

## 5.Install Python
```
sudo apt-get install python
```

## 6.Download the Hyperledger Fabric docker images for the version specified //ต้องลง docker ให้สำเร็จก่อนนะครับ
```
curl -sSL http://bit.ly/2ysbOFE | bash -s -- 1.4.1 1.4.1 0.4.15
```

## 7.Clone the hyperledger/fabric-samples repository // window อาจจะต้องลง gitcommand ก่อน
```
git clone https://github.com/hyperledger/fabric-samples.git
```

