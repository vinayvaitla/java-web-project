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
                deploy adapters: [tomcat7(credentialsId: 'e7b796b4-70e7-4e39-941a-8ef21233df4f', path: '', url: 'http://15.207.106.131:8080/')], contextPath: 'javawebapp1', war: '**/java-web-project.war'
            }
        }
    }
}
