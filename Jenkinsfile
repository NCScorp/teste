node('aws-codebuild'){

    stage('Clean') {
        deleteDir()
    }

    stage('Checkout') {
			
        timeout(time: 3600, unit: 'SECONDS') {
            checkout scmGit(
                userRemoteConfigs: [[credentialsId: 'JenkinsCheckoutHTTPS',
                url: 'https://github.com/NCScorp/teste-maroto.git']]
            )
        }
    }

    stage('Check dir'){
        sh "ls -lah"
    }
}