pipeline{
    agent any
    stages{
        stage('Build image') {
            app = docker.build("eu.gcr.io/igneous-sum-312016/db_pdo_pipeline")
            }
            stage('Push image') {
            docker.withRegistry('https://eu.gcr.io', 'gcr:docker_build') {
                app.push("${env.BUILD_NUMBER}")
                app.push("latest")
            }
            }
        }
    }


// pipeline {
//     agent any
//     stages {
//         stage('Build image') {
//             app = docker.build(' eu.gcr.io/igneous-sum-312016/php-apache')
//             script {
//                     def customImage = docker.build("my-image:${env.BUILD_ID}")
//                     customImage.push()
//             }
//         }
//         stage('Push image') {
//             docker.withRegistry('https://eu.gcr.io', 'gcr:docker_build') {
//                 app.push("${env.BUILD_NUMBER}")
//                 app.push('latest')
//             }
//         }
//     }
// }