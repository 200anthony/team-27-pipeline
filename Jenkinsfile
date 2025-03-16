pipeline {
    agent any
    stages {
        stage('...Build...') {
            steps {
                sh 'mvn clean '
            }
        }
        stage('...Test...') {
            steps {
                sh 'mvn test'
            }
            post{
                success{
                    echo "Artifacts"
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
