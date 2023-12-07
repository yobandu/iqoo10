pipeline {
    agent any
    
    stages {
        stage ('checkout'){
            steps {
                git "https://github.com/yobandu/iqoo10.git"
            }}
        stage ('build'){
            steps {
                sh 'mvn install'
                }}
        stage ('deployement'){
            steps {
                sh 'cp target/iqoo10.war /home/abhishek/apache-tomcat-9.0.82/webapps'
                }}
    }
}
