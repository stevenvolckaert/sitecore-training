<p align="center">
    <a href="module-6.md">← Module 6</a> | <strong>Module 7</strong> | <a href="module-8.md">Module 8 →</a>
</p>

# Module 7: Configuring the Experience Editor

The Experience Editor can be extended. This module handles that topic.

## 7.1 Data Source Restrictions

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

## 7.2 Parameters and Parameters Templates

Additional parameters can be configured on controls, to give authors more control of the presentation, for instance.
Additional Parameters need to be entered in the Experience Editor as key-value pairs of strings. If an author makes a
mistake when specifying the key, the parameter won't work.

This scenario is better covered by using a Parameters template. This template must inherit the `Standard Rendering
Parameters` template.

Of course, the code needs to be adapted to read the parameters, and apply them to the Web Forms control (or MVC view).

## 7.3 Placeholder Settings (slide 230)

* Placeholder settings make placeholder controls (`<sc:Placeholder />`) selectable in the Experience Editor.
* These are used to set up restrictions in the `Allowed Controls` field. This influences the available options in the
  Experience Editor when adding components.
* It does **not** affect the presentation details dialogs in Content Editor or Experience Editor. 

**Allowed Controls**: Define the components that can be added to a placeholder. When empty, all is allowed.

### Compatible Renderings

Configured on component definition items (like a Sublayout), **Compatible Renderings** allow one to limit the control
selection in another way. If two components are defined as compatible (both their definition items must have this
configured), one can swap them out in the Experience Editor.

*For this to work, both controls **must** also be allowed to be placed on the placeholder!*

## 7.4 Advanced Experience Editor Configuration

Custom Experience buttons can be created: You'll need to inherit some kind of Sitecore base class (or interface),
implement it, and then link it in the web.config. Tip: You can use Sitecore Rocks to view the web.config!

Custom Experience buttons are persisted in the `core` database (`/core/sitecore/content/Applications/WebEdit/Custom
Experience Buttons`).

It's also possible to add custom Experience Editor buttons to fields! Go the the template, and edit the field definition
item.

|||
|--------------------------:|----------------------------------------------------------------------|
| Component Toolbar Buttons | Assigned in the component definition item (e.g. Sublayout)           |
| Field Toolbar Buttons     | Assigned on the field definition item (child item of data templates) |

The `<sc:EditFrame />` ASP.NET Web Forms control surround an area on a page or compnent, and display buttons allowing
you to edit fields that would not normally be editable in the Experience Editor.

<p align="center">
    <a href="module-6.md">← Module 6</a> | <strong>Module 7</strong> | <a href="module-8.md">Module 8 →</a>
</p>
