pipeline {
    agent{
	label{
            label 'built-in'
             customWorkspace "/mnt/Assignment"			
	}
	}
	stages {
	stage ('clone repo 22q1'){
	steps {
	   dir ('/mnt/Assignment/22q1'){ 
	   sh "rm -rf *"
	   sh "sudo git clone https://github.com/Jbundile/Assignment.git -b 22q1"
	   }
	}
   }
	stage ('clone repo 22q2'){
	steps {
	   dir ('/mnt/Assignment/22q2'){ 
	   sh "rm -rf *"
	   sh "sudo git clone https://github.com/Jbundile/Assignment.git -b 22q2"
	   }
	}
	}
	stage ('clone repo 22q3'){
	steps {
	   dir ('/mnt/Assignment/22q3'){ 
	   sh "rm -rf *"
	   sh "sudo git clone https://github.com/Jbundile/Assignment.git -b 22q3"
	   }
	}
	}
	stage ('copy index file to docker container'){
	steps{
	      sh "chmod -R 777 /mnt"
		  sh "docker cp /mnt/Assignment/22q1/Assignment/index.html f29fc06549ea:/usr/local/apache2/htdocs"
		  sh "docker cp /mnt/Assignment/22q2/Assignment/index.html 0e747fc85e3b:/usr/local/apache2/htdocs"
		  sh "docker cp /mnt/Assignment/22q3/Assignment/index.html d56d06276d82:/usr/local/apache2/htdocs"
	}
	
	}
}
}
