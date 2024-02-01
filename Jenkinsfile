def gv

pipeline {
    agent any
    stages {
        stage("init") {
            steps {
                script {
                    gv = load "script.groovy"
                }
            }
        }
        stage("Build") {
            steps {
                script {
                    // echo "building jar"
                     gv.buildApp()
                }
            }
        }
        stage("Test") {
            steps {
                script {
                    //echo "building image"
                    gv.testApp()
                }
            }
        }
        stage("Deploy") {
            steps {
                script {
                    //echo "deploying"
                    gv.deployApp()
                }
            }
        }
    }   
}