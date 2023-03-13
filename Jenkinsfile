node('aws-codebuild'){

    stage('Clean') {
        deleteDir()
    }

    stage('Checkout') {
			
        timeout(time: 3600, unit: 'SECONDS') {
            checkout scm: scmGit(userRemoteConfigs: [
                [ 
                    credentialsId: 'JenkinsCheckoutHTTPS',
                    url: 'https://github.com/NCScorp/teste' 
                ]
            ])
        }
    }

    stage('Check dir'){
        sh "ls -lah"
    }
}