@Library('jenkins-shared-Iibrary')

pipeline {
    agent any
    tools {
        maven 'Maven'
    }

    stages {
        stage("init") {
            steps {
                script {
                  gv = load "script.groovy"
                }
            }
        }

        stage("build jar") {
            }
            steps {
                script {
                    gv.buildjar()
                }
            }
        }

        stage("build image") {
            steps {
                script {
                    gv.buildImage()
                }
            }
        }

        stage("deploy")
            steps {
                script {
                    gv.deployApp()
                }
            }
        }
    }   
}
