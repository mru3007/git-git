pipeline{
  agent{
    label{
      label "built-in"
      customWosrkspace "/mnt/data"
    }
  }
    
    stages{
      stage ("Build") {
        steps{
              docker pull httpd
              cp /mnt/data/index.html /usr/local/apache2/htdocs
       }
      }
      
      stage ("deploy"){
        steps{
              docker run -itdp 80:80 --name httpd httpd
        }
      }
  
    }
  
}
