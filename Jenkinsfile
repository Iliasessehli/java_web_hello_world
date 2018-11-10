node {
stage('prepare'){
    checkout scm
    // use for non multibranch: git 'https://github.com/amuniz/maven-helloworld.git'
    

}
stage('mvn packege'){
    def mvnHome = tool 'maven 3.5.4'
    bat "${mvnHome}/bin/mvn clean package"

}
stage('deploy tomcat'){
   
    bat "target\bin\webapp.bat"

}

}
