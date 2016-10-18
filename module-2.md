# Module 2: Defining Data

Templates can inherit from multiple base templates.
* Field names **should** be unique, also when inheriting!
* Field sections with the same name will merge.
* Avoid circular data template inheritance

## 2.3 Standard Values

* [Sitecore Powershell Extensions][1] are useful to refactor templates to so that they all have `__Standard Values`.
  See the [Sitecore Marketplace][2].

## 2.4 Insert Options

*Insert Options* are used to limit the insert options that Content Editors will see in the Content Editor.

* It's recommended to configure *Insert Options* in the `__Standard Values` of a template.
* right-click `__Standard Values` → Tasks → add insert options.

## 2.5 Summary and Optional Lab

[1]: https://marketplace.sitecore.net/Modules/S/Sitecore_PowerShell_console.aspx
[2]: https://marketplace.sitecore.net
