node('with-docker-compose')  {
    
    stage('Check env') { 
        sh 'pwd'
        sh 'ls -la'
    }
    
    stage('Docker-Compose Up') {
		sh 'docker-compose up -d'
    }
    
    stage('User input') {
        input message: 'Paused before tear-down '
    }
        
    stage('Docker-Compose Down') {
        sh 'docker-compose down -v'
    }
 
}
