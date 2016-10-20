<p align="center">
    <a href="module-3.md">← Module 3</a> | <strong>Module 4</strong> | <a href="module-5.md">Module 5 →</a>
</p>

# Module 4: Sitecore API

## 4.1 Basic API Concepts and Retrieving items

Assembly `Sitecore.Kernel` namespaces:

* `Sitecore.Data`: CRUD operations & item manipulation;
* `Sitecore.Context`: Contains members regarding the current HTTP request;
* `Sitecore.Links`: Infrastructure for handling hyperlinks.

Some useful utilities:

* Sitecore.DateUtil
* Sitecore.IO.FileUtil
* Sitecore.StringUtil
* Sitecore.UIUtil
* Sitecore.MainUtil

Getting the site's *Home* item can be useful at times *(unknown at this point)*. This is specified in the `<site>` node
in `web.config`.

~~~
var startPath = Sitecore.Context.Site.StartPath;
var homeItem = Sitecore.Context.Database.GetItem(startPath);
~~~

### Notes

* Everything in Sitecore.Context is about the *current* HTTP request.
* Makes sense to store IDs required in code in a central place (repository), e.g. a static class containing contstants.
* Get decendants, e.g. using the API's Axes.GetDescendants() methods, might be a performance issue because it queries
  recursively! Be careful when using it. Better use GetChildItems, but this method doesn't search recursively.
* Always compare items by using the IDs!
* A custom LinkManager implementation can be created, but beware: you might also need to create a custom ItemResolver
  implementation.

## 4.3 Creating, Deleting and Modifying Items

Retrieving item fields can be done in two ways:

* `Item["field-name"]` returns the raw field value as a string. Returns `string.Empty` if the field is `null` (and
  likely also when the field does not exist).
* `Item.Fields["field-name"]` returns the field as a `Field` object. Use the `Field.Value` property to get the raw value
  as a string.

Some fields, like text fields, can be updated by setting the `Field.Value` property. Note that this makes the field
*uneditable* in Experience Editor.

*`Sitecore.Context.User` contains either the currently signed in user, or **anonymous**.*

## 4.4 Working with Complex Fields

* Always use one of the `FieldRenderer.Render` methods, instead of manually creating HTML elements. If not, the result
  won't be editable in the Experience Editor.
* Fields are **not** settable. To edit fields, you must retrieve a handle to it, then edit its members one by one. This
  could of course be mitigated by using the *repository pattern*.

<p align="center">
    <a href="module-3.md">← Module 3</a> | <strong>Module 4</strong> | <a href="module-5.md">Module 5 →</a>
</p>
