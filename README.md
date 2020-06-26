# WebHare Code Generator #

This module enables you to generate code for WebHare. 

Using the application's interface, you can add fields/members of many types (textedit, array, image, etc) which results in (yes, somewhat opionated) XML 

One of the big pros of using this (apart from the obvious time saver) is that the generated code doesn't crash, which is especially annoying when creating widgets and if you need to start all over again adding your cool widget because of a crash due to a little typo.

Apart from this, it can also be used as a reference to the 'newest' syntax in HareScript/XML. For example, the generated code uses the new siteprofile syntax and the `<filetype>` `kind=virtualfile` attribute that have been added to [WebHare 4.28](https://gitlab.com/webhare/platform/-/blob/master/whtree/modules/system/doc/topics/changelogs/4.28.md#things-that-are-nice-to-know).

This of course depends on the maintenance of this repository. Disclaimer: I'm not promising anything!

## Installation

To install this module:

```
git clone https://github.com/WouterHendriks/wh-codegenerator.git "$(wh getdatadir)installedmodules/codegenerator"
```

## Starting up

To start the main application, assuming a default install, go to:

https://my.webhare.dev/?app=codegenerator

(if you haven't set this yet, you probably need to set it to something like http://localhost:8000/)

## Generating code

The application can generate the following types of code:

1) Overview folder with index file and custom details page
2) Custom filetype
3) Widget
4) Form (quite basic atm)

It generates a folder and the following files:

- `<name>.es` (JavaScript)
- `<name>.scss` (SCSS)
- `<name>.siteprl.xml` (siteprofile)
- `<name>.witty` Witty (HTML template) file
  
In the case of forms, it also adds a `<name>.formdef.xml`.

The code generation assumes that the following folders are present, in which a new folder is created:

1) Overview folder: /modulename/webdesigns/modulename/pages/
2) Custom filetype: /modulename/webdesigns/modulename/pages/
3) Widget: /modulename/webdesigns/modulename/widgets/
4) Form: /modulename/webdesigns/modulename/

The code generator will not create the folder if it's not present to prevent accidental overwrites. When generating code the application will also tell you what it will do.

## No 'edit mode'

At the moment the code generator just adds code. It's not capable of editing existing code. Not yet, anyway.

## This repo

Since WebHare is constantly evolving, this repository will probably be changing all the time. So be sure to pull the newest version from time to time!

## Enjoy it!

![](http://www.quickmeme.com/img/5b/5b3761867c14de76ab959f4b9ece9a3b51654222b93c92e7e02c4e80fad9da21.jpg "")

