<p align="center">
    <a href="module-6.md">← Module 6</a> | <strong>Module 7</strong> | <a href="module-8.md">Module 8 →</a>
</p>

# Module 7: Configuring the Experience Editor

The Experience Editor can be extended. This module handles that topic.

## Datasource Location and Template Restrictions

When datasource location is configured, the *Select the Associated Content* dialog box (in Experience Editor) appears by
default when adding a new component.

The `Datasource Location` and `Datasource Template` fields are configured on *component definition items* (e.g.
sublayouts). The location is the parent data item in the tree of the things that need to be selectable in the control.
The template is used to restrict selecting a specified template. The `Datasource Location` field also accepts a Sitecore
Query.

To make a template with customized parameters, your template must inherit `Standard Rendering Parameters` Then fill in
the `Parameter Template` field in the rendering (e.g. sublayout). If not, you'll get a very strange error when trying to
edit the parameters in the Experience Editor.

Compatible renderings is a placeholder setting (`Placeholder Settings` item in `/sitecore/Layout/Placeholder Settings/`)
can be used to configure the Experience Editor also: Authors will be able to select only the compatible renderings in a
certain placeholder.

## 7.4 Advanced Experience Editor Configuration

Custom Experience buttons can be created: You'll need to inherit some kind of Sitecore base class (or interface),
implement it, and then link it in the web.config. Tip: You can use Sitecore Rocks to view the web.config!

Custom Experience buttons are persisted in the `core` database (`/core/sitecore/content/Applications/WebEdit/Custom
Experience Buttons`).

It's also possible to add custom Experience Editor buttons to fields! Go the the template, and edit the field
definition item.

|||
|--------------------------:|----------------------------------------------------------------------|
| Component Toolbar Buttons | Assigned in the component definition item (e.g. Sublayout)           |
| Field Toolbar Buttons     | Assigned on the field definition item (child item of data templates) |

The `<sc:EditFrame />` ASP.NET Web Forms control surround an area on a page or compnent, and display buttons allowing
you to edit fields that would not normally be editable in the Experience Editor.

<p align="center">
    <a href="module-6.md">← Module 6</a> | <strong>Module 7</strong> | <a href="module-8.md">Module 8 →</a>
</p>
