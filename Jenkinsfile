node {
    
    def customImage
    def REPOSITORY = 'conology_repository'
   
    
    environment {
        ACCESS_KEY = credentials("ACCESS_KEY")
        SECRET_ACCESS_KEY = credentials("SECRET_ACCESS_KEY")
        TEST = credentials("TEST")
        REGION = 'eu-central-1'
    }
    
    stage ('Test') {
        sh "echo ${env.TEST} ${env.REGION} ${REPOSITORY}"
    }
    /*stage ('Pull') {
      sh 'docker pull nginxdemos/hello'
    }*/
    
    /*stage ('Checkout'){
        checkout scm
    }
    stage ('Build'){
        
        sh 'echo Starting build of wordpress'
        customImage = docker.build("jhg_wordpress:${env.BUILD_ID}","./Wordpress")
    }
    stage ('Deploy') {
        
        sh 'echo Deploying Env'
        sh 'docker-compose up -d --build'    
    }
    
    stage ('Configure') {
        sleep 20
        sh 'docker exec -i JHG_wordpress sh -c "wp core install --url=http://localhost:8080 --title=Example --admin_user=supervisor --admin_password=strongpassword --admin_email=info@example.com --allow-root"'
        sh 'docker exec -i JHG_wordpress sh -c "wp plugin install talentlms --allow-root --activate"'
        sh 'docker exec -i JHG_wordpress sh -c "wp plugin install yada-wiki --allow-root --activate"'
    }
    stage('create images') {
        // here we need to save the running & configured containers to images
        sh 'docker commit JHG_wordpress jhg_wordpress_cloud'
    }*/
    
    /*stage('upload to ECR') {
        
        //login with user
        sh "aws configure set aws_access_key_id ${env.ACCESS_KEY}"
        sh "aws configure set aws_secret_access_key ${env.SECRET_ACCESS_KEY}"
        sh "aws configure set default.region ${env.REGION}"
        
        //one time job
        // create a jenkins-secret encrypted version of ~./aws
        // store that version in the repo under /credentials
        
        //every time
        // load these credentials and store them in the jenkins-blueocean image to have aws preconfigured
        
        //create the AWS repository
        sh "aws ecr create-repository --repository-name ${REPOSITORY} || true"
       
        //tag the docker images 
        //sh 'docker tag jhg_wordpress_cloud 586513809140.dkr.ecr.eu-central-1.amazonaws.com/automation/jhg_wordpress_cloud'
        //sh 'docker tag mysql:5.7 586513809140.dkr.ecr.eu-central-1.amazonaws.com/automation/mysql:5.7'
        sh 'docker tag nginxdemos/hello 586513809140.dkr.ecr.eu-central-1.amazonaws.com/hello'
        
        //get the token from AWS
        sh 'aws ecr get-login --no-include-email --region eu-central-1'
        //sh 'aws ecr get-login --no-include-email --region eu-central-1 | bash'
      
        //push the image 
       // sh 'docker push 586513809140.dkr.ecr.eu-central-1.amazonaws.com/hello'
      
    }
    stage('deploy AWS') {
        // here we push the freshly created images to AWS and execute them
        
        // ECS stuff in here!
    }*/
}
