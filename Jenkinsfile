//Jenkinsfile (Declarative Pipeline)
//test
//hello
//test2
//test4
//test5
//test6
/* Requires the Docker Pipeline plugin */
pipeline {
    agent any 
    environment {
        // Using returnStdout
        CC = """${sh(
                returnStdout: true,
                script: 'echo "clang"'
            )}""" 
        // Using returnStatus
        EXIT_STATUS = """${sh(
                returnStatus: true,
                script: 'exit 1'
            )}"""
    }
    stages {
        stage('Example') {
            environment {
                DEBUG_FLAGS = '-g'
            }
            steps {
                sh 'printenv'
                echo "$CC"
                sh ('echo ${EXIT_STATUS}')
                echo "${BUILD_ID}"
            }
        }
    }
}
