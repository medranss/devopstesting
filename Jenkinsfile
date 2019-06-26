pipeline {
    agent any
    stages { 
        stage('Clean and Clone Repo') {
            steps { 	
		script {
                    if (fileExists('./devopstesting')){
                        bat label: '', script: 'git pull origin master'
                    }
		    else{
                        bat label: '', script: 'git clone https://github.com/medranss/devopstesting.git'
		    }
                } 	  
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
