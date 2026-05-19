pipeline{
  agent any
  tools {
    maven 'Maven'
    jdk 'jdk'
  }
  stages {
stage('Checkout') {
steps {
git branch:'master', url:'https://github.com/RachanaN-27/gradle-jenkins.git'
}
}
    stage('Build') {
  steps {
sh 'gradle build'
  }
    }
    stage('Test') {
  steps {
sh 'gradle test'
  }
    }
    stage('Run Application') {
  steps {
sh 'gradle run'
  }
    }
  }
  post{
success{
echo "build success maga"
}
    failure{
echo "build fali maga sorry"
    }
  }
}
