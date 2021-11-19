pipeline {
    agent any
    // { dockerfile true }
    // environment {
    //     appName = 'jenkins-blog'

    //     KEY_PASSWORD = credentials('android')
    //     KEY_ALIAS = credentials('androiddebugkey')
    //     KEYSTORE = credentials('debug.keystore')
    //     STORE_PASSWORD = credentials('android')
    //     APPCENTER_API_TOKEN = credentials('AppcenterApiToken')

    // }
    stages {
        stage('Run Tests') {
            steps {
                echo 'Running Tests'
                // script {
                //     // VARIANT = getBuildType()
                //     sh "./gradlew test${VARIANT}UnitTest"
                // }
            }
        }
        stage('Build Bundle') {
            // when { expression { return isDeployCandidate() } }
            steps {
                echo 'Building'
                // script {
                //     // VARIANT = getBuildType()
                //     sh "./gradlew -PstorePass=${STORE_PASSWORD} -Pkeystore=${KEYSTORE} -Palias=${KEY_ALIAS} -PkeyPass=${KEY_PASSWORD} bundle${VARIANT}"
                // }
            }
        }
        // stage('Deploy App to Appcenter Distribute') {
        //     // when { expression { return isDeployCandidate() } }
        //     steps {
        //         appCenter 
        //         //apiToken: '9d5011324c537e7963eb6b156738f2dfe3a70b5f',
        //         apiToken: "${APPCENTER_API_TOKEN}"
        //         ownerName: 'uat.xspring@gmail.com',
        //         appName: 'XPG-FINANCE-ANDROID',
        //         pathToApp: "**/outputs/bundle/${VARIANT.toLowerCase()}/*.aab",
        //         distributionGroups: 'Collaborators',
        //         releaseNotes:"For uat issue 25/10/2021",
        //     }
            // steps {
            //     echo 'Deploying'
            //     script {
            //         VARIANT = getBuildType()
            //         TRACK = getTrackType()

            //         if (TRACK == Constants.RELEASE_TRACK) {
            //             timeout(time: 5, unit: 'MINUTES') {
            //                 input "Proceed with deployment to ${TRACK}?"
            //             }
            //         }

            //         try {
            //             CHANGELOG = readFile(file: 'CHANGELOG.txt')
            //         } catch (err) {
            //             echo "Issue reading CHANGELOG.txt file: ${err.localizedMessage}"
            //             CHANGELOG = ''
            //         }

            //         androidApkUpload googleCredentialsId: 'play-store-credentials',
            //                 filesPattern: "**/outputs/bundle/${VARIANT.toLowerCase()}/*.aab",
            //                 trackName: TRACK,
            //                 recentChangeList: [[language: 'en-US', text: CHANGELOG]]
            //     }
            // }
        }
    }
