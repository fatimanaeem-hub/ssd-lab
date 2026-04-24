pipeline {
    agent any

  
    parameters {
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Run tests?')
    }

 
    environment {
        VERSION = "1.0"
    }

    stages {

        stage('Build') {
            steps {
                echo "Version is ${VERSION}"
            }
        }

        // Optional: your Test stage
        stage('Test') {
            when {
                expression { params.executeTests == true }
            }
            steps {
                echo 'Testing..'
            }
        }
    }
}
