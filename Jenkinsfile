pipeline {
agent any
stages{
    stage('checkout-stage'){
        steps {
            checkout([$class: 'GitSCM', branches: [[name: 'main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Ranjithkatam/DevOps_Assignment_Riktamtech.git']]])
        }
    }
    stage('Docker-Build'){
        steps {
            sh 'docker build -t hello-riktam .'
        }
    }
    stage('Running-Container'){
        steps {
            sh 'docker run -p 5000:5000 -d hello-riktam'
        }
    }
    }
}
