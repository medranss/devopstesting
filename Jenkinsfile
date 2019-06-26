pipeline {
    agent any
    stages { 
        stage('Clean and Clone Repo') {
            steps { 
                bat label: '', script: 'git pull https://github.com/medranss/devopstesting.git'
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
