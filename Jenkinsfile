pipeline {
    agent any
    stages {
        stage('Compile'){
            steps {
                echo "Compiled successfully!!";    
            }
        }
        stage('Quality-Gate'){
            steps {
                echo "SonarQube quality gate passed successfully!!";
                /*sh exit ("1");*/    
            }
        }
        stage('Deploy'){
            steps {
                echo "Deployed successfully!!";
            }
        }
    }
    post {
        always {
            echo "This will run always";
        }
        success {
            echo "This will run only if successfull";
        }
        failure {
            echo "This will run only if failed";
        }
        unstable {
            echo "This will run only if the run was marked as unstable";
        }
        changed {
            echo "This will run only if the state of the pipeline has changed";
            echo "For example, if the pipeline was previously failing but is now successful";
        }
    }
}
