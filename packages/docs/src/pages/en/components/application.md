---
meta:
  title: Application
  description: Vuetify comes equipped with a default markup that makes it easy to create layouts (boilerplate) for any Vue application.
  keywords: default layout, vuetify default markup, vuetify default layout
related:
  - /features/theme/
  - /components/app-bars/
  - /components/navigation-drawers/
---

# Application

Application components are the building blocks for creating layouts

![App Entry](https://cdn.vuetifyjs.com/docs/images/components-temp/v-app/v-app-entry.png)

----

## Usage

The `v-app` component serves as a root level layout and theme provider. It replaces the default `<div id="app">` root element that Vue uses to mount and initiate your application. The following markup is a basic example of what your Vue entry file might look like:

```html { data-resource="App.vue" }
<v-app>
  <v-navigation-drawer></v-navigation-drawer>

  <v-app-bar></v-app-bar>

  <v-main>
    <!-- Application content -->
  </v-main>
</v-app>
```

<entry />

## Anatomy

There are 7 components that have [Application](/features/application-layout/) support out of the box.

![App Anatomy](https://cdn.vuetifyjs.com/docs/images/components-temp/v-app/v-app-anatomy.png)

| Element / Area | Description |
| - | - |
| 1. [v-app](/api/v-app/) | Root layout component |
| 2. [v-navigation-drawer](/api/v-navigation-drawer/) | Holds navigation components such as [v-list](/components/lists/) |
| 3. [v-system-bar](/api/v-system-bar/) | Used to replicate an application window's system bar |
| 4. [v-app-bar](/api/v-app-bar/) | Used for top level navigation links and application title |
| 5. [v-main](/api/v-main/) | The main content area |
| 6. [v-bottom-navigation](/api/v-bottom-navigation/) | Used for top level navigation links on mobile devices |
| 7. [v-footer](/api/v-footer/) | Contains information and links related to the page. Must use **app** prop |

## API

| Component | Description |
| - | - |
| [v-app](/api/v-app/) | Primary component |
| [v-main](/api/v-main/) | Content area |

## Guide

Vuetify features an application layout system that allows you to easily create complex website designs.

The system is built around an outside-in principle, where each application layout component reserves space for itself in one of four directions&mdash;left, right, up, and down&mdash; leaving the available free space for any subsequent layout component(s) to occupy.

The `v-app` component combines the functionality of the [Application layout](/features/application-layout/) and [Theme providers](/components/theme-providers/) to replace your application's root element.

This guide focuses on the how the `v-app` component is used within your application. For detailed information on the layout service itself and how it positions elements, visit the [Application layout](/features/application-layout/) page.

#### Using layouts

The Vuetify layout system supports a variety of use-cases that range from the ability to nest them multiple times to dynamically changing their composition in real-time. [Application components](#anatomy) automatically bind to the nearest `v-app` or `v-layout` component and are positioned based upon their render order.

### App-bar

A `v-app-bar` is located above the main content and typically used as a container for top level navigation links.

<example file="application/app-bar" />

<alert type="info">

  Application components automatically apply position: **fixed** to the layout element. If your application calls for an _absolute_ element, use the **absolute** prop overwrite this functionality.

</alert>

## Accessibility

By default, `v-main` is assigned the [TR](https://www.w3.org/TR/html51/) tag of [**main**](https://www.w3.org/TR/html51/grouping-content.html#the-main-element) which denotes that it is the main content area of the `body` of a document or application.

<backmatter />
