

It is best practice to configure default IVR profile in GVP environment, in case, if your regular DN-Profile mapping is not happening. This post will explain step by step instructions to configure default profile

  * select your&#8217; ‘tenant’ object – in most cases, it is ‘Resources’ – under Administrator –> Provisioning –> Tenants
  * Create section gvp.general in options tab and update following values
  * name : _default-application_, value : _DefaultApp_ (Default IVR Profile application name)
  * name : _service-type_, value : _voicexml_

  * Click ‘_Save & Close_’ to save settings