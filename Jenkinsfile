pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/nurlayla-06/5097_prak8.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test' // Asumsinya sudah ada unit test
            }
            post {
                success {
                    echo 'Tes berhasil!'
                }
                failure {
                    echo 'Tes gagal!'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Menjalankan aplikasi...'
                sh 'nohup node app.js &'
            }
        }
    }
}
