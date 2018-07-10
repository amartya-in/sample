pipeline {

environment {

BUILD_SCRIPTS_GIT="https://github.com/amartya-in/sample.git"

BUILD_SCRIPTS='mypipeline'

BUILD_HOME='/Users/ayush/jenkins-my/workspace/'

}

agent any

stages {

stage('Checkout: Code') {

steps {

sh "mkdir -p $BUILD_HOME/repo;\


git clone $BUILD_SCRIPTS_GIT repo/$BUILD_SCRIPTS"

sh "chmod -R +x $WORKSPACE/repo/$BUILD_SCRIPTS"

}

}

stage('build') {
	sh "$BUILD_HOME/mypipeline/build.sh"

steps {


}

}

}

post {

always {


}

}

}
