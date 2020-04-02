pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'Clone repository'
            }
        }

        stage('Build') {
            steps {
                echo 'Building code'
            }
        }

        stage('Test') {
            parallel {

                stage('Entity test') {
                    steps {
                        echo 'Testing entities....'
                    }
                }

                stage('Admin test') {
                    steps {
                        echo 'Testing admin....'
                    }
                }

                stage('Repository test') {
                    steps {
                        echo 'Testing repositories....'
                    }
                }

                stage('Service test') {
                    steps {
                        echo 'Testing services....'
                    }
                }

                stage('Integration test') {
                    steps {
                        echo 'Testing integrations....'
                    }
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying code'
            }
        }

        stage('Monitor') {
            steps {
                echo 'Monitoring software'
            }
        }

        stage('Condicional') {
            when {
                branch "master" 
            }
            steps {
                echo 'This branch is master'
            }
        }
    }
}