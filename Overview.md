==Overview==
Update Time: 2025-03-07 02:27
overview
In order to make it easier for developers to perceive the impact of changes on their applications, we categorize them as follows:

Changes for all applications
Such changes may affect all applications running on mirrored devices with the latest version of HarmonyOS NEXT Developer, regardless of whether your application is developed using API 14 or earlier.

These changes need to be adapted by the app.

Changes to UX styles or effects
Only the UX style and effect provided by the system are changed, and the developer can judge whether the overall style or expected effect of the app will be affected according to the change description.

Adaptation recommendations for changes fall into the following categories:

Adaptation required: Such changes will directly affect the invocation of interfaces or the use of functions, and inappropriate changes may cause the application project to fail to compile successfully, or other unforeseen errors. It is strongly recommended that developers check the change description as soon as the new version is enabled, and refer to the adaptation guide to adjust the changes involved as soon as possible.
Suggested adaptation: Adaptation is not suitable for this type of change, which will not cause the compilation of the application project to fail, but may deviate from the original intention of the developer, such as changes in the size of the component, changes in the duration of animations, etc. Developers need to learn more about this change and analyze the impact to adapt the app to the desired state.
No adaptation required: Such changes are generally positive optimizations and do not negatively affect the application project, nor do they affect the layout, interaction, etc. Developers can check and understand the changes. Some changes may provide configuration capabilities, and if developers want to keep the original state, they can also refer to the adaptation guide to adjust it.
Changes for all applications
Kit

Description of the change

Historical Engineering Adaptation Recommendations

ArkUI

Image、Text和ListItem组件onDragStart接口默认行为变更

Adaptation is required

Axis events can be triggered by BEGIN, END, and CANCEL callbacks

No adaptation required

The SetStyledString operation of the TextController allows you to save the property string information of the set to the TextController

Adaptation is required

On 2in1 devices, the level of the floating window is adjusted from lower than the dock bar to higher than the dock bar

No adaptation required

Call Service Kit

The calling app doesn't display the call capsule when it's in the foreground

Adaptation is required

Preformance Analysis Kit

HiAppEvent模块onReceive、OH_HiAppEvent_OnReceive、takeNext接口支持应用分身故障日志订阅隔离

No adaptation required

Changes to UX styles or effects
Description of the change

Historical Engineering Adaptation Recommendations

Motion photo autoplay effect changed

No adaptation required

The NavDestination title bar toolbar supports sliding and hiding after 2 seconds, and the display will not be restored. Tabs component TabBar show and hide animation changes

No adaptation required
