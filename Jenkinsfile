pipeline{
    agent any
    tools {
    maven  "shivani"
    }
    stages{
        stage("clone"){
            steps{
                echo "cloning the code "
                git branch: 'test', url: 'https://github.com/mantu0tech/simple-java-app.git'
            }
        }
        stage("build "){
            steps{
                echo "running the code "
                sh "mvn clean install"
            }
        }
        stage("artifact "){
            steps{
                echo "packaging the code "
                archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
            }
        }
    }
}
