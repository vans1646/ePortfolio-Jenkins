# ePortfolio-Jenkins
Here you can find my used files, sources and the [presentation](./Jenkins_ePortfolio.pdf) of my ePortfolio :)

## Quick start guide
To get started with Jenkins it's best to use the official [Jenkins website](https://www.jenkins.io/doc/pipeline/tour/getting-started/).

Here you can find a guide that will take you step by step to achieving a working Jenkins Dashboard

### Prepare your GitHub respository
If you want to run the Pipeline with every new commit on your repository, you need to activate webhooks.
- go to your repository settings > webhooks > add a new webhook
- here you link the URL of your Jenkins. Therefore it has to be available at all times (running on a server)

### Jenkins Plugins
To get the full experience of Jenkins it's mandatory to install plugins

During installation you get asked to install all recommended ones - do that

Further more I recommend Git, Docker, NodeJS, Pipeline and Blue Ocean

You can achieve that on your dashboard via Manage Jenkins > Plugins

### Adding a Jenkins Pipeline
To add a new Pipeline click on your dashboard New Item. For simplicity choose simply a Pipeline and give it a name.

Hit OK and you can configure your Pipeline! 

If you want to trigger via Webhooks and configured your GitHub repository accordingly you have to tick 'GitHub hook trigger for GITScm polling' under Build Triggers.

If you want to define your Pipeline with a Jenkinsfile from your repository you need to change the Pipeline definition to 'Pipeline script vom SCM'
- for reference you can have a look at my [Jenkinsfile](./Jenkinsfile)

Choose Git and link your repository URL. Jenkins will then try to find the Jenkinsfile in your repository when building the Pipeline.

*Congratulations! You created your first Pipeline!*
