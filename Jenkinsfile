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
                   
                       sh "docker pull httpd"
                       sh "docker run -itdp 80:80 --name server-1 httpd"
                       sh "cp /mnt/data/index.html /usr/local/apache2/htdocs/"
                    }
        }
      
      
    }
  
}
}
