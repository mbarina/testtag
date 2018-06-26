pipeline {
    agent any


    stages {
        stage('Build') {
            steps {
                def tag = sh(returnStdout: true, script: "git tag --contains | head -1").trim()
                if(tag){
                  echo 'Building..'
                  echo tag
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Test2') {
            steps {
                echo 'Testing2..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
