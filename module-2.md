<p align="center">
    <a href="module-1.md">← Module 1</a> | <strong><a href="#">Module 2</a></strong> | <a href="module-3.md">Module 3 →</a>
</p>

# Module 2: Defining Data

Templates can inherit from multiple base templates.
* Field names **should** be unique, also when inheriting!
* Field sections with the same name will merge.
* Avoid circular data template inheritance

## 2.3 Standard Values

* `__Standard Values` contains all fields of the data template, *including* the fields of inherited data templates.
* `__Standard Values` also contain defaults for layouting! However, these need to be accessed
* Standard Values allows to select defaults for field values, insert options, presentation, and workflow.
* [Sitecore Powershell Extensions][1] are useful to refactor templates to so that they all have `__Standard Values`. See
  the [Sitecore Marketplace][2].

### Tokens

Tokens are *dynamic* default field values: They are substituted *the moment an item is created*. You can create your own
tokens programmatically.

* `$id`
* `$name`
* `$parentid`
* `$parentname`
* `$date`
* `$time`
* `$now` (equivalent to `$date` + `$time`)

## 2.4 Insert Options

*Insert Options* are a list of date templates. They are used to limit the template options authors have when using the
Sitecore UIs.

* It's recommended to configure *Insert Options* in the `__Standard Values` of a template.
* right-click `__Standard Values` → Tasks → add insert options.

## 2.5 Summary and Optional Lab

## Key Vocabulary

***TODO Add to Confluence Glossary Article***

#### Data Template
Defines an item’s type.Contains field sections and fields. Should always have a unique icon. Used to create items.
#### Field
Holds content. Can be different types: Single-Line Text, Rich Text, Image, General Linkand more. Type determines the
interface that the author sees for editing that field.
#### Data Template Inheritance
Data templates can inherit fields and field sections from other data templates. Reduces duplication.
#### Standard Values
__Standard Values is a child item of a data template and is the mechanism for defaults when items are created.
#### Insert Options
List of item types that can be inserted by authors as a child of a particular item.

[1]: https://marketplace.sitecore.net/Modules/S/Sitecore_PowerShell_console.aspx
[2]: https://marketplace.sitecore.net

<p align="center">
    <a href="module-1.md">← Module 1</a> | <strong><a href="#">Module 2</a></strong> | <a href="module-3.md">Module 3 →</a>
</p>
