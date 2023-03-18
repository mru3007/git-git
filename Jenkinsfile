pipeline{
  agent{
    label "built-in"
  }
    
    stages{
      stage ("Build") {
        steps{
              docker build ("-t httpd:1.0")               
       }
      }
      
      stage ("deploy"){
        steps{
              docker run ("-itdp 80:80 --name httpd httpd:1.0")
        }
      }
  
    }
  
}
