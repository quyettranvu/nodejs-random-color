pipeline {
    agent any
    stages {
        // stage('Checkout') {
        //     steps {
        //         git 'https://github.com/hoanglinhdigital/nodejs-random-color.git'
        //     }
        // }

        stage('Build') {
            steps {
                sh 'docker build -t nodejs-random-color:ver-${BUILD_ID} .'
            }
        }
        stage('Upload image to ECR') {
            steps {
                sh 'aws ecr get-login-password --region ap-southeast-1 | docker login --username AWS --password-stdin 309814440714.dkr.ecr.ap-southeast-1.amazonaws.com'
<<<<<<< HEAD
                sh 'docker tag nodejs-random-color:ver-${BUILD_ID} 309814440714.dkr.ecr.ap-southeast-1.amazonaws.com/nodejs-random-color:ver-${BUILD_ID}'
=======
                sh 'docker tag nodejs-random-color:latest 309814440714.dkr.ecr.ap-southeast-1.amazonaws.com/nodejs-random-color:ver-${BUILD_ID}'
>>>>>>> f89a011 (update Jenkinsfile)
                sh 'docker push 309814440714.dkr.ecr.ap-southeast-1.amazonaws.com/nodejs-random-color:ver-${BUILD_ID}'
            }
        }
    }
}
