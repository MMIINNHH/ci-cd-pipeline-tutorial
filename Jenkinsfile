pipeline {
    environment {
        registry = "noon-ai-dis.ncr.gov-ntruss.com/noon-ai-dis-web"
        registryCredential = 'container-registry'
        dockerImage = ''
    }
    
    agent any

    stages {
        stage('Git Clone') {
            steps {
                git branch: 'master', credentialsId: 'Git-Credentials-with-ID', url: 'https://github.com/MinHyeong-Lee/ci-cd-pipeline-tutorial.git'
            }
        }
        stage('Build') {
            steps {
                sh 'echo Build Test'
                // final String url = "'Accept: application/vnd.github+json' -H 'Authorization: Bearer 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' https://api.github.com/repos/MHNCity/noon-ai-dis-web/tags"

                // final String response = sh(script: "curl -H $url", returnStdout: true).trim()

                // echo response
                // sh 'docker build -t $registry:$BUILD_NUMBER .'
                // sh 'docker image tag $registry:$BUILD_NUMBER $registry:latest'
            }
        }
        // stage('Push image') {
        //     steps {
        //         withDockerRegistry([ credentialsId: registryCredential, url: "" ]) {
        //             sh 'docker push $registry:$BUILD_NUMBER'
        //             sh 'docker push $registry:latest'
        //         }
        //         echo 'Push image...'
        //     }
        // }
        // stage('Clean image') {
        //     steps {
        //         sh 'docker rmi $registry:$BUILD_NUMBER'
        //         sh 'docker rmi $registry:latest'
        //         echo 'Clean image...'
        //     }
        // }
    }
}
