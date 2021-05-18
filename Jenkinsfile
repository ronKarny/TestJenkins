node{
    stage('Initialize'){
        def dockerHome = tool 'myDocker'
        env.PATH = "${dockerHome}/bin:${env.PATH}"
    }
    stage ('Clone') {
        checkout scm
    }
    stage("build"){
        sh """docker build -t hello ."""
    }
    stage("run"){
        sh """ docker run --rm hello """
    }
    
}
