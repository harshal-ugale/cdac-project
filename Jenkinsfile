pipeline{agent any 
  stages{ stage('Clone Repo') 
          { steps 
                  { sh "export AWS_DEFAULT_REGION=us-east-1"
                   sh "aws cloudformation create-stack --stack-name ${stackname} --template-body file://rds.json --parameters ParameterKey='DBInst',ParameterValue='${dbinst}' ParameterKey='MasterUser',ParameterValue='${masteruser}' ParameterKey='MasterPass',ParameterValue='${masterpass}' --region 'us-east-1'"
                  }
           }
         }
      }