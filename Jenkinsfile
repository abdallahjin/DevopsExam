node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t 6422:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'abdallahjin' -p 'Junaid10' "
sh "docker tag 6422:latest abdallahjin/6422:latest"
sh "docker push abdallahjin/6422:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}
