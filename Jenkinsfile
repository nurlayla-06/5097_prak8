pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git url: 'https://github.com/nurlayla-06/5097_prak8.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                echo 'Tahap build berjalan.'
            }
        }

        stage('Test') {
            steps {
                echo 'Tes unit berjalan (simulasi).'
            }
        }
    }
}
