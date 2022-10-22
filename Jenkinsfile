pipeline{
     agent {
	      label{
		    label'built-in'
	   }
	 }
     stages{
	    stage('create_image'){
		   steps
		   {
			   sh"chmod 777 index.html"
			   sh"docker stop httpdcontainor"
			   sh"docker system prune -a -f "
		      sh"docker run --name httpdcontainor -itdp 8080:80 httpd"
              sh"docker cp index.html httpdcontainor:/usr/local/apache2/htdocs/ "
			  
		   }
		}
	 }	 
	 
}
