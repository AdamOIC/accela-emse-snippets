
* ### 1.2.0
  * New code snippet for running WTUA event code - _scripttestWTUA.
* ### 1.1.5
  * Fix aa.sendMail to include the third parameter for email cc
  * Rename 'CapModel' in _scripttestcapid to 'cap' to allow that code snippet and '_scripttestincludes' to work better together in a variety of agencies.
* ### 1.1.1-1.1.4
  * Added calls for ScriptResult.Code_Block
  * Renamed params in some parsed method text, re-formatting throughout library of parsed text
* ### 1.1.0
  * Added additional object
* ### 1.0.9
  * _scripttestincludes declares the 'ADMIN' userId env variable to support different agency's calls
  * _scripttestincludes adds an eval for logDebug to support aa.print in the script test window when the function is called in _INCLUDES files
* ### 1.0.6 -1.0.8
  * Added additional objects
* ### 1.0.5
  * Fixed variable error in _scripttestcapid
  * Enhanced _scripttestincludes 
* ### 1.0.4
  * Added the AddressScript model accessible with .address.
* ### 1.0.3
  * ScriptTester code block: Load in INCLUDES_ files with the prefix "_scripttestincludes". Master Scripts are only loaded if you have EMSE_EXECUTE_OPTIONS>USE_MASTER_INCLUDES set to 'Yes'.  The INCLUDES_CUSTOM file will be loaded from Events>Custom Script unless you have a script called 'INCLUDES_CUSTOM' in the agency's Events>Scripts.
  * Compression of snippet file
* ### 1.0.2
  * Fixed comment in _scripttestcapid
  * Addition of capModel and capId Model 
* ### 1.0.1
  * Miscellaneous formatting updates.
  * Added the env and ScriptResult classes
  * Added a ScriptResult snippet "ScriptResult.code_block" to insert code to convert a ScriptResult return into its output value.
* ### 1.0.0
  * Initial release of the snippet extension with support for the aa root, cap, inspections, workflow, and util




 











