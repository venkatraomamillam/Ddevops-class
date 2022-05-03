pipeline {
    
	agent any
/*	
	tools {
        maven "maven3"
    }
*/	
    
	
    stages{
        
        stage('BUILD'){
            steps {
                bat 'D:/Maven/maven/maven/bin/mvn clean install -DskipTests'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }    

	    
}
