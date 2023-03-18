pipeline{
  agent any
    stages{
      Stage (Build) {
              docker build -t httpd:1.0                
      }
      
      stage (deploy){
              docker run -itdp 82:80 --name httpd httpd:1.0
           
      }
  
    }

}
