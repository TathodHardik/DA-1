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
			   sh"docker stop httpdcontainor3"
			   sh"docker system prune -a -f "
		      sh"docker run --name httpdcontainor3 -itdp 90:80 httpd"
              sh"docker cp index.html httpdcontainor3:/usr/local/apache2/htdocs/ "
			  
		   }
		}
	 }	 
	 
}
