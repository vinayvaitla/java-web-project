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
                deploy adapters: [tomcat7(credentialsId: 'ab53f948-4c5c-4ae5-a480-2c1ad4dd55da', path: '', url: 'http://3.109.184.237:8080/')], contextPath: 'javawebapp1', war: '**/java-web-project.war'
            }
        }
    }
}
