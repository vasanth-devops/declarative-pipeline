pipeline {
    agent any
	
    stages {
        stage('One') {
                steps {
                        echo 'Hi, this is Vasanth...'
			
                }
        }
	    stage('Two'){
		    
		steps {
			input('Do you want to proceed?')
        }
	    }
        stage('Three') {
                when {
                        not {
                                branch "master"
                        }
                }
                steps {
			echo "Hello"
                        }
        }
        
    }
	agent {
    		dockerfile {
            		args "-v /tmp:/tmp -p 8000:8000"
    }
}
}

