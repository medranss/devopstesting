pipeline {
    agent any
    stages { 
        stage('Clean and Clone Repo') {
            steps { 		  
                bat label: '', script: 'git pull origin master'
            }
        }
        stage('Build') {
            steps {
                dir('./devopstesting') {
                    bat label: '', script: '''javac "HelloWorld.java"
                                                java HelloWorld'''
                }
            }
        }
    }
}
