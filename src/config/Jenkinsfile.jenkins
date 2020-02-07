pipeline {
    agent { docker { image 'maven_3_6_3' } }

    stages {
        stage ( 'Git Checkout' ) {
            steps {
                git url:'https://github.com/suminorue/jenkins-test'
            }
        }
        stage ('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}