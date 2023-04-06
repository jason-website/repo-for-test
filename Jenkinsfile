pipeline{
agent any 
    triggers {
    GenericTrigger(
            genericVariables: [
                    [key: 'commit', value: '$.commits[0].id'],
                    [key: 'committer', value: '$.commits[0].committer.name'],
                    [key: 'ref', value: '$.ref']
            ],
            token: 'test',
            causeString: 'Triggered by github webhook on commit $commit to $ref by $committer',
            printContributedVariables: true,
            printPostContent: true
    )
  }
stages{
stage("build"){
steps{
 echo 'this is a build'
     }
               }
       }
}
