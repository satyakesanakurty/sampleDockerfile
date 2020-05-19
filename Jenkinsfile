pipeline
{
  agent
  {any}
  stages
  {
    stage('Deploy to satya branch')
    {
      when{
        branch 'satya'
      }
      steps
      {
        def uerInput = input(
        id: 'userInput', message: 'enter your cron exp',
        paramaters : [string(defaultValue: 'None'),]
        )
        echo "you have entered ${userInput}"
      }
    }
  }
}
