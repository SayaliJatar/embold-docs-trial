Embold Jenkins Plugin allows users to scan code after Jenkins build is triggered. Users can configure Embold modules from this plugin. 
The plugin requires sign-in with the Embold Server deployed within the organization.

### Prerequisites 
Jenkins version 1.6.1.2 to 2.164.2
Remote Analysis should work from Jenkins machine (where build is happening) to Embold machine. (Refer Remote Analysis article).
Install standalone corona on build machine (master/node) (e.g. /opt/gamma. It will be your GAMMA_ROOT folder) (Refer steps for Ubuntu, Windows, Redhat).
For running gcov, Gcovr should be installed on the build machine.
JDK (Java Development Kit)
JAVA_HOME environment variable need to set for build machine (master or slave) which should point to /bin
