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
                url: 'http://3.109.184.237:8080/')], 
                contextPath: 'javawebapp1', 
                war: '**/java-web-project.war'
            }
        }
    }
}
