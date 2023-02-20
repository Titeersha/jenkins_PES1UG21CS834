pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'g++ -c PES1UG21CS834_tt.cpp' //changing file name 
                sh 'g++ -o PES1UG21CS834 PES1UG21CS834.cpp'
                echo 'build stage successful'
            }
        }
        stage('Test'){
            steps{
                sh './PES1UG21CS834'
                echo 'Test stage executed successfully'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deployed Successfully'
            }
        }
    }
    post{
        failure{
            echo 'Pipeline Failed'
        }
    }
}
