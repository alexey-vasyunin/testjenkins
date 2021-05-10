pipeline {
    agent any
    parameters {
        choice(name: 'builderPlugin', choices: ['Maven', 'Gradle'])
        string(name: 'args', defaultValue: '', description: 'Additional arguments for maven')
    }
    stages {
        stage('Build') {
            steps {
                sh """
                echo "Building..."
                echo "{$params.builderPlugin}"
                echo "{$params.args}"
                """
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}