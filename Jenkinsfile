stage('git_sync') {
    node {
        echo 'aaa'
        git branch: 'feature/sprint71', credentialsId: 'ff2dee19-1563-4907-ad75-d9213327ecd2', url: 'https://git.it.bbraun.net/scm/pc/product-center-5.git'
        withAnt (installation: 'A110') {
            if (isUnix()) {
              sh "ant -Dhttps.proxyHost=fra1.sme.zscalertwo.net -Dhttps.proxyPort=9480 -buildfile hybris/build/build.xml install"
            } else {
              bat "ant -Dhttps.proxyHost=fra1.sme.zscalertwo.net -Dhttps.proxyPort=9480 -buildfile hybris/build/build.xml install"
            }
        }
        echo 'bbbb'
    }
}
