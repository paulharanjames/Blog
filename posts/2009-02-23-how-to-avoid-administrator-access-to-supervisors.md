
In Genesys, if you are configuring non-agent, they are automatically added to the ‘Administrators’ access group. Many times, we have to configure Supervisors and would like to provide access to their agent group only. Prior to 7.6 version, it is achieved by creating new access group and removing the person from Administrators group.

From 7.6, you can disable the default access to the users. For every user, you need to manually assign him to the access group. 

To disable the default access, create section **‘Security’** in Configuration Server ‘**Options’** tab and configure the option to **‘no-default-access’** to **‘0’.** Simple and found it useful to avoid any human errors