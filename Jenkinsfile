pipeline {
    agent any
    stages {
stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean install -s /opt/setting.xml'
            }
        }

stage('Nexus Lifecycle Analysis') {
steps {
nexusPolicyEvaluation iqApplication: 'mytest', iqStage: 'build'
}
}
}

}
