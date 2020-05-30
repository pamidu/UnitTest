pipeline {
    agent any
    stages {
        stage('Build ID') {
            steps {
                sh('echo ${BUILD_NUMBER}')
                            }
        }
        stage('Build Docker Image') {
            steps {
              sh ('phpunit CalculatorTest.php')
              // sh('docker build -t 156109194032.dkr.ecr.us-west-2.amazonaws.com/liongate-dev:Admin-Portal .')

            }
        }
        stage('Re-init ECR Auth Token') {
            steps {
                sh('echo ${BUILD_NUMBER}')
              // sh('aws ecr get-login --no-include-email --region us-west-2 --no-include-email > auth-token.sh')
               //sh('chmod +x auth-token.sh')
              // sh('sh ./auth-token.sh')
            }
        }
        stage('Push Docker Image') {
            steps {
                sh('echo ${BUILD_NUMBER}')
              //  sh('docker push 156109194032.dkr.ecr.us-west-2.amazonaws.com/liongate-dev:Admin-Portal')
               

            }
        }
         stage('ECS Deploynment')   {
             steps {  
                 sh('echo ${BUILD_NUMBER}')
            // sh('/bin/sh ./ecs.sh')
            }
        }
    }

}
