pipeline {
    agent any
    triggers {
        pollSCM "* * * * *"
    }
    stages {
        stage ("terraform init") {
            steps {
                sh ('terraform init')
            }
        }

        stage ("terraform Action") {
            steps {
                sh ('terraform apply --auto-approve')
           }
        }
    }
}
