pipeline {
    agent { docker 'rust:1.75' }
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