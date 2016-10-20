<p align="center">
    <a href="module-5.md">← Module 5</a> | <strong>Module 6</strong> | <a href="module-7.md">Module 7 →</a>
</p>

# Module 6: Real World Solutions

We'll use the `TrainCore` Sitecore instance from now on, instead of the `BasicSitecore` Sitecore instance.

## 6.1 Familiar Concepts

* It's possible to see the Template inheritance tree, in Content Editor as well as in the Sitecore Rocks Visual Studio
  extension.

## 6.2 Dealing with Larger Sites

### Multi-Language Support

* Sitecore language fallback is implemented out-of-the box (needs to be enabled) in Sitecore XP 8.1.

Navigate your browser to `<wwwroot>/sitecore/admin/showconfig.aspx` to display the compiled `web.config`. This
functionality is also available in the Sitecore Rocks Visual Studio extension.

**Licensing model: One separate license is needed *per IIS application pool*.**

## 6.3 Versioned Layouts

Culture names used for languages need to be valid .NET culture names. Add supported languages to the `/System/Languages`
item.

A *shared* field value means that it's shared between all languages of a numbered version. Useful for numbers, for
instance. *Unversioned* fields have a single value, per language.

Sitecore 8 introduces *Versioned Layouts*. As explained earlier, presentation is stored in the `__Renderings` system
field (a shared field). The `__Final Renderings` field is new, which is a versioned field and, like the `__Renderings`
field, contains a layout delta.

## 6.4 Sitecore Query

It uses XPath to manipulate the raw XML values.

*It is recommended **not** to use this feature. It possibly leads to performance issues.*

We recommend *Sitecore Fast Query* - it translates into T-SQL statements which are executed directly on the SQL Server.

<p align="center">
    <a href="module-5.md">← Module 5</a> | <strong>Module 6</strong> | <a href="module-7.md">Module 7 →</a>
</p>
