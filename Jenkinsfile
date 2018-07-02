pipeline {
    agent { node { label 'node2' } }
    stages {
        stage('Test') {
            when{
              buildingTag()
            }
            steps{
                sh "echo $BUILD_NUMBER"
                sh "echo $BUILD_TAG"
                sh  "py.test -v --host=ifdadmin@192.168.10.158 --junit-xml junit.xml /test/test_myinfra.py"
            }
        }
    }
}
