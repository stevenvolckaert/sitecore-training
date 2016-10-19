<p align="center">
    <a href="module-3.md">← Module 3</a> | <strong><a href="#">Module 4</a></strong> | <a href="module-5.md">Module 5 →</a>
</p>

# Module 4: Sitecore API

*TODO Ask the trainer what's the difference between the **Feed** and **RSS** device, when layouting.*

* Everything in Sitecore.Context is about the *current* HTTP request.
* Makes sense to store IDs required in code in a central place (repository), e.g. a static class containing contstants.
* Get decendants, e.g. using the API's Axes.GetDescendants() methods, might be a performance issue because it queries
  recursively! Be careful when using it. Better use GetChildItems, but this method doesn't search recursively.
* Always compare items by using the IDs!
* A custom LinkManager implementation can be created, but beware: you might also need to create a custom ItemResolver
  implementation.

## 4.4 Working with Complex Fields

* Always use one of the `FieldRenderer.Render` methods, instead of manually creating HTML elements. If not, the result
  won't be editable in the Experience Editor.
* Fields are **not** settable. To edit fields, you must retrieve a handle to it, then edit its members one by one. This
  could of course be mitigated by using the *repository pattern*.

<p align="center">
    <a href="module-3.md">← Module 3</a> | <strong><a href="#">Module 4</a></strong> | <a href="module-5.md">Module 5 →</a>
</p>
