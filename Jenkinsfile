pipeline {

    agent any

    tools {
        maven 'maven3.6.3'
        jdk 'jdk8'
    }

    stages {
        stage ('pull from git') {
            steps {
              

		git 'https://github.com/zonayed78/maven-pipeline.git'
            }
        }
        stage ('Build') {
            steps {
                bat 'mvn clean compile package'
                bat 'java -cp target/my-app-1.0-SNAPSHOT.jar com.mycompany.app.App'
            }
        }
    }
}
