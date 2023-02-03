pipeline  {

   agent any
//    def registryProjet='mateo1345/'

    stages{
        stage('Clone') {
            steps {
                checkout scm
            }
        }

        stage ("Prune") {
            steps {
            sh 'docker system prune -a --volumes -f'
            }
        }

        stage('Install'){
            steps{
                sh 'apk update'
                sh 'apk add docker-compose'
            }
        }

        stage('Build') {
            steps{
                sh 'docker-compose up -d'
            }
        }
    }
}