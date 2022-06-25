pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                sh "mvn clean package"
            }
        }
        stage("Deploy"){
            steps{
                deploy adapters: [tomcat7(credentialsId: '88bb4bd0-78a7-4184-88a2-11cc70a44662', 
                path: '', 
                url: 'http://52.66.204.58:8080/')], 
                contextPath: 'javawebapp1', 
                war: '**/java-web-project.war'
            }
        }
    }
}
