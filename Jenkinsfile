pipeline {
    agent any
    stages {
        stage ("Harish SCM") {
            steps {
                git branch: 'main', credentialsId: 'b1d44588-85de-4657-a639-89a34c835a30', url: 'https://github.com/naveenchowdary415/Girish12345.git'
            }
        }
        stage ("Harish_BUILD") {
            steps {
                bat "mvn install"
            }
        }
        stage ("Harish_deployment") {
            steps {
                deploy adapters: [tomcat8(credentialsId: '7759e1cb-1e15-4f4c-b127-297f174bf0b2', path: '', url: 'http://3.137.173.92:8090')], contextPath: null, war: '**/*.war'
            }
        }
    }
}
