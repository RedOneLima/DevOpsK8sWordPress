pipeline {
   agent any
    
   stages {
      
      // Execute when branch = 'main'
      stage("Main Branch deployment") {
         when {
		    branch 'main'
		 }
         steps {
            sh 'kubectl apply -f ./kubernetes'
         }
      }
  
   }
}