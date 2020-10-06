## Setting up your Maximo environment
  - Ensure your 'webappurl' system properties are configured with your application's hostname/ip address
  - Ensure the APIs (object structures) being used for integration are granted authorization for the Maximo user (such as  mxintadm) you will configure in App Connect.  This is the Maximo user that the Maximo Connector in App Connect will use to access the Maximo REST API. These object structures include:
     - MXAPIDOMAIN (Skilllevel)  
     - MXAPICRAFT
     - MXAPIPERUSER
     - MXAPILABOR
- Increase the lengths of
    - SKILLEVEL Domain to 30
    - CRAFT attribute on the CRAFT object to 30
