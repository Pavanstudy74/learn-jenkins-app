pipeline{
    agent any
    stages{
        stage("Build"){
            agent {
                docker {
                    image "node:24-alpine"
                }
            }
                steps {
                sh """ 
                ls -al
                node --version
                npm --version
                npm ci
                npm run build
                ls -al
                
                """
            }
        
        }
    }
}