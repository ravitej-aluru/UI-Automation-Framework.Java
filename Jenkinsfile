node {
    stage('Checkout') {
        echo 'Checking out files...'
        checkout scm
        //checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/ravitej-aluru/UI-Automation-Framework.Java.git']]])
    }
    stage('Build') {
        echo 'Building....'
        sh returnStdout: true, script: 'mvn clean compile'
    }
    stage('Test') {
        echo 'Testing....'
        sh returnStdout: true, script: 'mvn clean test'
    }
    stage('Deploy') {
        echo 'Deploying....'
    }
}