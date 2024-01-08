pipeline {
    agent {
        docker {
            image 'rust:1.75'
            argv ''
        }
    }
    stages {
        stage('build') {
            steps {
                sh 'rustc --version'
                sh 'cargo test'
                sh 'cargo build --release'
            }
        }
    }
}