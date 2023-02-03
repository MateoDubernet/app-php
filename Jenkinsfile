node {

   def registryProjet='mateo1345/'
//    def IMAGE="${registryProjet}app:3.5"

    stage('Clone') {
        echo "clone"
        //   checkout scm
    }

    def img = stage('Build') {
        echo "build"
        //   docker.build("$IMAGE",  '.')
    }

    stage('Run') {
        echo "run"
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