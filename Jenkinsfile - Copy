node { 
currentBuild.result = "SUCCESS" 
try { 
stage('Checkout'){ 
checkout scm 
                 }
    }

 catch (err) { 
currentBuild.result = "FAILURE" 
mail body: "project build error is here: ${env.BUILD_URL}" , 
from: 'mahesh288646@gmail.com', 
replyTo: 'mahesh288646@gmail.com', 
subject: 'project build failed', 
to: 'mahesh288646@gmail.com' 
throw err 
} 
             




} 
