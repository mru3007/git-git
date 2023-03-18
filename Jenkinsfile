pipeline{
  agent{
    label{
      label "built-in"
      customWorkspace "/mnt/data"
    }
  }
    
    stages{
      stage ("Build and deploy") {
        steps{
                   dir ("/mnt/data"){
                     agent{
                               docker {pull 'httpd'}
                     }    
                       sh "cp /mnt/data/index.html /usr/local/apache2/htdocs "
       }
      }
      }
      
      stage ("deploy"){
        steps{
                   agent{
                   docker run {'-itdp 80:80 --name httpd httpd'}
                  }
          }
      }
  
    }
  
}
