node {
    stage("Pull source code from GitHub."){
      git branch: 'main', url: 'https://github.com/vikram-opensrc/dockerProject.git'
    }
    stage("Build dockerfile."){
      sh 'sudo docker build -t pipeline .'
    }
    stage("Create container."){
      sh 'sudo docker rm -f c01 && sudo docker run -itd --name c01 -p 8081:80 pipeline'
    }
}
