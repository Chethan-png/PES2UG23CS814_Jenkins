pipeline {
    agent any  // This defines the environment where the pipeline will run.

    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file
                    sh 'g++ -o YOUR_SRN-1 yourfile.cpp'  // Replace 'yourfile.cpp' with your .cpp file name.
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Run the compiled .cpp file and print the output
                    sh './YOUR_SRN-1'  // This runs the compiled binary.
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Add deploy-related scripts here
                    echo 'Deploying your application'
                    // You can add deploy logic, such as copying files or triggering deploy scripts.
                }
            }
        }
    }

    post {
        failure {
            // This block is triggered if any stage fails.
            echo 'Pipeline failed'
        }
        success {
            // This block is triggered if the pipeline runs successfully.
            echo 'Pipeline succeeded'
        }
    }
}
