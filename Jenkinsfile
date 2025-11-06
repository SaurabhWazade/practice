pipeline {
  agent {
    label {
      label "QA1"
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
        sh "sudo docker run -dp --name s1 httpd"
      }
    }
    stage ('three') {
      steps {
        sh "sudo git clone "
      }
    }
    stage ('four') {
      steps {
        sh '''sudo docker cp /root/.jenkins/workspace/js1/index.html s1:/usr/local/apache2/htdocs/
        sudo docker exec s1 sh -c "chmod 644 /usr/local/apache2/htdocs/index.html"'''
      }
    }
  }
}
