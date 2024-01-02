pipeline {  
 agent any 

 tools {nodejs "Node"}
 
 environment {
        // Define the site name
        iisSiteName = "TextUtils"
    }
  
 stages {  

  stage('Clean and Install Dependencies') {
    steps {
        sh 'npm cache clean --force'
        sh 'npm install --force'
    }
}
    
    stage('Build') {
        steps {
           sh 'npm run build'
           
        }
    }
    
      
   stage('Deploy in IIS') {
            steps {
               
                // Execute the PowerShell command to get PhysicalPath
                script {
                
               //  docker cp e3f6ebcaf6e4db3a1b289bbf43d201aa80b51555838fa83ecf5184d7ce5ec588:/var/jenkins_home/workspace/TextUtils-React_main/build C:\\inetpub\\wwwroot\\TextUtils
                  // sh 'cp -r C:\inetpub\wwwroot\TextUtils /var/jenkins_home/workspace/TextUtils-React_main/build'
                
                        // Copy from the image to the workspace
              
               sh ' cp C:/Jaimin/Text/* C:/Jaimin/wwwroot/TextUtils'
                    
                // Define the PowerShell copy command

                
                }
            }
        }
 }  
} 
