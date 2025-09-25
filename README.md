# C/C++ Definition Autocompletion

**Autocomplete function definitions from declared functions on the fly.**

<br>

## Features

To trigger the autocompletion, type a `.` on a new blank line in your `.c/.cpp` file.

### **Currently we are supporting:**
- member class functions
- normal functions
- template functions
- nested member class functions
- and many more...

### **Additional Features:**
- only functions which are not defined already are suggested
- special handling of constructors to quickly have a member initializer list on hands
- inlined / deleted / defaulted / pure virtual functions are not suggested
- specify interval to automatically update symbols

 <br>

## Examples:

![Member function completion demo](images/member_function_completion_demo.gif)


![Constructor demo](images/constructor_demo.gif)

<br>

## Requirements

- C/C++ Extension

<br>

## Extension Settings

This extension contributes the following settings:

* `definition-autocompletion.trigger_character`: The character that triggers the completion suggestion on a new blank line. (default=`.`)
* `definition-autocompletion.update_index_on_save`: Wether to update the symbol index table when saving the current text document. (default=`true`)
* `definition-autocompletion.update_index_on_change`: Wether to update the symbol index table when changing the active text editor. (default=`false`)
* `definition-autocompletion.update_index_interval` : The interval in seconds in which the symbol index table will update. Specify `0` to deactivate the interval. (default=`20`)
* `definition-autocompletion.source_file_extension_patterns` : The source file extension patterns as an array. (default=`["c", "cpp"]`)
* `definition-autocompletion.header_file_extension_patterns` : The header file extension patterns as an array. (default=`["h", "hpp"]`)

<br>

## Known Issues

- nested return Types are not extended by the outer layer Type
- currently only works with workspaces

<br>

## Future Plans

- fix issues

<br>

## Release Notes


### 1.2.0

  - add namespace support
  - add nested template declaration support
  - fix configuration options to specify the header/source file patterns

### 1.1.9

  - added configuration options to specify the header/source file patterns

### 1.1.8

  - fixed issues with folder detection outside workspaces

### 1.1.7

  - some improvements in signature detection

### 1.1.6

  - fixed issues with workspace folder detection

### 1.1.5

  - automatically index a not yet indexed file when switching to it, regardless of the `definition-autocompletion.update_index_on_change` option.
  - added interval to update the symbol index periodically

### 1.1.4

  - fixed issues with member function definitions

### 1.1.3

  - fixed issues with definition detection in source files

### 1.1.2

  - detect more function attributes and specifiers correctly

### 1.1.1

  - supporting constructors member initialization list

### 1.1.0

 - supporting templates
 - supporting inline functions
 - supporting nested class members

### 1.0.0

 - Initial release

