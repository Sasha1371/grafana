pipeline {
    agent any

    stages {
        
        stage('Start Grafana using Docker Compose') {
            steps {
                script {
                    sh '''
                    cd /opt/grafana
                    sudo docker-compose up -d
                    '''
                }
            }
        }
    }

    post {
        always {
            sh 'docker ps -a'
        }
    }
}
