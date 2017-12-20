node('master') {
  
  checkout([$class: 'GitSCM', branches: [[name: '*/master']], browser: [$class: 'GithubWeb', 
  repoUrl: 'https://github.com/Swaty0908/jenkinsPipelineBuildTestDeploy'], doGenerateSubmoduleConfigurations: false,
  extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/Swaty0908/jenkinsPipelineBuildTestDeploy.git']]])
  
   bat 'mvnw cmd clean install'
  
   bat '''cd docker
cd internal-db
docker build -t spring-petclinic .'''
  
   
   
}
