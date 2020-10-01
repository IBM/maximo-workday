## Setting up your Maximo environment
  - Ensure your 'webappurl' system properties are configured with your application's hostname/ip address
  - Ensure the APIs (object structures) being used for integration are granted authorization for the Maximo user (such as  mxintadm) you will configure in App Connect.  These object structures include:
     - MXAPIDOMAIN (Skilllevel)  
     - MXAPICRAFT
     - MXAPIPERUSER
     - MXAPILABOR
