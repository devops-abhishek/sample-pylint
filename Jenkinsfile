pipeline {
    agent any

    stages {
        stage('Pylint') {
            steps {
              pylint --rcfile=./pylintrc sample.py
              pylint --rcfile=./pylintrc sample1.py
              exit 0
            }
        } 
        stage('Pylint-Report') {
            steps {
                recordIssues (
                    tool: PyLint()
                )    
            }
        }
    }
}
