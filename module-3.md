<p align="center">
    <a href="module-2.md">← Module 2</a> | <strong>Module 3</strong> | <a href="module-4.md">Module 4 →</a>
</p>

# Module 3: Presentation

* *Layouts do not have `__Standard Values`.*
* All presentation is stored in the layout's `__Renderings` system field. See [Module ](module-5.md) for more
  information.

## 3.2 Preparing to Build with Visual Studio

## Creating a Layout

* A data template can have *only one* layout (per device). It is always configured in its `__Standard Values`.
* Use the Sitecore Rocks keyboard shortcut (Ctrl+U) to open the Layout designer.
* An item's *presentation details*, also called  *Layout Details*, can be configured on a template's `__Standard
  Values`, and on the template itself. Always configure the presentation details on the template's `__Standard Values`,
  so the inheriting works.

## 3.4 Creating Components

### Component Types

*Components are also frequently called **controls**. Sometimes, they're also referred to as **widgets**.*

| Component Type           | Description                              |
|-------------------------:|------------------------------------------|
| **Layout**               | The main presentation building block. Maps to an ASP.NET Web Forms page (`*.aspx`), or an ASP.NET MVC   *Master Page*. |
| **Sublayout**            | Maps to a ASP.NET Web Forms control (`*.ascx`). |
| **Controller Rendering** | The ASP.NET MVC counterpart of a *Sublayout*. Maps to a ASP.NET MVC *Controller* and *Action Method*. |
| **XSLT Rendering**       | A legacy technology. XSLT renderings are interpreted, not compiled, and hence slower to render.
| **Sitecore Web Control** | ASP.NET Web Forms controls, like `<sc:Placeholder />`, `<sc:Text />` and `<sc:Image />`. Equivalent ASP.NET MVC counterparts exist likely exist as well. |

Enter placeholder keys using lowercase. Implementing this convention ensures that the difference between placeholders
and components can be observed when using the Experience Editor. *In this editor, there's no other way to differentiate
the two from each other.*

[Module 7](module-7.md) covers *Placeholder Settings*, Sitecore items required by the Experience Editor.

## 3.5 Dynamic Binding

| | |
|--------------------:|-----------|
| **Static Binding**  | Presentation of a page is handled solely by a single layout. For ASP.NET Web Forms, the `<sc:Sublayout />` web control can be used. It is very likely that a ASP.NET MVC counterpart exists as well. |
| **Dynamic Binding** | The process of binding components to a layout, sublayout, or controller rendering (ASP.NET MVC view). Requires placeholders to be present on the layout: The component is plugged into the placeholder dynamically (on-demand). ***Important: Any number of components can be bound to a specified placeholder. You're not limited to binding a single component to a single placeholder.*** |

## 3.6 Rendering Content

Sitecore Web Controls are ASP.NET Web Controls. Use them to display the appropriate content, and to make the content
editable in Experience Editor.

* Every control has a mandatory `Field` attribute. Note: The equivalent for `<sc:FieldRenderer />` is `FieldName`.

## Vocabulary

* **Presentation Details**: An item’s presentation details are instructions that specify which layout and components are
  used and which placeholders to use for dynamically binding components.
* **Layout**: A layout is your page canvas. It is linked to an .aspx file on the file system, which may also be referred
  to as a ‘layout’. You can have one layout per item per device.
* **Component**: A unit of functionality. All components have a definition item in the Sitecore tree and a file on the
  file system. Components can be: Sitecore Sublayouts (.ascx), XSLT renderings (.xslt), or web controls (.cs).
* **Placeholder**: A placeholder is a Sitecore control that determines where on a page a component can be inserted. It
  is added to regular HTML markup and must have a key.

<p align="center">
    <a href="module-2.md">← Module 2</a> | <strong>Module 3</strong> | <a href="module-4.md">Module 4 →</a>
</p>
