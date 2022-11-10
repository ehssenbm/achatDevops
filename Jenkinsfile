pipeline{
    agent any

    stages{


        stage('Cloning from GitHub') {
                steps {
                    git branch: 'main', url: 'https://github.com/ehssenbm/achatDevops.git'
                }
                
            }
      
      stage('Clean'){
            steps {
                sh 'mvn clean '
            }
            
        }
        stage('Compile'){
            steps {
                sh 'mvn compile -DskipTests'
            }
            
        }
        
        
       /* stage('UNIT test'){
            steps{
                sh 'mvn test'
            }
        }

         stage('SonarQube Analysis'){
                steps {
                    sh """mvn sonar:sonar -DskipTests \
                            -Dsonar.language=java \
                             
                            
                    """
                }
                
            }
        
        
        
        
      stage('Nexus'){
            steps{
                sh 'mvn deploy -DskipTests'
            }
        }
        
        stage('Build Docker Image') {
            steps {
                script {
                        sh """ docker build -t ehssen/achat ."""
                    
                  
                }
            }
        }   
       */

        
        stage('Login') {
            steps{
                
                sh """ docker login -u "ehssen" -p "ehssen123" docker.io  """
            }
        }
        
        
        
        
        
       stage('push to DockerHub') {
            steps{

                sh """ docker push  ehssen/achat """
                
            }
        }
        
       
        
        
        
        
        
       
        
        
       


    }
}
