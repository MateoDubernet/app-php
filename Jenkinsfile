pipeline  {

   agent any
   def registryProjet='mateo1345/'

    stages{
    stage('Clone') {
            steps {
                checkout scm
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

        stage('Curl'){
            steps{
                sh 'curl localhost:9000/create_db.php'
            }
        }
    }
    

    // def img = stage('Build') {
    //     echo "build"
    //     docker.build("$IMAGE",  '.')
    // }

    // stage('Run') {
    //     echo "run"
    //     //   img.withRun("--name run-$BUILD_ID -p 8000:80") { c ->
    //     //   }
    // }

    // stage('Push') {
    //     echo "push"
    // //    docker.withRegistry('https://index.docker.io/v1/' , 'hub_docker_id') {
    // //           img.push 'latest'
    // //           img.push()
    // //       }
    // }
}