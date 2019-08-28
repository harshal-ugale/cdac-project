pipeline{agent any 
  stages{ stage('Clone Repo') 
          { steps 
                  { sh "export AWS_DEFAULT_REGION=us-east-1"
                    sh "aws cloudformation create-stack --stack-name ${stackname} --template-body file://rds.json --region 'us-east-1' --parameters ParameterKey='DBUser',ParameterValue=${dbusername} ParameterKey='DBPassword',ParameterValue=${dbpassword},ParameterKey='DBInstanceIdentifier',ParameterValue=${dbInstancesIdentifier}" 
           }
         }
      }
}
