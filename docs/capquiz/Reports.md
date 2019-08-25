# Reports

CAPQuiz supports a **Report** sub-plugin type.

CAPQuiz report sub-plugins is mainly intended to display custom reports on the quiz data. However, it may also be used to plugin other functionality into the CAPQuiz module.

## Overview
Theses report sub-plugins have the prefix `capquizreport_`, and live inside `mod/capquiz/report`.

A capquiz report plugin just needs to implement one class.

```php
class capquizreport_name_report extends report {
    public function display($capquiz, $cm, $course, $download) {
        // Generate and display the report, or
        // some other functionality.
    }
}
```
The base class is defined in `mod/capquiz/report/report.php` and you just need to implement the display method. This gets called from `mod/capquiz/classes/output/report_renderer.php` after some basic set-up has been done.

## What files make up a CAPQuiz report
```
mod/capquiz/report/name/
    report.php                     - Contains the implementation of the capquiz_name_report class.
    version.php                    - Normal Moodle plugin version.php file.
    lang/en/capquizreport_name.php - Language strings for your plugin.
    db/*                           - Lets you define db tables, capabilities, etc.
```
* It is possible to make a working plugin with only the first three of these.
* The only lang string you need to define is `pluginname`.

## Template
A basic template for capquiz report plugin is available at [Github](https://github.com/KQMATH/moodle-capquizreport_template)

## Naming conventions
Following naming conventions should be kept in mind while writing a CAPQuiz report plugin:

* Folder name should be same as pluginname, in lowercase.
* Name of the extended class should be in format `\capquizreport_name\report`
* `\ capquizreport_name\report` must implement the function
```php
function display($capquiz, $cm, $course, $download) {}
```

## When a user view the report
The will go to a URL like `https://.../mod/capquiz/view_report.php?id=cmid&mode=name`. There may also be additional parameters in the URL if your report contains several internal pages with links between them. The attempts reports is a good example of this.

This leads to a call to the `capquizreport_name_report::display($capquiz, $cm, $course, $download)` method. You can put whatever code you like in there.

## The attempts report classes
There are some useful helper classes in `mod/capquiz/report/attemptsreport.php`. This is basically some reusable functionality that is used by the attempts report. If you want to make a similar report (with one row for each capquiz attempt) you should probably build on these classes.

There are also useful helper functions in mod/capquiz/report/reportlib.php.