# Change Log

## [1.0.9]
- Update to the _scripttestincludes snippet

## [1.0.8]
- Added in additional classes: appSpecificInfo, calendar, document, examination, guidesheet, publicUser, set

## [1.0.6] - 2022-03-01
- Added expiration, invoice, parcel, owner

## [1.0.5] - 2022-02-17
- Fixed variable error in _scripttestcapid
- Enhanced _scripttestincludes support and env variables

## [1.0.4] - 2022-02-09
- Updates to readMe
- Fixed prefix on capId root object
- Added 'address' script class

## [1.0.3] - 2022-02-07
- ScriptTester: Load in INCLUDES_ files
- Compression of snippet file

## [1.0.2] - 2022-01-31
- Fixed comment in _scripttestcapid
- Addition of capModel and capId Model

## [1.0.1] - 2022-01-26
- Housekeeping on log and readme
- Lowered compatibility versioning to VSC 1.32
- Cleanup of formatting
- File compression to improve performance
- Updates to some method objects to correct parsing problems
- Added 'env' class
- Added 'ScriptResult' class. Not chained from the aa root, instead accessible with the prefix "ScriptResult."
- Added "ScriptResult.code_block" to insert the standard validation of a script result return

## [1.0.0] - 2022-01-25

- Initial release
- Exposes 'aa', 'cap', 'inspection', 'workflow', and 'util'
- ScriptTest starter code snippets