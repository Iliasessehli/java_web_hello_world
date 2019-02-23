node {
stage('prepare'){
    checkout scm
    // use for non multibranch: git 'https://github.com/amuniz/maven-helloworld.git'
    

}


stage('package'){
    def mvnHome = tool 'maven_3.6.0'
    bat "${mvnHome}\\bin\\mvn clean package"

}
stage('deploy'){
    def mvnHome = tool 'maven_3.6.0'
    bat "${mvnHome}\\bin\\mvn clean deploy"

}
stage('deploy tomcat'){
   
    bat "target\\bin\\webapp.bat"

}

}
