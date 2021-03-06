---
-api-id: T:Windows.UI.Input.Inking.InkInputProcessingConfiguration
-api-type: winrt class
-api-device-family-note: xbox
---

<!-- Class syntax.
public class InkInputProcessingConfiguration : Windows.UI.Input.Inking.IInkInputProcessingConfiguration
-->

# Windows.UI.Input.Inking.InkInputProcessingConfiguration

## -description
Manages how input is processed by the [InkPresenter](inkpresenter.md) object.

## -remarks
Primary input is not from (or modified by) a secondary affordance, such as a pen barrel button, pen eraser tip, right mouse button, or similar.

Secondary input, by default, is processed as primary input and rendered as an [InkStroke](inkstroke.md) by the [InkPresenter](inkpresenter.md). For custom handling of secondary input by your application, set [InkInputProcessingConfiguration.RightDragAction](inkinputprocessingconfiguration_rightdragaction.md) to [LeaveUnprocessed](inkinputrightdragaction.md). This indicates that input should be passed through the [InkPresenter](inkpresenter.md) as [UnprocessedInput](inkpresenter_unprocessedinput.md) for custom processing.

If [InkInputProcessingConfiguration.Mode](inkinputprocessingconfiguration_mode.md) is set to [None](inkinputprocessingmode.md), the value of [RightDragAction](inkinputprocessingconfiguration_rightdragaction.md) is ignored and input is always passed as [UnprocessedInput](inkpresenter_unprocessedinput.md) through to your app for custom processing.

If [InkInputProcessingConfiguration.Mode](inkinputprocessingconfiguration_mode.md) is set to [Inking](inkinputprocessingmode.md) or [Erasing](inkinputprocessingmode.md), the value of [RightDragAction](inkinputprocessingconfiguration_rightdragaction.md) must be set to [LeaveUnprocessed](inkinputrightdragaction.md) to pass input as [UnprocessedInput](inkpresenter_unprocessedinput.md) through to your app for custom processing.

To manage what secondary input is processed by your app, see [InkInputConfiguration](inkinputconfiguration.md).

## -examples

## -see-also
[InkPresenter.InputProcessingConfiguration](inkpresenter_inputprocessingconfiguration.md), [Pen and stylus interactions](http://msdn.microsoft.com/library/3da4f2d2-5405-42a1-9ed9-3a87bcd84c43), [Ink sample](http://go.microsoft.com/fwlink/p/?LinkID=620308), [Simple ink sample](http://go.microsoft.com/fwlink/p/?LinkID=620312), [Complex ink sample](http://go.microsoft.com/fwlink/p/?LinkID=620314)