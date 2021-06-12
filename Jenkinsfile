pipeline {
    agent {
node {
label 'master'
}
}
    stages {
        stage('scm') {
            steps {
            git branch: 'main', credentialsId: 'e32f1dd7-551d-42af-a4eb-8ee0718b97bf', url: 'https://github.com/madhavibonugowlla/vamseeeee.git'}
        }
    stage('build') {
        steps {
            sh '''
            echo "this is for maven builds"
            pwd
            ls
            cd com.fb
	    ls -ll
            mvn clean
            mvn compile
            '''
        }
    }
    stage('test_cases') {
        steps {
            sh '''
            echo "this is for sonarstage"
	    ls -ll
            mvn test
            '''
        }
    }
    stage('package') {
        steps {
            sh '''
            echo "this is for sonarstage"
	    ls -ll
            mvn package
            '''
        }
    }
    stage('sonar') {
        steps {
            sh '''
            echo "this is for sonarstage"
	    ls -ll
            mvn sonar:sonar
            '''
        }
    }
    stage('jfrog') {
        steps {
            sh '''
            echo "this is for jfrog-stage"
	    ls -ll
           
            '''
        }
    }
    }
}
