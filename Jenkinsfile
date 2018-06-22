node {
    stage('checkout') {
        dir('module-a') {
            git url: 'https://github.com/jordanglassman/forrester-module-a.git'
        }
        dir('module-b') {
            git url: 'https://github.com/jordanglassman/forrester-module-b.git'
        }
    }
    stage('build') {
        dir('module-a') {
            withMaven(maven: 'Maven350') {
                sh "mvn clean package"
            }
        }
        dir('module-b') {
            withMaven(maven: 'Maven350') {
                sh "mvn clean package"
            }
        }
    }
}