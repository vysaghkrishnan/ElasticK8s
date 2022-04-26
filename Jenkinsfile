pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
            checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/vysaghkrishnan/ElasticK8s.git']]])  
     stages {
	 stage("terraform init") {
            steps {
                sh ('terraform init') 
            }
        }
        
        stages {
	    stage ("terraform Action") {
              steps {
                echo "Terraform action is --> ${action}"
                sh ('terraform ${action} --auto-approve') 
           }
        }
    }
   }
}
}

}
}
