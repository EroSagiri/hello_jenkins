pipeline {
    agent {
        docker {
            image 'rust:1.75'
        }
    }

    stages {
        stage('build') {
            steps {
                sh 'rustc --version'
                sh 'cargo build --release'
            }
        }

        stage('test') {
            steps {
                sh 'cargo test'
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: 'target/release/hello_jenkins', fingerprint: true
        }
    }
}
