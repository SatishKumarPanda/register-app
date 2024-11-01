pipeline {
  agent {
    label 'Test'
  }
  tools {
   jdk 'jdk17'
  maven 'maven3'
  }
  stages {
    stage ("git checkout"){
      step{
        echo "git work"
      }
    }
    stage ("cleanup workspace"){
      step{
        cleanWSs()
      }
    }
  }
}
