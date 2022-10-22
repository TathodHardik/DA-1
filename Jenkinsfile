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
		      sh"docker run --name httpdcontainor4 -itdp 80:90:80 httpd"
              sh"docker cp index.html httpdcontainor:/usr/local/apache2/htdocs/ "
			  
		   }
		}
	 }	 
	 
}
