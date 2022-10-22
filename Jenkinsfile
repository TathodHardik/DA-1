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
			   
			   sh"docker system prune -a -f "
		      sh"docker run --name httpdcontainor1 -itdp 8083:80 httpd"
              sh"docker cp index.html httpdcontainor1:/usr/local/apache2/htdocs/ "
			  
		   }
		}
	 }	 
	 
}
