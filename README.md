# What is the Cake Contrib Organisation?

The Cake Contrib Organisation was created after a discussion on Gitter which questioned what happens when a community contributed Cake Addin becomes unmaintained by the original author.

The upshot of that conversation was we (the Cake Team):

* wanted to provide a central location that Addin Authors could decide to move their Addin's to, when it was clear that they were no longer able to maintain an Addin, which would mean that other interested maintainers could easily be added to the Team to help with the maintenance
* wanted to provide a central location that Addin Authors could choose to move their Addin's to, even when they were still interested in maintaining the project, and just wanted to take advantage of the benefits of moving into this Organisation
* wanted to provide the infrastructure to allow Continuous Integration Builds of the Addin's, without having to worry about the setup overhead
* wanted to provide an option to notify the Cake community about new releases of the Addin via official Cake Contrib communication channels such as Gitter and Slack

# How do I, as an Addin Author, transfer a repository to the Organisation?

Moving a repository into this organisation is a very simple process, but it does involve a couple hoops.  It is not possible to move a repository directly into the Organisation, unless you are an owner of the Organisation.

As a result, the easiest way to move a repository into this Organisation is to first transfer the repository to a member of the Cake Team, and from there, they will move it into the Cake Contrib Organisation.

Once that request has been made, the following process will be followed:

* If the original maintainer of the repo hasn't been invited to the `cake-contrib` organisation, an invite will be sent out
* If a team has not been created in the Organisation for the original maintainer of the repo, one will be created using the convention `Team <First Name>`
* Repository will be transferred from Team Member account to `cake-contrib` Organisation, and added to the `Team` and `Team <First Name>` teams
* Once the transfer is complete, go to the settings of the repository and click on `Collaborators & teams` tab
* Give Admin permission to all Teams
* Remove all collaborators, as they should now be included as teams
* Check with the original owner if they want to use the standard labels for issues in this repository.  If they do, run the label creation tool
* Go to AppVeyor
* If this was a new user invited to the organisation, create a matching role for that user and map the GitHub Team to that role
* Add a new AppVeyor Project for the new repository
* Go to the Settings section, and click on Notifications
* Add a slack and web hook notification, using settings from an existing project as a basis
* Run the permission sync tool
  * If this was a new user added to the Organisation, you will need to run the tool for all projects
  * If this was an existing user adding a new project, you will only need to run the tool for one project
* Check the permissions and environment variables section to make sure that they are filled out
* Create environment variable for `WYAM_DEPLOY_REMOTE` and add value (similar to existing projects i.e. `https://github.com/cake-contrib/Cake.Hg`)
* Go to coveralls.io and add new project using `cake-contrib` account
* Create environment varialbe for `COVERALLS_REPO_TOKEN` and copy in value from above step
* If a yml file has been added to the Website Repository, make sure to update the link to the repository
* Inform user of process being complete

# What permissions will I, as an Addin Author have, once I move it to this Organisation?

The bottom line is, we want you, as the original Addin creator, and potential continued maintainer, to have the exact same permissions that you had when you created the repository in the first place.

To this end, the following things will happen:

* A new GitHub Team will be created for yourself
* Any repositories that you are going to be maintaining will be added to this Team with full admin permissions
* An AppVeyor Project will be created for the new repositories in the Organisation
* An AppVeyor Role will be created which will map to the new GitHub Team
* This AppVeyor Role will be provided with the correct permissions to access each AppVeyor Project
* The necessary settings will be added to the AppVeyor project to allow notifications to be sent via the official Cake Contrib communication channels

# Tracking Addin's, Modules and Recipes

Due to the growing number of Addin's, Modules and Recipes that are available, we are tracking the current status of each of these.

Ideally, all addin's, modules and recipes will appear on the [Cake Website](http://cakebuild.net/), however, this requires PR's from the maintainers, so in the meantime, you can find this information [here](https://github.com/cake-contrib/Home/blob/master/Status.md).

This tracks things like:

* the fact that the addin/module/recipe actually exists
* a link to the NuGet package
* information about the maintainer
* whether the maintainer has been contacted about providing additional information
* whether the cake-contrib user has been added as a co-maintainer to the NuGet packages
* whether the addin has been added to the Cake Build website
* whether the addin repository has been moved to the Cake Contrib Organisation

# License

[![License](http://img.shields.io/:license-mit-blue.svg)](https://github.com/cake-contrib/Cake.Recipe/blob/develop/LICENSE)

# Chat Room

Come join in the conversation about anything related to the Cake Contrib Organisation in our Gitter Chat Room

[![Join the chat at https://gitter.im/cake-contrib/Lobby](https://badges.gitter.im/cake-contrib/Lobby.svg)](https://gitter.im/cake-contrib/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
