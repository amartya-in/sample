pipeline {
environment {
BUILD_SCRIPTS_GIT="https://github.com/amartya-in/sample.git"
BUILD_SCRIPTS='mypipeline'
BUILD_HOME='/Users/ayush/jenkins-my/'
}
agent any
stages {
stage('Checkout: Code') {
steps {
sh "mkdir -p $BUILD_HOME/repo; \
git clone $BUILD_SCRIPTS_GIT repo/$BUILD_SCRIPTS; \
sh chmod -R +x $BUILD_HOME/repo/$BUILD_SCRIPTS"
}
}
stage('build') {
steps {
sh "$BUILD_HOME/mypipeline/build.sh"
}
}
}
post {
always {
cleanWs()
}
}
}
