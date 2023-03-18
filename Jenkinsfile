pipeline{
  agent any
    
    stages{
      stage ("Build") {
              docker build ("-t httpd:1.0")               
      }
      
      stage ("deploy"){
              docker run ("-itdp 80:80 --name httpd httpd:1.0")
           
      }
  
    }
  
}
