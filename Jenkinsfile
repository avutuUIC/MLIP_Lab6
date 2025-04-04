pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''#!/bin/bash
                echo 'In C or Java, we can compile our program in this step'
                echo 'In Python, we can build our package here or skip this step'
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''#!/bin/bash
                echo 'Test Step: Running pytest in virtual environment'

                # Activate the virtual environment
                source /Users/apoorvav/Desktop/Assignments/Sem2/RAI/Lab\\ Assigments/Lab7/lab7/bin/activate
                
                # Run pytest
                pytest

                echo 'Tests completed successfully!'
                '''
            }
        }
        stage('Deploy') {
            steps {
                echo 'In this step, we deploy our project'
                echo 'Depending on the context, we may publish the project artifact or upload pickle files'
            }
        }
    }
}
