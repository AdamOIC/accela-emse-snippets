# Accela EMSE Snippets README

A [Visual Studio Code](https://code.visualstudio.com/) snippet extension to provide a library of intellisense support on the 9.2 EMSE Accela API, along with some other helpful code that can be run in Script Tester.

Primarily designed for creating and editing Master Scripts 3.0 events, batches, pageflows, expressions, or other scripts written with the standard Rhino JS framework.
 
<br>
 
#
## Getting Started
<br>
The Accela EMSE Library extension supports code writing for Master Scripts 3.0. To begin, create a new Javascript file or open an existing .js file.

![Change Language](./images/change_language.gif)


From there, trigger intellisense to see a list of commands, or start typing a snippet prefix.  These Snippets are typically accessed with their class names, for the script root it's `aa` or using the item's name wrapped in periods like `.cap.`

<br>

The intellisense library is loaded with the script root's methods and classes, access it by typing `aa`. This is the starting point for accessing the other classes and methods documented in EMSE: 
![aa root](./images/toggle_aa_root.gif)

<br>

### Additional Details

Most items have additional info loaded in. It is sourced from the EMSE description and return value.  When viewing the intellisense list, open an item's description with the `>` toggle:

![toggle description](./images/toggle_intellisense_description.gif)

<br>

### Tab Stops

Each parameter has a tab stop. Stay on the home row, tab through them without having to slow down:

![Tab Stops](./images/ex_tab_stops.gif)


<br>

### Drilling Down

Need to chain into other classes but are a little unsure where to go? No problem!  Start with your root object and select the item you want, like `aa.cap`. Then trigger intellisense again to get the collection of methods for the class. Overloaded methods are appended with a number, step through with arrow keys to see which parameters they take.

![Drilling Down](./images/ex_drilling_down.gif)

 
<br>

#
## Other Snippet Commands
<br>
There are a couple other useful snippets for supporting development and testing within Script Tester.  Check out

* `_scripttestfunctions` loads some helper functions
    * print(str) - Simply removes the aa root for logging to the debug window
    * parseObj(obj) - Add any object and run the code to get a print out of its contents or available methods

* `_scripttestcapid` enters a few lines of code to generate a capId and cap object from a record AltID, useful as a starting point to explore a particular record.

* `ScriptResult.code_block` Adds in the standard .getSuccess()/.getOutput() code block to convert a ScriptResult variable into its output.
<br>
 
#
## Related VS Code Settings and
<br>

If you are new to VS Code, here are some snippet settings and commands that may impact the experience. These settings are applied globally and are not exclusive to this extension.
* To trigger Intellisense, use `Ctrl+Space` (Windows,linux) or `Cmd+Space` (Apple) Many of the items in this extension will require intellisense to be triggered after your selection to see the next level of choices.

* To change the whether snippets are completed by the `tab` key, change the `editor.tabCompletion` setting to on, off, or onlySnippets.

* The intellisense suggestion order can be rearranged. Change the value in the setting `editor.snippetSuggestions`:
    * top: show above other suggestions
    * bottom: show below other suggestions
    * inline: show snippets mixed in with everything else
    * none: turn them off
* Snippets providing suggestions can be toggled with the setting `editor.suggest.snippetsPreventQuickSuggestions`: true or false

 
<br>

#
## Known Issues
<br>
The 9.2 EMSE API javadoc is parsed to provide the foundation of these snippets.  Due to the size and consistency of the javadoc, the intellisense suggestions may be incomplete or missing.  Basically, some of it requires a human touch to improve. <br><br>

For example, the InspectionScript method returns are often blank and placed in the description of the method. We are actively working on cleaning up the snippet library and are open to feedback and fixes.

Reach out on the Discord channel to let others know about this extension and give feedback for corrections.

 
<br>
 
#
## Release Notes

* ### 1.0.0 (Beta)

  * Initial release of the snippet extension with support for the aa root, cap, inspections, workflow, and util

* ### 1.0.1 (Beta)

  * Miscellaneous formatting updates.
  * Added the env and ScriptResult classes
  * Added a ScriptResult snippet "ScriptResult.code_block" to insert code to convert a ScriptResult return into its output value:
  <br>
  `"ScriptResult.code_block" ->`
  <br>
  > if(ScriptResultVarible.getSuccess()) {
  > <br>
  > &nbsp;&nbsp;&nbsp;&nbsp;ScriptResultVariable = ScriptResultVariable.getOutput();
  > <br>
  > } else {
  > <br>
  > &nbsp;&nbsp;&nbsp;&nbsp;aa.print("ScriptResult Failed");
  > <br>
  > }

* ### 1.0.2
  * Fixed comment in _scripttestcapid
  * Addition of capModel and capId Model
 
* ### 1.0.3
  * ScriptTester code block: Load in INCLUDES_ files with the prefix "_scripttestincludes". Master Scripts are only loaded if you have EMSE_EXECUTE_OPTIONS>USE_MASTER_INCLUDES set to 'Yes'.  The INCLUDES_CUSTOM file will be loaded from Events>Custom Script unless you have a script called 'INCLUDES_CUSTOM' in the agency's Events>Scripts.
  * Compression of snippet file

<br>
 
#
## Future Releases
<br>
Updates to the extension will include additional class root/methods along with general cleanup of the intellisense contents.  Also on the road map are Script Tester code blocks to add INCLUDES_ files and event emulation for in-system testing.

 
<br>
 
**Enjoy!**
