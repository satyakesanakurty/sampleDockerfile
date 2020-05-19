pipeline
{
  agent any
  stages
  {
    stage('Deploy to satya branch')
    {
      when{
        branch 'satya'
      }
      steps
      {
       sh """
        echo "enter a var name"
        read var
        echo "you have entered"
        echo $var
       """
      }
    }
  }
}
