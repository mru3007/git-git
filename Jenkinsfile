pipeline{
  agent any{
    stages{
      Stage (Build) {
              docker build -t httpd                
      }
      
      stage (deploy){
              docker run -itdp 80:80 --name httpd httpd
           
      }
  
    }
  }
}
