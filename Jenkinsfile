pipeline {
    agent any
    stages {
        stage('Build ID') {
            steps {
                sh('echo ${BUILD_NUMBER}')
                            }
        }
        stage('Unit Test') {
            steps {
              sh ('phpunit CalculatorTest.php')
            }
        }
       
    }

}
