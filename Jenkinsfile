pipeline {
  agent {
    label {
      label "QA2"
    }
  }
  stages {

    stage ('one') {
      steps {
        sh """ sudo yum install docker -y
        sudo systemctl start docker"""
        
      }
    }
    stage ('two') {
      steps {
        sh "sudo docker run -dp 80:80 --name s1 httpd"
      }
    }
    stage ('three') {
      steps {
        sh "sudo git clone https://github.com/SaurabhWazade/practice.git"
      }
    }
    stage ('four') {
      steps {
        sh '''sudo docker cp /mnt/jenkins-slave/workspace/js2/index.html s1:/usr/local/apache2/htdocs/
        sudo docker exec s1 sh -c "chmod 644 /usr/local/apache2/htdocs/index.html"'''
      }
    }
  }
}
