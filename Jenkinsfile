 pipeline{

	 agent{
		  label 'LinuxBuildSlave1'
		   }
	 tools{
		   maven 'Maven'
		   jdk 'JAVA8' 
		   }

	 stages{
		stage('build the file in maven'){		  
			steps{
				mvn clean install
				  }   
		}
		 stage('stop tomcat'){		  
			steps{
				service tomcat8 stop
				  }
		}
		 stage('remove old war files'){
			steps{
			   rm -rf /var/lib/tomcat8/webapps/
				 }
		}
		 stage('copy new war file'){
			steps{
			   cp -f target/*.war /var/lib/tomcat8/webapps/		
				  }	 
	   }
		 stage('start tomcat'){	  
			steps{
				service tomcat8 start
				  }
		}
	}	   

}
