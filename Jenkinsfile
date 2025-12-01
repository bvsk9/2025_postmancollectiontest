pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Run build commands
                echo "Building the project"
            }
        }
            stage('Deploy to DEv') {
            steps {
                // Run build commands
                echo "Deploy the project to DEv"
            }
        }
        
          stage('Pull docker image') {
            steps {
                // Run build commands
                
                 'docker pull bvskrishnadocker/fetchurls:1.0'
                 
            }
        }
        
         stage('Run API test cases') {
            steps {
                // Run build commands
                
                 'docker run -v ${pwd}/newman:/app/newman bvskrishnadocker/fetchurls:1.0'
                 
            }
        }

     stage('Deploy to prod') {
            steps {
                // Run build commands
                echo "Deploy the project to prod"
            }
        }
     

    }   
}
