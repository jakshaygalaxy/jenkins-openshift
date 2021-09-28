pipeline {
    agent {
        node { label 'jenkins-slave' }
    }
    stages {
        stage('Build') {
            agent { dockerfile true }
            steps {
              	sh 'oc login --token=sha256~IGjYjwEWixCSlZnsrnMkoZ5n04VmWZ-UHJh4fvEO_UI --server=https://api.sandbox-m2.ll9k.p1.openshiftapps.com:6443'
		sh 'oc get all -o name'
            }
        }
    }
}
