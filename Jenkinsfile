node {

   def registryProjet='mateo1345/'

   stage('Checking'){
        sh 'docker version'
   }

    stage('Clone') {
        checkout scm
    }

    stage('Install'){
        echo "install"
        sh 'apk update'
        sh 'apk add docker-compose'
    }

    stage('Build') {
        echo "build"
        sh 'docker-compose up -d'
    }

    stage('Test'){
        sh 'curl localhost:8000'
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