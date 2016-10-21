p align="center">
    <a href="module-8.md">← Module 8</a> | <strong>Module 9</strong> | <a href="module-10.md">Module 10 →</a>
</p>

# Module 9: Beyond the Developer Environment

## 9.1 Caching and Performance (slide 279)

There are three different caches:

* Item cache;
* Data cache;
* Prefetch cache - created when the web application starts.

See the Performance Tuning Guide for guidance regarding caching configuration (of Item retrieval)

HTML caching is also possible, for components. However, this is disabled by default. This can be enabled on the
component definition item, on the `__Standard Values` of a template, and per component instance.

Statically bound components have cache settings set in the markup. See slide 281.

The HTML cache is cleared in its intirety when publishing (any form of publishing).

### Experience Editor Debug Mode (slide 286)

Use Debug mode (selectable in the Experience Editor) - it contains a trace of e.g. sublayouts that were created to
render the page, and the time it took.

Debug mode always runs against the `web` database.

## 9.2 Publishing (slide 288)

Sitecore 8.2 introduces a *publishing service*. It's performance is optimized; publishing goes **much** faster than
using the other publish methods.

## 9.3 Installing and Scaling Sitecore (slide 294)

## 9.4 Team Development and the Development Environment

## 9.5 Basic Security (slide 312)

Role-based access control (RBAC) is supported: One assigns access rights (allow, deny, or inherit) to users and roles.
Roles can inherit from each other.

When access rights conflict, *explicit deny* always takes precedence. However, this setting (setting *allow*) can be
overridden at user level.

Security Editor: Used to define access rights; Access Viewer: Used to view the resulting access rights.

## 9.6 Workflows

Items can be assigned *commands*, a step to be executed by a person, and *actions*, which is executed automatically.

<p align="center">
    <a href="module-8.md">← Module 8</a> | <strong>Module 9</strong> | <a href="module-10.md">Module 10 →</a>
</p>
