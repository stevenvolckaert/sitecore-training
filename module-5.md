<p align="center">
    <a href="module-4.md">← Module 4</a> | <strong>Module 5</strong> | <a href="module-6.md">Module 6 →</a>
</p>

# Module 5: Advanced Presentation Concepts

## 5.1 Reusable Content

* Use *Data Source* to create and set data that can be rendered differently by different components. It is reusable
  content.
* *Content Items* don't have presentation (you can set it, though.)
* A component that takes data from an item that is not the context item.
* *Data Source* is comparable with setting the DataSource of ASP.NET Web Forms controls, and WPF controls.

To get content:

~~~
// Gets the data source item of the current request.
// This snippet only applies to ASP.NET Web Forms.
public Item GetDataSourceItem()
{
    var dataSourceIdString = Attributes["sc_datasource"];
    var dataSourceItem = Sitecore.Context.Database.GetItem(dataSourceIdString);
    return dataSourceItem;
}
~~~

Beware: Force controls to use a different data source than the context item by setting the control's `Item` property in
code-behind. Or set the control's `DataSource` property to the formatted ID string. You can also set it declaratively in
the `.ascx` file.

## 5.2 Layout Deltas

* A *Layout Delta* is basically a transform, set on an individual content item, to alter the presentation.
* In the Content Editory, you can see which items have their presentation overridden. Right-click the gutter (a.k.a. the
  Quick Action Bar), and enable **Presentation Overridden**. A specific icon will appear in the gutter next to items
  that have their presentation overridden.
* Layout Deltas are persisted as XML in the `__Renderings` system field.

<p align="center">
    <a href="module-4.md">← Module 4</a> | <strong>Module 5</strong> | <a href="module-6.md">Module 6 →</a>
</p>
