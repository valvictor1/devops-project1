node {

    withMaven(maven:'maven') {

        stage('Checkout') {
            git url: 'https://github.com/valvictor1/devops-project1.git', credentialsId: 'valvictor1', branch: 'master'
        }

        stage('Build') {

            **dir('project-dir') {**
                sh 'mvn clean install'

                def pom = readMavenPom file:'pom.xml'

                print pom.version
                env.version = pom.version
            }
        }
    }
}


