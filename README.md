# first-pipeline-to-promotion

print_greetings
  print the pipeline id
  print hello world
  print the environment variables
create_infrastructure
  create the ec2 instance by cloudformation stack named after the workflow id digits 0 to 5
upload_file
  describe the ec2 instance to obtain the instance public ip
  store it in the inventory file and persist to workspace
configure_infrastructure
  install ansible and its dependencies
  configure the ec2 instance using ansible that installs a javascript website listening on port 3000
smoke_test
  curl the website successfully then continue if unsuccessful then destroy the environment deleting the ec2 instance
create_and_deploy_front_end
  create the s3 bucket and copy the repository to it.
get_last_deployment_id
  obtain the pipeline id
promote_to_production
  create the cloudfront distribution pointing to the s3 bucket.

n
