pipeline {
    agent any
    
    stages {
        stage ('checkout'){
            steps {
                   'checkout scm'
            }}
        stage ('build'){
            steps {
                sh '/home/abhishek/apache-maven-3.9.5-bin/apache-maven-3.9.5/bin/mvn install'
                }}
        stage ('deployement'){
            steps {
                sh 'cp target/iqoo10.war /home/abhishek/apache-tomcat-9.0.82/webapps'
                }}
    }
}
