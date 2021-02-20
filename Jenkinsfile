node {
    stage('Checkout SCM') {
        git branch: 'master', url: 'https://github.com/jayeshwani0025/angulr-app.git'
    }

    stage('Install node modules') {
        sh "npm install"
    }

    stage("Test") {
        sh "npm run test-headless"
    }

    stage("Build") {
        sh "npm run build --prod"
    }
    
    stage("Copy") {
        sh "cp -a /var/lib/jenkins/workspace/angular-pipeline/dist/angulr-app/. /var/www/angulr-app/html/"
    }
}
