def buildClosure = {
  def nodeHome = tool name: 'nodejs-10.13.0', type: 'jenkins.plugins.nodejs.tools.NodeJSInstallation'
  env.PATH = "${nodeHome}/bin:${env.PATH}"

  stage('Install')
  sh 'yarn'

  stage('Lint')
  sh 'yarn lint'

  stage('Test')
  // --watchAll=false is hack to stop jest from watching forever
  // (see https://github.com/facebook/create-react-app/issues/784#issuecomment-392497169)
  sh 'yarn test -- --coverage --watchAll=false'

  stage('Build')
  sh 'yarn build'
}

def buildParameterMap = [:]
buildParameterMap['appName'] = 'chuck-norris-app'
buildParameterMap['buildClosure'] = buildClosure
buildParameterMap['namespaces'] = ['nebm-dev']
buildParameterMap['namespacesWithApproval'] = ['nebm-prd']

buildAndDeployGeneric(buildParameterMap)

// vim: ft=groovy
