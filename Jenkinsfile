node {
stage("Git Clone"){

git branch: 'main', url: 'https://github.com/surya5826/Customer.git'
}
stage("Docker build"){ 
 sh 'docker build -t customer:latest .'
sh 'docker images'
stage("Deploy"){
 sh 'docker rm -f customer||true' 
sh ' docker run -d -p 9002:9002 --name customer customer:latest'
}
}
}
