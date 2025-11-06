pipeline {
  agent {
    label {
      label "QA3"
    }
  }
  stages {

    stage ('one') {
      steps {
        sh """ sudo yum install docker -y
        sudo systemctl start httpd"""
        
      }
    }
    stage ('two') {
      steps {
        sh "sudo docker run -dp 80:80 --name s1 httpd"
      }
    }
    stage ('three') {
      steps {
        sh "sudo git clone "
      }
    }
    stage ('four') {
      steps {
        sh '''sudo docker cp /root/.jenkins/workspace/js3/index.html s1:/usr/local/apache2/htdocs/
        sudo docker exec s1 sh -c "chmod 644 /usr/local/apache2/htdocs/index.html"'''
      }
    }
  }
