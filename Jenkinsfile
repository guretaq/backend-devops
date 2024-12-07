pipeline {
    agent any
    stages{
        stage("build - instalación de dependiencias"){
            agent {
                docker {
                    label 'contenedores'
                    image 'node:22-alpine'
                    reuseNode true
                }
            }
            stages{
                stage("build - instalación de dependiencias"){
                    steps{
                        sh 'npm install'
                    }
                }
                stage("build - build del proyecto"){
                    steps{
                        sh 'npm run build'
                    }
                }
            }
        }
    }
}