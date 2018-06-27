pipeline {
    agent { node { label 'node2' } }
    stages {
        stage('Build') {
            steps {
                  echo 'Building..'
            }
        }
        stage('Test') {
            steps {
              sh  "/home/mbarina/.local/bin/py.test -v --host=root@192.168.10.178 --junit-xml junit.xml /test/test_myinfra.py"
            }
        }
        stage('Test2') {
            steps {
                echo 'Testing2..'
            }
        }
        stage('Test3') {
            steps {
                echo 'Testing3..'
            }
        }
        stage('Test4') {
            steps {
                echo 'Testing4..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
