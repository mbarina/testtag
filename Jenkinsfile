pipeline {
    agent { node { label 'node2' } }
    stages {
        stage('Test') {
            when{
              tag "v1.0.*"
            }
            steps{
                sh "echo $BUILD_NUMBER"
                sh  "py.test -v --host=ifdadmin@192.168.10.158 --junit-xml junit.xml /test/test_myinfra.py"
            }
        }
    }
}
