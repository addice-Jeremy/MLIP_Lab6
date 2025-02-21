pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''#!/bin/bash
                echo 'Skipping build step for Python'
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''#!/bin/bash
                echo 'Test Step: Running pytest...'

                # Activate virtual environment
                source mlip/bin/activate

                # Run pytest
                pytest

                echo 'Pytest completed successfully'
                '''  # Removed `exit 1` to prevent failure after fixing the script
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
