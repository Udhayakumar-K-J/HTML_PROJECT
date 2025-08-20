pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Udhayakumar-K-J/HTML_PROJECT.git'
            }
        }

        stage('Archive HTML Files') {
            steps {
                archiveArtifacts artifacts: '**/*.html', allowEmptyArchive: true
            }
        }
    }

    post {
        success {
            echo "✅ HTML Project pipeline completed successfully!"
        }
        failure {
            echo "❌ Pipeline failed!"
        }
    }
}
