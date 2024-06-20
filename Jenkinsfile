node {
    def app
    stage('Clone') {
        checkout scm
    }
    stage('Build image') {
        app = docker.build('amadou80/nginx')
    }
    stage('Test image') {
        app = docker.build('amadou80/nginx').withRun('-p 80:80') { c ->
            sh 'docker ps'
        }
    }
}
