pipeline{
  agent{
    label{
      label "built-in"
      customWorkspace "/mnt/data-q2"
    }
  }
    
    stages{
      stage ("Build and deploy") {
        steps{
                   dir ("/mnt/data-q2"){
                   
                       sh "docker pull httpd"
                       sh "docker run -itdp 81:80 --name server-q2 httpd"
                       sh "docker cp /mnt/data/index.html server-q2:/usr/local/apache2/htdocs/"
                    }
        }
      
      
    }
  
}
}
