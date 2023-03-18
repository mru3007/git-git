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
                       sh "docker run -itdp 80:80 --name server-2 httpd"
                       sh "docker cp /mnt/data/index.html server-2:/usr/local/apache2/htdocs/"
                    }
        }
      
      
    }
  
}
}
