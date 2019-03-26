node {
   stage('Git Access'){
       git 'https://github.com/Ashuxyz/MyAppDemo'
   }
   stage('build'){
       def buildtool = tool name: 'maven', type: 'maven'
       sh "$buildtool/bin/mvn install"
   }
   stage('deploy'){
       sh "cp target/MyAppDemo.war /var/lib/tomcat8/webapps/"
   }
   stage('success'){
        'archiveArtifacts'
   }
}
