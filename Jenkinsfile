node{
    def name = "vikas"
    def mvnHome = tool name: 'Maven_home', type: 'maven'
    echo "welcome to ${name}"
    
        stage('SCM Checkout'){
        git branch: 'main', credentialsId: 'Git-cred', url: 'https://github.com/vikas99341/my-maven-app.git'
    }
        stage('Compile'){
        sh "${mvnHome}/bin/mvn  compile"
    }    
        stage('Test'){
        sh "${mvnHome}/bin/mvn  test"
    }    
        stage('Package'){
        sh "${mvnHome}/bin/mvn  package"
    }    

}
