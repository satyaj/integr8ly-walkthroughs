# Custom walkthroughs for an Integreatly cluster


## Running custom walkthroughs

To run a custom walkthrough you need an exiting OpenShift cluster with integreatly installed.

* Navigate to the `webapp` namespace and edit the resource `webapp > tutorial-web-app-operator`.
* Edit the YAML by adding the following section in *Spec > Template > Properties*:

----
WALKTHROUGH_LOCATIONS: https://github.com/integr8ly/tutorial-web-app-walkthroughs#master,https://github.com/satyaj/integr8ly-walkthroughs#master
----

NOTE: If you do not want the default Integreatly walkthoughs to be displayed, then do not include the *https://github.com/integr8ly/tutorial-web-app-walkthroughs#master* location.

* You can add more walkthroughs by using the `,` separator.

* The WALKTHROUGH_LOCATION assumes a *walkthrough* folder exists with the walkthroughs. If your walkthroughs are in a different folder, use the parameter *walkthroughsFolder=/docs/labs/citizen-integrator-track*

----
WALKTHROUGH_LOCATIONS: https://github.com/RedHatWorkshops/dayinthelife-integration.git?walkthroughsFolder=/docs/labs/citizen-integrator-track&walkthroughsFolder=/docs/labs/developer-track&walkthroughsFolder=/docs/labs/operations-track
----

* Save the YAML to trigger a redeployment of the *tutorial-web-app*.

## Creating custom walkthroughs

Refer to the detailed guide below on creating custom walkthroughs:
https://mojo.redhat.com/docs/DOC-1190932

This repository can be a common repository for all the custom walkthroughs of the GPTE middleware team. Any custom walkthroughs created should be imported here to the *walkthroughs* folder.
