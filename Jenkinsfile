pipeline {
   agent any
    
   stages {
      
      // Execute when branch = 'main'
      stage("Main Branch deployment") {
         when {
		    branch 'main'
		 }
         steps {
            withKubeConfig([credentialsId: 'kubectl-wordpress', serverUrl: 'https://devops2:6443']) {
               sh 'kubectl apply -f ./kubernetes'
            }
         }
      }
  
   }
}