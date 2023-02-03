node {

   def registryProjet='mateo1345/'
//    def IMAGE="${registryProjet}app:3.5"

    stage('Clone') {
        echo "clone"
        checkout scm
    }

    def img = stage('Build') {
        echo "build"
        sh 'docker-compose up -d'
        sh 'docker-compose ps'
    }

    stage('Run') {
        echo "run"
        sh 'curl http://localhost:8000'
        //   img.withRun("--name run-$BUILD_ID -p 8000:80") { c ->
        //   }
    }

    stage('Push') {
        echo "push"
    //    docker.withRegistry('https://index.docker.io/v1/' , 'hub_docker_id') {
    //           img.push 'latest'
    //           img.push()
    //       }
    }
}