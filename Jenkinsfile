 pipeline{

	 agent{
		  label 'LinuxBuildSlave1'
		   }
	 tools{
		   maven 'Maven'
		   jdk 'JAVA8' 

		   }
	 stages{
	   stage('Building the maven project'){
	     steps{
		   echo "Building "
		 
		 }
	   
	   }
	   stage('testing the maven '){
	     steps{
		 
		 echo "testing"
		 }
	   
	   }
	   stage('Package the project'){
	     steps{
		  echo "running packaing "
		 
		 }
	   
	   }
	   stage('running deployment'){
	     steps{
		  echo " deployment running"
		 
		 }
	   
	   }
	 
	 }
}
