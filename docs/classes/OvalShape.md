**super**: **[Shape](Shape.md)**

Represents an oval shape.

### Events

* **Load**()
This event is called when the object becames available in the current runtime system.

* **WillShow**()
The view is about to be added to the App's views hierarchy.

* **WillHide**()
The view is about to be removed from the App's views hierarchy.

* **TouchesBegan**(**touches**: **[Object](../gravity/types.md)**): <strong>[Bool](../gravity/types.md)</strong> 
This event is called when one or more new touches occurred in this view and the userInteractionEnabled property is enabled. Return "true" if you want to consume the event and not forward it to the next responder, return "no" to forward any events that you do not handle yourself.

* **TouchesMoved**(**touches**: **[Object](../gravity/types.md)**, **touchInside**: **[Bool](../gravity/types.md)**): <strong>[Bool](../gravity/types.md)</strong> 
This event is called when the location or force of a touch changes and the userInteractionEnabled property is enabled. Return "true" if you want to consume the event and not forward it to the next responder, return "no" to forward any events that you do not handle yourself.

* **TouchesEnded**(**touches**: **[Object](../gravity/types.md)**, **touchInside**: **[Bool](../gravity/types.md)**): <strong>[Bool](../gravity/types.md)</strong> 
This event is called when one or more fingers are raised and the userInteractionEnabled property is enabled. Return "true" if you want to consume the event and not forward it to the next responder, return "no" to forward any events that you do not handle yourself.

* **TouchesCancelled**(**touches**: **[Object](../gravity/types.md)**): <strong>[Bool](../gravity/types.md)</strong> 
This event is called when the sysyem receives a system interruption (such as a system alert) requiring cancellation of the touch sequence and the userInteractionEnabled property is enabled. Return "true" if you want to consume the event and not forward it to the next responder, return "no" to forward any events that you do not handle yourself.

* **DidShow**()
The view has been added to the App's views hierarchy.

* **DidHide**()
The view has been removed from the App's views hierarchy.

* **Unload**()
This event is called when the object has been removed from the current runtime system (but not yet deallocated).



### Methods

* **func** **animate**(**duration**: **[Float](../gravity/types.md)**, **delay**: **[Float](../gravity/types.md)**, **options**: **<a href="#_enum_AnimationOption">AnimationOption</a>**, **closure**: **[Closure](../gravity/closure.md)**, **completion**: **[Closure](../gravity/closure.md)**)
Animate changes to one or more views using the specified duration, delay, options and completion handler.

* **func** **setFocus**()
Force focus to be set to the selected control. For TextField and TextView that means force Keyboard to appear.

* **func** **clearFocus**()
Clear focus from selected control





### Enumeration

#### AnimationOption
 * .AllowAnimatedContent
 * .AllowUserInteraction
 * .Autoreverse
 * .BeginFromCurrentState
 * .CurveEaseIn
 * .CurveEaseInOut
 * .CurveEaseOut
 * .CurveLinear
 * .LayoutSubviews
 * .OverrideInheritedCurve
 * .OverrideInheritedDuration
 * .OverrideInheritedOptions
 * .Repeat
 * .ShowHideTransitionViews
 * .TransitionCrossDissolve
 * .TransitionCurlDown
 * .TransitionCurlUp
 * .TransitionFlipFromBottom
 * .TransitionFlipFromLeft
 * .TransitionFlipFromRight
 * .TransitionFlipFromTop
 * .TransitionNone



