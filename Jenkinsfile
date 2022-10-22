pipeline{
     angent {
	      label'built-in'
	 }
     stages{
	    stage('create_image'){
		   steps
		   {
		      sh"docker run --name httpdcontainor -itdp 81:80 httpd"
              sh"docker cp index.html httpdcontainor:/usr/local/apache2/htdocs/ "
			  
		   }
		}
	 }	 
	 
}
