


pipeline {

	agent {
        label "master"
    }
 
    stages {
        stage("clone code") {
            steps {
                script {
			withMaven(maven:'mm'){
                    // Let's clone the source
				git 'https://github.com/ikramBej/hello-world-greeting.git';}
                }
            }
        }
        stage("mvn build") {
            steps {
                script {
                    // If you are using Windows then you should use "bat" step
                    // Since unit testing is out of the scope we skip them
			withMaven(maven:'mm'){
				bat "mvn package -DskipTests=true"}
                }
            }
        }
	    
        stage("mvn clean install ") {
            steps {
                script {
                    // If you are using Windows then you should use "bat" step
                    // Since unit testing is out of the scope we skip them
			withMaven(maven:'mm'){
				bat "mvn clean"}
                }
            }
        }
        stage("mvn test ") {
            steps {
                script {
                    // If you are using Windows then you should use "bat" step
                    // Since unit testing is out of the scope we skip them
			withMaven(maven:'mm'){
				bat "mvn test"}
                }
            }
        }
	    
	    
	    
	    
	    
	   
        
        
     
	    
	    
	    
        
        
    
        
        
       
}

}
