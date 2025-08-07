**xfceGIT.sh**

script file to install and maintain manual Xfce git (gitlab.xfce.org) installation.

Note: components to be installed listed starting line 16
  -  XFCE_CORE = core Xfce components (from xfce group)
  -  XFCE_PLUGINS = xfce4-panel plugins (from panel-plugins group)
  -  THUNAR_PLUGINS = thunar plugins (from thunar-plugins group)
  -  XFCE_APPS = Xfce applications (from apps group)
Note: if adding any components to this group additional scripting may be required to process correctly.  

First run:
  - xfceGIT.sh init       >> initializes the build system and environment
  - xfceGIT.sh updateall  >> installs (pulls, builds, installs) all Xfce components

Successive runs:
  - xfceGIT.sh update     >> updates (pulls, builds, installs) only the components with new code pushes
  - xfceGIT.sh updateall  >> updates (pulls, builds, installs) all components
  - xfceGIT.sh info       >> show version info for all installed components
  - xfceGIT.sh log [LINES] [COMPONENT]
      - displays commit logs
      - LINES = the number of recent commits to display (default = 10)
      - COMPONENT = the Xfce component to focus on (default = all)
