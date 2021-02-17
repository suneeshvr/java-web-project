pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh "mvn clean package"
            }
        }
        stage('Build'){
            steps{
                deploy adapters: [tomcat7(credentialsId: '85b22afd-7303-4be2-add1-074fd2351988', path: '',
                url: 'http://ec2-13-232-9-214.ap-south-1.compute.amazonaws.com:8080/')],
                contextPath: 'javawebapp', war: '**/java-web-project.war'
            }
        }
    }
}
