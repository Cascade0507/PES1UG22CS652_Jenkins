pipeline
{
    agent{
        docker{
            image 'node:14'
        }
    }
    stages {
        stage('Clone Repository'){
            steps {
                git branch: 'main',
                url: 'https://github.com/Cascade0507/PES1UG22CS652_Jenkins.git'
            }
        }
        stage('Build Application'){
            steps {
                sh 'g++ -o new new.cpp'
            }
        }
        stage('Test Application'){
            steps{
                sh './new'
            }
        }
        stage('Deploy Application'){
            steps{
                echo 'Deploying Application'
            }
        }
        
    }
    post{
        failure{
            echo 'Build Failed'
        }
    }
}