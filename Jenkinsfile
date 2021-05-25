pipeline {
    agent any
    stages {
        stage('Build image') {
            steps{
                echo "Start build"
                echo "Building..."
                echo "End of Bulding"
            }
        }
        stage('Test image') {
            steps{
                echo "Start Testing"
                echo "Testing..."
                echo "End of Testing"
            }
        }
        stage('Deploy image') {
            steps{
                echo "Start Deploying"
                echo "Deploy..."
                echo "End of Deploying"
            }
        }
    }
}

// pipeline {
//     agent any
//     stages {
//         stage('Build image') {
//             app = docker.build(' eu.gcr.io/igneous-sum-312016/pdo_pipeline')
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
