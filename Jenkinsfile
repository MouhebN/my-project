pipeline {
    agent any

    triggers {
        gitlab(triggerOnPush: true, branchFilterType: "All")
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Show System Date') {
            steps {
                script {
                    echo "La date système est : ${new Date()}"
                }
            }
        }
    }

    post {
        always {
            echo "Pipeline terminé"
        }
    }
}
