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
                       sh "docker run -itdp 90:80 --name server-0 httpd"
                       sh "docker cp /mnt/data/index.html server-0:/usr/local/apache2/htdocs/"
                    }
        }
      
      
    }
  
}
}
