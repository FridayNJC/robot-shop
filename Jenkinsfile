pipeline{
  agent any
  stages{
    stage('Cloaning our git'){
      steps {
          git 'https://github.com/FridayNJC/robot-shop.git/'
      }
    }
    stage("build"){
      steps{
        sh 'docker build -t nileshchudasama/cart:v1 ./cart'
        sh 'docker push nileshchudasama/cart:v1'
        sh 'docker rmi -f $(docker images -a -q)'
        sh 'docker build -t nileshchudasama/catelouge:v1 ./catelouge'
        sh 'docker push nileshchudasama/catelouge:v1'
        sh 'docker rmi -f $(docker images -a -q)'
        sh 'docker build -t nileshchudasama/dispatch:v1 ./dispatch'
        sh 'docker push nileshchudasama/dispatch:v1'
        sh 'docker rmi -f $(docker images -a -q)'
        sh 'docker build -t nileshchudasama/load-gen:v1 ./load-gen'
        sh 'docker push nileshchudasama/load-gen:v1'
        sh 'docker rmi -f $(docker images -a -q)'
        sh 'docker build -t nileshchudasama/mongo:v1 ./mongo'
        sh 'docker push nileshchudasama/mongo:v1 ./mongo'
        sh 'docker rmi -f $(docker images -a -q)'
        sh 'docker build -t nileshchudasama/mysql:v1 ./mysql'
        sh 'docker push nileshchudasama/mysql:v1'
        sh 'docker rmi -f $(docker images -a -q)'
        sh 'docker build -t nileshchudasama/payment:v1 ./payment'
        sh 'docker push nileshchudasama/payment:v1'
        sh 'docker rmi -f $(docker images -a -q)'
        sh 'docker build -t nileshchudasama/ratings:v1 ./ratings'
        sh 'docker push nileshchudasama/ratings:v1'
        sh 'docker rmi -f $(docker images -a -q)'
        sh 'docker build -t nileshchudasama/shipping:v1 ./shipping'
        sh 'docker push nileshchudasama/shipping:v1'
        sh 'docker rmi -f $(docker images -a -q)'
        sh 'docker build -t nileshchudasama/user:v1 ./user'
        sh 'docker push nileshchudasama/user:v1'
        sh 'docker rmi -f $(docker images -a -q)'
        sh 'docker build -t nileshchudasama/web:v1 ./web'
        sh 'docker push nileshchudasama/web:v1'
        sh 'docker rmi -f $(docker images -a -q)'
      }
    }
    stage("test"){
      steps{
        echo "testing the application.."
      }
    }
    stage("deploy"){
      steps{
        echo "deploing the application.."
      }
    }
  }
}
