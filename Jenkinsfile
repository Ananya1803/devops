node{
stage('SCM'){
checkout scm
}
stage(build'){
}
stage('aws connect'){
aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 319876539559.dkr.ecr.us-east-1.amazonaws.com
}
stage('Build Docker Image'){
docker build -t mydocker-repo .
}
stage('Tag Docker Image'){
docker tag mydocker-repo:latest 319876539559.dkr.ecr.us-east-1.amazonaws.com/mydocker-repo:latest
}
stage('Push Docker Image'){
docker tag mydocker-repo:latest 319876539559.dkr.ecr.us-east-1.amazonaws.com/mydocker-repo:latest
}
}
