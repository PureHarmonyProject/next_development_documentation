**Changes to UX styles or effects**
Update Time: 2025-03-07 02:27
341
Change Title: Changed the autoplay effect of dynamic photos

Reason for change

Movie photos zoom in to 1.1x when playing automatically, and flickering and shaking effects are noticeable when sliding left and right for movie photos to autoplay. To improve the experience on the user interface, Motion Photos is set to autoPlay when autoplay does not zoom in.

Impact of Changes

No application adaptation is required for this change.

@ohos.multimedia.medialibrary模块中的autoPlay接口ux默认行为规范变更。

Behavior before change: magnified to 1.1x when autoplay is set to autoplay for dynamic photos.

Behavior after change: Motion Photos do not zoom in when autoPlay is set to autoplay.

Starting API Level

13

Interfaces/components changed

@ohos.multimedia.medialibrary模块中的autoPlay接口。

Adaptation guidance

The default behavior changes, and no adaptation is required.

342
illustrate
此变更涉及NavDestination标题栏工具栏和Tabs组件TabBar,详见下述两条说明。

Changed the title: The NavDestination title bar toolbar supports sliding and hiding after 2 seconds, and the display will not be restored

Reason for change

UX specification changes.

Impact of Changes

This change does not involve app adaptation.

Before: The title bar toolbar of the NavDestination component is hidden by scrolling up and down, and it is automatically displayed after 2 seconds of inactivity.

After: The title bar toolbar of the NavDestination component is hidden by scrolling up and down, and it will not be automatically displayed after 2 seconds of inactivity.

Start API level

14

Interfaces/components changed

NavDestination.bindToScrollable, NavDestination.bindToNestedScrollable

Adaptation guidance

The default behavior changes, and no adaptation is required.

Change Title: Changes to the display and hide animations of the Tabs component TabBar

Reason for change

UX specification changes.

Impact of Changes

This change does not involve app adaptation.

Before the change: The TabBar of the Tabs component is hidden by sliding up, disappearing by sliding, and is automatically displayed after 2 seconds of inactivity.

After the change: The TabBar of the Tabs component is hidden by sliding up and disappearing, and it will not be automatically displayed after 2 seconds of inaction.

Start API level

13

Interfaces/components changed

UIContext的bindTabsToScrollable、bindTabsToNestedScrollable接口

Adaptation guidance

The default behavior changes, and no adaptation is required.
