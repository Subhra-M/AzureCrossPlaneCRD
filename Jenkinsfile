pipeline {
agent any
    stages {
    stage('Set Build Name') {
      steps { 
        echo "Set Build Name"        
          echo("Crossplane")
          script { 
            currentBuild.displayName = "${BUILD_NUMBER}"
            currentBuild.description = "${GIT_COMMIT}"    
            sh '''#!/bin/bash
	   # alias kubectl=/usr/local/bin/kubectl
	    #echo "current context ---- "
	    #kubectl config current-context
	    echo "Applying crd ---- "
	    #kubectl apply -f defination.yml
	    #kubectl apply -f composition.yml
	     #kubectl apply -f claim.yaml
	     kubernetesDeploy(configs: "defination.yml", kubeconfigId: "7f0f69b6-5897-4729-af64-cd38ae605003")
	     
		'''
        }
      }
    } 
 }
}
