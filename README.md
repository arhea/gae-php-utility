## Google App Engine PHP Helpers
This is a command line tool that abstracts away long winded Google App Engine command line tasks. It only supports Mac at the moment. I only develop on a Mac so I am open to contributions for other platforms.

### Install Instructions
1. Clone this repository to your computer.
2. Add this directory to your path.
3. Install MacPorts if you dont already have it.
4. Run `gae install`

### Functions

#### Start
`gae start <directory>` Starts the Google App Engine development server in the current directory or the passed directory.
This function assumes you have followed the install instructions.

#### Deploy
`gae deploy <directory>` Deploys your application based on the `app.yaml` to your App Engine Application. It uses the OAuth method for authentication and may redirect you to the browser to allow the application. The directory is again optional, only use that if the directory you want to deploy is not the current one.

#### Rollback
`gae rollback <directory>` Rollback and application deploy or stop one that is hanging. Again, directory is optional.

#### Install
`gae install` This will install the PHP SDK and the proper App Engine preferred PHP. You must have MacPorts installed for this function to work properly.

#### Update Cron Jobs
`gae update_crons <directory>` Updates just the cron jobs and not the whole application

#### Update Task Queues
`gae update_queues <directory>` Updates just the task queues and not the whole application

#### Update DOS
`gae update_dos <directory>` Updates just the dos and not the whole application

#### Download Application
`gae download -A <app_id> -V <version_number> <output_directory>` Downloads your application from Google App Engine
* App ID - the application identifier. Usually <here>.appspot.com
* Version Number - the version number you wish to download
* Output Directory - where you want all the files to go

### Author
Alex Rhea
alex.rhea@gmail.com
