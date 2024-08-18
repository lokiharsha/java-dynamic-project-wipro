pipeline{
    agent any
    
    stages{
        
        stage('git scm'){
            steps{
                git 'https://github.com/lokiharsha/java-dynamic-project-wipro.git'
            }
        }
        stage('clean'){
            
            steps{
                sh 'mvn clean'
            }
        }
        stage('compile'){
            
            steps{
                sh 'mvn compile'
            }
            
        }
        stage('package'){
            
            steps{
                sh 'mvn package'
            }
            
        }
        stage('install'){
            
            steps{
                sh 'mvn install'
            }
            
        }
        stage('deploy to sonar'){
            
            steps{
                  sh '''
                sonar-scanner  -DprojectKey=your_project_key -Dsonar.sources=src/main/java
                  '''
                 }
        }
        
    }
   
    
}
