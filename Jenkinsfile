pipeline{
  agent{
    label{
      label "built-in"
      customWorkspace "/mnt/data-q3"
    }
  }
    
    stages{
      stage ("Build and deploy") {
        steps{
                   dir ("/mnt/data-q3"){
                   
                       sh "docker pull httpd"
                       sh "docker run -itdp 82:80 --name server-q3 httpd"
                       sh "docker cp /mnt/data/index.html server-q3:/usr/local/apache2/htdocs/"
                    }
        }
      
      
    }
  
}
}
