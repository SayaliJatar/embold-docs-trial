Embold Jenkins Plugin allows users to scan code after Jenkins build is triggered. Users can configure Embold modules from this plugin. 
The plugin requires sign-in with the Embold Server deployed within the organization.

### Prerequisites 
* Jenkins version 1.6.1.2 to 2.164.2
* Remote Analysis should work from Jenkins machine (where build is happening) to Embold machine. Refer [Remote Analysis article](https://docs.embold.io/installation-and-backup-guide/#remote-analysis).
* Install standalone corona on build machine (master/node) (e.g. /opt/gamma. It will be your GAMMA_ROOT folder) (Refer steps for [Ubuntu](https://docs.embold.io/installation-and-backup-guide/#install-standalone-corona-on-ubuntu), [Windows](https://docs.embold.io/installation-and-backup-guide/#install-standalone-corona-on-windows), [Redhat](https://docs.embold.io/installation-and-backup-guide/#install-standalone-corona-on-rhel-or-centos)).
* For running gcov, Gcovr should be installed on the build machine.
* JDK (Java Development Kit)
* JAVA_HOME environment variable need to set for build machine (master or slave) which should point to /bin

### Installation Steps 
1. Download file from your [Embold Account’s section](https://v1.embold.io/account) > Releases tab > Plugins > CI_CD > jenkins. There will be file with a name similar to the following: embold_jenkins_1.8.3.0.hpi.
2. Click on “Manage Jenkins” on Jenkins’s home page.
3. Jump to the Advanced tab.
4. Go to the Upload Plugin section and upload “embold_jenkins_1.8.3.0.hpi”.Click the “Upload” button.
5. After Embold Jenkins Plugin is updated, Jenkins needs to be restarted.
<img width="1269" alt="Jenkins_installation" src="https://user-images.githubusercontent.com/65024631/116405544-68da0980-a84d-11eb-8681-4f72b3a3a5a1.png">

### Integration Modes
1. As Post Steps: Hooking into the build process so that Jenkins Job can be marked unstable if Embold’s quality gate check fails.
2. As Post-build Actions:
   1. Hooking into Jenkins job workflow and gets triggered after the build is completed.
   2. In this mode, Embold Jenkins plugin will run irrespective, if the build has failed for any reason.
<img width="918" alt="Jenkins_integration" src="https://user-images.githubusercontent.com/65024631/116540569-f4b06c00-a907-11eb-935d-9ef71c1f5a2d.png">

