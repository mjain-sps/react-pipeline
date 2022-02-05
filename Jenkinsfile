pipeline {
     agent any
     stages {
        stage("install") {
            steps {
                sh "sudo npm install"
            }
        }
        stage("build"){
                sh "sudo npm run build"
        }
        stage("Deploy") {
            steps {
                sh "sudo rm -rf /var/www/jenkins-react-app"
                sh "sudo cp -r ${WORKSPACE}/build/ /var/www/jenkins-react-app/"
            }
        }
    }
}
