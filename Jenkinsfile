pipeline
{
    agent any

    stages
    {
        stage ('Compile Stage')
        {
            steps
            {
                withMaven(maven: 'maven-jenkins')
                {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage')
        {
            steps
            {
                withMaven(maven: 'maven-jenkins')
                {
                    sh 'mvn test'
                }
            }
        }

        stage ('Deployment Stage')
        {
            steps
            {
                withMaven(maven: 'maven-jenkins')
                {
                    sh 'mvn deploy'
                }
            }
        }
    }
}