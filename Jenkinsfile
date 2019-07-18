properties([
    pipelineTriggers([
        issueCommentTrigger('.*test this please.*')
    ])
])
node {
   stage('Build') {
     sh ' env | sort'
       if (env.CHANGE_ID) {
                pullRequest.addLabel(['Build Failed'])
            }
   }
}
