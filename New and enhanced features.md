New and enhanced features
Update Time: 2025-03-07 02:27
Ability Kit
Added support for creating an app context based on a specified physical screen ID to facilitate access and use of other on-screen information. (API Reference)
Added support for pulling up UIAbility through the C API. Only 2in1 devices are supported. (API Reference)
A callback method that supports app pre-shutdown is added, which can be used to ask the user whether to take the action immediately or cancel the action. Only 2in1 devices are supported. (API Reference - UIAbility, API Reference - AbilityStage)
ArkData
The new intelligent data platform provides data intelligence capabilities on the device side and completes the closed-loop of data and AI intelligence on the device side. Only 2in1 devices are supported. (Guide, API Reference)
UDMF adds the ability to obtain progress information and data. (API Reference)
ArkGraphics 2D
NativeBuffer支持的格式新增BLOB格式(NATIVEBUFFER_PIXEL_FMT_BLOB)和RGBA16 float格式(NATIVEBUFFER_PIXEL_FMT_RGBA16_FLOAT)。 (API参考)

ArkTS
The maximum number of runtime environments that can be created by a process has been increased from 16 to 64, and the number of worker child threads that need to be running at the same time and the total number of runtimes created by a process cannot exceed 80.

ArkUI
The base component adds the ability to insert text at a specified location on the edited text and delete the content of the specified area. (API Reference)
Focus axis events are added to general events, which support response to gamepad axis events (API Reference-C API, API Reference-ArkTS API); The C API additionally supports getting the value of the operation type of the current axis event (API Reference - C API).
Added support for setting whether the unselected grid dot is automatically selected when the password path passes. (API Reference)
Window Management adds the C API for window management, which is mainly used to set and obtain the properties of a specified window, and set the status bar style and navigation bar style of a specified window. (API Reference)
The Image component supports the ability to overwrite the original color, which only takes effect for SVG sources. (API Reference)
The Image component supports automatic transformation by image matrix, providing automatic transformation optimization when displaying grid-type thumbnails in a library-like scene. (API Reference)
Added support for Tabs and Swiper to set the mouse wheel page turning mode. (API Reference - Tabs Portlet, API Reference - Swiper Portlet)
NavDestination supports callbacks when an event returns, which is used to pass parameters when an event returns. (API Reference)
The TextPicker component adds support for configuring the text style of each selection. (API Reference)
The C API is added to the Progress component, which supports setting the linear progress bar style. (API Reference)
In the Screen Properties module, the Folding Screen State Enumeration has added several state definitions for Axis 2. (API Reference)
Added a NODE_BACKDROP_BLUR for the background blur effect property in the Node property style of the C API. (API Reference)
Added support for cross-language capabilities in FrameNode. (API Reference)
Added support for FrameNode to select the expansion mode of child nodes when traversing nodes. (API Reference)
Added support for setting the width and height to fit the layout of the parent component. (API Reference)
文本组件在TextMenuItem中新增支持快捷键提示(labelInfo)。 (API参考)
The three types of pop-up widgets support setting pop-up display levels and related attributes and effects (levelMode, levelUniqueId, immersiveMode). (API Reference - List Selection Pop-up, API Reference - Warning Pop-up, API Reference - Custom Pop-up)
bindSheet adds support for the radius attribute to set the radius of the half-modal page. Added support for non-gesture switching (detentSelection) attribute. (API Reference)
The Navigation Point component is added, which provides two navigation point styles: Dotted Navigation Point and Numeric Navigation Point. (API Reference)
The Swiper and Tabs components have added support for animated jumps. (API Reference - Swiper Component C API, API Reference - Swiper Component ArkTS API, API Reference - Tabs Component ArkTS API)
The Swiper component supports sliding behavior interception events, which can determine whether sliding behavior is allowed. Among them, the C API is controlled by attributes, and the attribute name is NODE_SWIPER_EVENT_ON_CONTENT_WILL_SCROLL. (API Reference - C API, API Reference - ArkTS API)
The accessibility framework of ArkUI is added support for third-party platforms to find the previous or next focus (ARKUI_ACCESSIBILITY_NATIVE_ACTION_TYPE_NEXT_HTML_ITEM, ARKUI_ACCESSIBILITY_NATIVE_ACTION_TYPE_PREVIOUS_HTML_ITEM). (API Reference)
Third-party platforms are connected to the ArkUI accessibility framework, and multi-instance scenarios are supported. (API Reference)
ohos.arkui.observer模块NavDestination组件信息新增NavDestination类型和uniqueId。 （API参考）
Added support for screenshots of C APIs. (API Reference)
UIContext added support for getting screenshots of loaded components by uniqueId. (API Reference)
UIContext adds the ability to get the layout information of the meta service menuBar relative window. (API Reference)
The C API is added for general events, and you can get the ID of the current touch event. (API Reference)
A new interface with the same name has been added to the window for 2in1 devices to set the application window size limit. (API Reference)
A new interface with the same name has been added to the window to specify the position of the mouse within the window and move the window. (API Reference)
Added asynchronous callback for window close event listening for 2in1 devices. (API Reference)
Added support for enabling the monitoring of picture-in-picture window size change events. (API Reference)
Added support for dynamically setting the title bar of the window. (API Reference)
Added the window support mode (full screen, floating window, split screen, etc.) of the main window. (API Reference)
NavDestination新增支持设置是否隐藏标题栏中的返回键。 (API参考)
The new C API supports the ability to control focus and handle focus events. (API Reference)
The C API is added to support forwarding cloned events. (API Reference)
PopupsboardAvavOdeode. I'm not going to be afraid of it. (API))
The pop-up window added support for setting the distance of the keyboard avoidance. Among them, the ArkTS API is provided as a property, and you can search for the keyword keyboardAvoidDistance in the table to which the link points. (API Reference-C API, API Reference-Custom Pop-up ArkTS API, API Reference-Pop-up Module ArkTS API)
Added support for setting ResourceStr images for attribute strings. (API Reference)
Added support for obtaining the image color filter effect (colorFilter) of attribute strings. (API Reference)
Added the ability to get the drag and drop data from the drag and drop progress bar. (API Reference-C API, API Reference-ArkTS API, where the specific method in the table linked to by the ArkTS API can be retrieved for startDataLoading)
Added support for defining component screenshot areas. (API Reference)
Added component parameters to the Tabs component, which allows you to set the tab location of the Tabs. (API Reference)
Added support for triggering callbacks when the text content is about to change. (API Reference-Search, API Reference-TextArea, and TextInput)
Added support for getting touch-related events from left or right hand, involving multiple modules:
The C API is added to the event module. (API Reference)
The hand attribute of the FingerInfo object is added to the binding gesture method. (API Reference)
The TouchObject object has a new hand property. (API Reference)
The Hand attribute is added to the clickevent object. (API Reference)
Added support for checking the number of fingers on the touch screen, involving multiple modules:
NDKㅺ⻰⻪ (API))
Added a property to set whether to check the number of fingers touching the screen isFingerCountLimited in the component. You can view this property on the reference page for each component. (API Reference - Long Press Gesture Event, API Reference - Swipe Gesture Event, API Reference - Pinch Gesture Event, API Reference - Rotate Gesture Event, API Reference - Swipe Event, API Reference - Double-Click and Multi-Tap Events)
Added support for setting the priority of key event processing and the ability to redispatch. Involve:
NDK adds a C API for setting the priority of key event processing. (API Reference)
A new NODE_DISPATCH_KEY_EVENT has been added to the ArkUI_NodeEventType enumeration in the NDK to indicate the redispatch event of component key events (C API). (API Reference)
UIContext adds the ArkTS API to set the priority of key event processing. (API Reference)
UI UI ៕𑁅ArkTS API. (API))
C API supports NODE_CHECKBOX_GROUP related capabilities. You can search for the keyword in the API reference. (API Reference)
AppGallery Kit
The application metadata management service is added to support the management of dynamic icons. (Guide, API Reference)

ArkWeb
Added support for persistent cookies. (API Reference)

Basic Service Kit
Added support for uploading and downloading multiple files using a single upload request, which can be configured through the multipart parameter of Config. (API Reference)
剪贴板新增支持设置进度指示条。 (API Reference - C API, API Reference - ArkTS API)
Camera Kit
Added support for obtaining the type of distributed camera device. (API Reference)
Added support for mirrored recording. (API Reference)
Connectivity Kit
The Wi-Fi management capability of the wifiManager module is available for enterprise applications. (API Reference)

Core File Kit
The file picker adds the ability to batch authorize files. (Guide, API Reference)

Device Security Kit
Added support for anti-fraud applications to obtain scam messages. (Guide)
Added support for anti-fraud applications to obtain fraudulent call records. (Guide)
Enterprise Data Guard Kit
Added support for watermark protection when KIA files are opened. (Guide)
Added support for enterprise recovery key management. (Guide)
IAP Kit
PurchaseParameter新增购买参数quantity，支持单次购买多个商品。 （API参考）
Added support for refunds of non-game app orders. (API Reference)
NAME Kit
Added support for moving the input method window. (API Reference)

Input Kit
Added support for the recognition and distribution of key events for gamepad devices. (API Reference)

Localization Kit
Added the ability to obtain simplified representations of languages, such as changing the simplified representations of "en-Latn-US" to "en". (API Reference)

Map Kit
Added support for setting and viewing the zoom ratio of the logo. (Guide)
Added support for displaying 3D globes on maps. (Guide)
Added support for setting custom tile layers. (Guide)
Added support for using textures to achieve polyline textures. (API Reference)
Added support for Marker collision detection. (Guide)
Added support for setting textures for polyline segments and setting textures dynamically. (API Reference)
Added petalMaps module, which supports pulling up petal maps. (Guide, API Reference)
Added support for setting the theme color of map Picker. (API Reference)
Added support for pulling up sub-windows in the zoning query control. (API Reference)
Added support for map Picker to close the callback. (API Reference)
Added support for aggregating the expansion icon and clicking the callback. (API Reference)
MDM Kit
Added support for setting browser hosting policies for specified browsers. (API Reference)
Media Kit
Added support for screen recording: Added a callback to get the screen ID of the screen recording. (API Reference)

Media Library Kit
Added support for previewing and replacing images in albums via photoPicker. (API Reference)

Multimodal Awareness Kit
Added support for motion perception, which can perceive user behaviors and actions. (Guide, API Reference)

Preview Kit
Added C API to accelerate file opening. (Guide, API Reference)

Remote Communication Kit
The OntimeInfo API is added to listen for the success/failure of an HTTP request. (API Reference)

Speech Kit
TextReader adds support for logging out and pulling callbacks to the bottom of playlists with user-defined parameters. (API Reference)
