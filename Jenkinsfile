pipeline {
    agent any

    stages {
        // stage('Build') {
        //     steps {
        //         bat 'dir && node --version && npm --version && npm ci && npm run build && dir'
        //     }
        // }
        stage('Test') {
            steps {
                script {
                    if (fileExists('build/index.html')) {
                        bat 'npm test'
                    } else {
                        echo 'build failed!!'
                    }
                }
            }
        }
    }
}
