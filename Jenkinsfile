pipeline { 
   agent any

   environment {
       CI = 'true'
   }

   stages {
       stage('Checkout') {
           steps {
               git branch: 'main', url: 'https://github.com/rilaaaa/Praktikum-8-PPMPL.git' 
           }
       }

       stage('Install Dependencies') {
           steps {
               bat 'npm install'
           }
       }

       stage('Run Unit Tests') {
           steps {
               bat 'npm test'
           }
       }

       stage('Build') {
           steps {
               echo 'Building the application...'
               // Tambahkan perintah build jika diperlukan
           }
       }

       stage('Deploy') {
           steps {
               echo 'Deploying the application...'
               // Tambahkan perintah deploy jika diperlukan
           }
       }
   }

   post {
       success {
           echo 'Pipeline finished successfully!' 
       }
       failure {
           echo 'Pipeline failed!'
       }
   }
}