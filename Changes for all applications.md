Changes for all applications
Update Time: 2025-03-07 02:27
ArkUI
363
变更标题:Image、Text和ListItem组件onDragStart接口默认行为变更

Reason for change

The Image, Text, and ListItem components do not take effect after setting the builder attribute in the DragItemInfo return value of the onDragStart API.

Impact of Changes

This change involves application adaptation, and only applies to the Image, Text, and ListItem components.

Before: After setting the builder attribute in the return value of the onDragStart API, the pixelMap and extraInfo attributes could not be resolved.

After: After setting the builder property in the return value of the onDragStart API, the pixelMap and extraInfo properties can be resolved.

illustrate
This change has been versioned, and if the application does not compile with the SDK version after the change was introduced, it will not be affected by the change and can still maintain the interface behavior before the change on the later version of the system.

Start API level

API 11

Interfaces/components changed

涉及组件： Image, Text, ListItem组件。

涉及接口: onDragStart(event: (event: DragEvent, extraParams?: string) => CustomBuilder | DragItemInfo)

Adaptation guidance

The return value of the onDragStart interface is used to specify the image (pixelMap, builder) displayed during the drag-and-drop process and the extra information (extraInfo) carried by the component during the drag-and-drop process. After the change, pixelMap has a higher display priority than builder. If the developer has set both pixelMap and builder, the pixelMap property in the return value should be removed. Similarly, if you don't want to pass extraInfo, you should remove the property. The specific implementation code is as follows:

@Entry
@Component
struct SlideExample {
  build() {
    Row() {
      Image()
 . onDragStart((event) => {
        return {
          builder: () => { this.pixelMapBuilder },
          If you need to drag and drop the builder, you need to remove the assignment of the pixelMap property.
          // pixelMap:this.pixelMap,
          If the builder is set and you don't need to pass extraInfo, you need to remove the assignment of the extraInfo property.
          // extraInfo: "test"
        }
      })
 }. height('100%')
  }
}
356
Changed title: Axis events can be triggered by BEGIN, END, and CANCEL callbacks

Reason for change

Developers cannot listen to event callbacks of the BEGIN, END, and CANCEL types of axis events.

Impact of Changes

This change does not involve app adaptation.

Before: Developers listen to axis event callbacks through the OH_NativeXComponent_RegisterUIInputEventCallback API, but cannot receive event callbacks of BEGIN, END, and CANCEL.

After the change: Developers can listen to axis event callbacks through the OH_NativeXComponent_RegisterUIInputEventCallback API, and can receive event callbacks of BEGIN, END, and CANCEL.

illustrate
This change has been versioned, and if the application does not compile with the SDK version after the change was introduced, it will not be affected by the change and can still maintain the interface behavior before the change on the later version of the system.

Start API level

API 12

Interfaces/components changed

OH_NativeXComponent_RegisterUIInputEventCallback interface.

Adaptation guidance

The default behavior changes, and no adaptation is required.

348
Change title: The SetStyledString API of the TextController allows you to save the property string information of the set to the TextController

Reason for change

Optimized the binding time between attribute strings and Text components.

Impact of Changes

This change involves app adaptation.

Before: When a developer calls the setStyledString API of the TextController to set a property string, if the TextController has not been bound to the corresponding Text at the time of the call, the setting will be invalid.

After: When a developer calls the setStyledString API of the TextController, the TextController will save the set property strings. When the TextController is bound to the Text, if the property string saved by calling the setStyledString operation is stored in the TextController, the Text automatically sets the saved property string and displays the corresponding property string.

illustrate
This change has been versioned, and if the application does not compile with the SDK version after the change was introduced, it will not be affected by the change and can still maintain the interface behavior before the change on the later version of the system.

Start API level

API 12

Adaptation guidance

The call to the setStyledString interface is now more flexible, and Text is able to display the property string correctly.

@Entry
@Component
struct StyledStringExample {
  controller: TextController = new TextController()

  aboutToAppear(): void {
    this. controller. setStyledString(new  StyledString("123456")) // 变更前，由于此时controller还未和Text绑定，此次设置不生效。 变更后，属性字符串可以正确的显示
  }

  build() {
    Row() {
      Column() {
        Text(undefined, {controller: this.controller})
 }. width('100%')
 }. height('100%')
  }
}
362
Changed title: On 2in1 devices, the level of the floating window has been adjusted from lower than the dock bar to higher than the dock bar

Reason for change

The TYPE_FLOAT type of floating window created by the application is lower than the Dock and will be blocked by the Dock bar, and the experience does not meet the expectations of the application in scenarios such as video conferencing.

Impact of Changes

This change does not involve app adaptation.

Before: On 2in1 devices, the TYPE_FLOAT type of floating window level is below the dock bar.

New: On 2in1 devices, the TYPE_FLOAT type of floating window is on top of the dock bar.

Start API level

9

Interfaces/components changed

@ohos.window.d.ts

Interface: TYPE_FLOAT

Adaptation guidance

The default behavior changes, and no adaptation is required.

Call Service Kit
359
Change title: The call app doesn't display the call capsule when it's in the foreground

Reason for change

Optimized call experience.

Impact of Changes

This change involves app adaptation.

Before: During a call, even if the app is in the foreground, the call capsule will be displayed, and you can click the capsule to return to the call interface.

After the change: During a call, if the app is in the foreground, the call capsule will not be displayed; If the app is in the foreground but not in the call interface, the app needs to display the picture-in-picture interface to return to the call interface by itself, as shown in the figure.

Before the change

After the change (the foreground is applied, but not the call interface)





Starting API Level

4.1.0(11)

Interfaces/components changed

voipCall.reportIncomingCall（上报来电）

voipCall.reportOutgoingCall（上报去电）

Adaptation guidance

During a call, if the app is not in the foreground, you need to display the picture-in-picture interface to return to the call interface, see Using the Picture-in-Picture feature in the app for details.

Preformance Analysis Kit
324
Change title: The onReceive, OH_HiAppEvent_OnReceive, and takeNext APIs of the HiAppEvent module support application doppelganger fault log subscription isolation

Reason for change

In principle, the design of application clones requires data isolation, and the fault logs of the current application clones are not isolated from the main application, which is not easy to maintain the logs of the clone applications.

Impact of Changes

This change does not involve app adaptation

Before the change: HiAppEvent can obtain the fault logs of both the main application and the clone application in the main application and the clone application.

After the change: HiAppEvent can only obtain the fault logs of the main application in the main application, and the doppelganger application can only obtain the fault logs of the doppelganger application.

Start API level

takeNext接口起始API 9
OnReceiveAPI 11
OH_HiAppEvent_OnReceive interface starting API 12
Interfaces/components changed

@ohos.hiviewdfx.hiAppEvent.d.ts中的onReceive、takeNext接口。

hiappevent.h中的OH_HiAppEvent_OnReceive接口。

Adaptation guidance

The default behavior changes, and no adaptation is required.
