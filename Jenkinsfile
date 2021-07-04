 pipeline {
           agent any
           stages {
                stage("Read File") {
                     steps {
                          script{
                                          
                          def data3 = readFile "file.txt"
	                  println(data3)
				  
				 def array3 = readJSON text:data3
				  println(array3)
				userInput1 = input(
				message: 'What are we deploying today?', ok : "Deploy", id :'DB_id',
				parameters:[choice(name: 'Param1' ,choices : array3.name, description: "Select a database to your choice")]
				)
				
				  
			  }
                     }	
                }
           }
      }
