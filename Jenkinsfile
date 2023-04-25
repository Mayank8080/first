pipeline {
    agent any

    stages{
        stage("git"){
            steps{
                git url: 'https://github.com/Mayank8080/first.git', branch: 'master'

            }
        }
        stage("Build"){
            steps{
                sh 'mvn clean install'
            }
        }
        stage('Deploy to Tomcat') {
            steps {
                deploy adapters: [tomcat9(credentialsId: 'TomcatCredentials', url: 'http://localhost:9006/')], contextPath: '/webapp', war: '**/*.war'
            }
        }
        }
}
