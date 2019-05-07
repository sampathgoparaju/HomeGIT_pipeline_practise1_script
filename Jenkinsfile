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
		   sh 'mvn clean install'
		 
		 }
	   
	   }
	   stage('stop tomcat cat'){
	     steps{
		  sh 'service tomcat8 stop'
		 
		 }
	   
	   }
	   stage('copy war'){
	     steps{
		  sh 'cp -f target/*.war /var/lib/tomcat8/webapps/demo.war'
		 
		 }
	   
	   }
	   stage('start tomcat'){
	     steps{
		  sh 'service tomcat8 start'
		 
		 }
	   
	   }
	 
	 }
}
