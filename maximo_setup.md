## Setting up your Maximo environment
  - Ensure your 'webappurl' system properties are configured with your application's hostname/ip address (https://www.ibm.com/support/knowledgecenter/en/SSLKT6_7.6.1.2/com.ibm.mif.doc/reference/r_mif_sys_props.html)
  - Ensure the APIs (object structures) being used for integration are granted authorization for the Maximo user (such as  mxintadm) you will configure in App Connect.  This is the Maximo user that the Maximo Connector in App Connect will use to access the Maximo REST API. These object structures include:
     - MXAPIDOMAIN (Skilllevel)  
     - MXAPICRAFT
     - MXAPIPERUSER
     - MXAPILABOR
[Configure Object Structures](https://www.ibm.com/support/knowledgecenter/en/SSLKT6_7.6.1.2/com.ibm.mbs.doc/asset/t_dt_object_structure_sec.html)
- Increase the lengths of
    - SKILLEVEL Domain to 30
    - CRAFT attribute on the CRAFT object to 30
[Configure Database](https://www.ibm.com/support/knowledgecenter/en/SSLKT6_7.6.1.2/com.ibm.mbs.doc/configur/c_db_config.html)
