pipeline{

    agent any

    tools{
       maven 'Maven 3.9.15' 
    }    

    stages{
        stage('one'){
            steps{
                echo 'this is the first job'
                sh 'mvn compile '
                sleep 4
            }
        }
        stage('two'){
            steps{
                echo 'this is the second job'
                sh 'mvn clean test'
                sleep 9
            }
        }
        stage('three'){
            steps{
                echo 'this is the third job'
                sh 'mvn package -DskipTests'
                sleep 7
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}
