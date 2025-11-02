
======== Exception caught by rendering library =====================================================
The following assertion was thrown during performLayout():
RenderBox was not laid out: _RenderLayoutBuilder#30fbf relayoutBoundary=up12 NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
'package:flutter/src/rendering/box.dart':
Failed assertion: line 1965 pos 12: 'hasSize'


Either the assertion indicates an error in the framework itself, or we should provide substantially more information in this error message to help you determine and fix the underlying cause.
In either case, please report this assertion by filing a bug on GitHub:
  https://github.com/flutter/flutter/issues/new?template=2_bug.yml

The relevant error-causing widget was: 
  Stack Stack:file:///F:/real/lib/const/widget.dart:687:11
When the exception was thrown, this was the stack: 
#2      RenderBox.size (package:flutter/src/rendering/box.dart:1965:12)
#3      ChildLayoutHelper.layoutChild (package:flutter/src/rendering/layout_helper.dart:53:18)
#4      RenderStack._computeSize (package:flutter/src/rendering/stack.dart:580:43)
#5      RenderStack.performLayout (package:flutter/src/rendering/stack.dart:607:12)
#6      RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#7      RenderBox.layout (package:flutter/src/rendering/box.dart:2382:11)
#8      RenderProxyBoxMixin.performLayout (package:flutter/src/rendering/proxy_box.dart:104:21)
#9      _RenderCustomClip.performLayout (package:flutter/src/rendering/proxy_box.dart:1431:11)
#10     RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#11     RenderBox.layout (package:flutter/src/rendering/box.dart:2382:11)
#12     ChildLayoutHelper.layoutChild (package:flutter/src/rendering/layout_helper.dart:52:11)
#13     RenderFlex._computeSizes (package:flutter/src/rendering/flex.dart:868:45)
#14     RenderFlex.performLayout (package:flutter/src/rendering/flex.dart:903:32)
#15     RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#16     RenderBox.layout (package:flutter/src/rendering/box.dart:2382:11)
#17     ChildLayoutHelper.layoutChild (package:flutter/src/rendering/layout_helper.dart:52:11)
#18     RenderFlex._computeSizes (package:flutter/src/rendering/flex.dart:808:43)
#19     RenderFlex.performLayout (package:flutter/src/rendering/flex.dart:903:32)
#20     RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#21     RenderBox.layout (package:flutter/src/rendering/box.dart:2382:11)
#22     RenderPadding.performLayout (package:flutter/src/rendering/shifted_box.dart:238:12)
#23     RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#24     RenderBox.layout (package:flutter/src/rendering/box.dart:2382:11)
#25     RenderProxyBoxMixin.performLayout (package:flutter/src/rendering/proxy_box.dart:104:21)
#26     RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#27     RenderBox.layout (package:flutter/src/rendering/box.dart:2382:11)
#28     RenderPadding.performLayout (package:flutter/src/rendering/shifted_box.dart:238:12)
#29     RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#30     RenderBox.layout (package:flutter/src/rendering/box.dart:2382:11)
#31     RenderProxyBoxMixin.performLayout (package:flutter/src/rendering/proxy_box.dart:104:21)
#32     RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#33     RenderBox.layout (package:flutter/src/rendering/box.dart:2382:11)
#34     RenderProxyBoxMixin.performLayout (package:flutter/src/rendering/proxy_box.dart:104:21)
#35     RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#36     RenderBox.layout (package:flutter/src/rendering/box.dart:2382:11)
#37     RenderSliverList.performLayout.advance (package:flutter/src/rendering/sliver_list.dart:251:18)
#38     RenderSliverList.performLayout (package:flutter/src/rendering/sliver_list.dart:283:12)
#39     RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#40     RenderSliverEdgeInsetsPadding.performLayout (package:flutter/src/rendering/sliver_padding.dart:139:12)
#41     RenderSliverPadding.performLayout (package:flutter/src/rendering/sliver_padding.dart:361:11)
#42     RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#43     RenderViewportBase.layoutChildSequence (package:flutter/src/rendering/viewport.dart:534:13)
#44     RenderViewport._attemptLayout (package:flutter/src/rendering/viewport.dart:1512:12)
#45     RenderViewport.performLayout (package:flutter/src/rendering/viewport.dart:1421:20)
#46     RenderObject._layoutWithoutResize (package:flutter/src/rendering/object.dart:2332:7)
#47     PipelineOwner.flushLayout (package:flutter/src/rendering/object.dart:1013:18)
#48     RendererBinding.drawFrame (package:flutter/src/rendering/binding.dart:494:19)
#49     WidgetsBinding.drawFrame (package:flutter/src/widgets/binding.dart:918:13)
#50     RendererBinding._handlePersistentFrameCallback (package:flutter/src/rendering/binding.dart:360:5)
#51     SchedulerBinding._invokeFrameCallback (package:flutter/src/scheduler/binding.dart:1297:15)
#52     SchedulerBinding.handleDrawFrame (package:flutter/src/scheduler/binding.dart:1227:9)
#53     SchedulerBinding._handleDrawFrame (package:flutter/src/scheduler/binding.dart:1085:5)
#54     _invoke (dart:ui/hooks.dart:170:13)
#55     PlatformDispatcher._drawFrame (dart:ui/platform_dispatcher.dart:401:5)
#56     _drawFrame (dart:ui/hooks.dart:140:31)
(elided 2 frames from class _AssertionError)
The following RenderObject was being processed when the exception was fired: RenderStack#e1f37 relayoutBoundary=up11 NEEDS-LAYOUT NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...  parentData: <none> (can use size)
...  constraints: BoxConstraints(w=438.0, 0.0<=h<=Infinity)
...  size: MISSING
...  alignment: Alignment.bottomCenter
...  textDirection: ltr
...  fit: loose
RenderObject: RenderStack#e1f37 relayoutBoundary=up11 NEEDS-LAYOUT NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
  parentData: <none> (can use size)
  constraints: BoxConstraints(w=438.0, 0.0<=h<=Infinity)
  size: MISSING
  alignment: Alignment.bottomCenter
  textDirection: ltr
  fit: loose
...  child 1: _RenderLayoutBuilder#30fbf relayoutBoundary=up12 NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...    parentData: not positioned; offset=Offset(0.0, 0.0) (can use size)
...    constraints: BoxConstraints(0.0<=w<=438.0, 0.0<=h<=Infinity)
...    size: MISSING
...    child: RenderPositionedBox#2c602 relayoutBoundary=up13 NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...      parentData: offset=Offset(0.0, 0.0) (can use size)
...      constraints: BoxConstraints(0.0<=w<=438.0, 0.0<=h<=Infinity)
...      size: MISSING
...      alignment: Alignment.center
...      textDirection: ltr
...      widthFactor: expand
...      heightFactor: expand
...      child: RenderConstrainedBox#1d9f7 relayoutBoundary=up14 NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...        parentData: offset=Offset(0.0, 0.0) (can use size)
...        constraints: BoxConstraints(0.0<=w<=438.0, 0.0<=h<=Infinity)
...        size: MISSING
...        additionalConstraints: BoxConstraints(w=438.0, h=Infinity)
...        child: RenderAspectRatio#82eee NEEDS-LAYOUT NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...          parentData: <none>
...          constraints: MISSING
...          size: MISSING
...          aspectRatio: 1.8
...  child 2: RenderFlex#47cb0 NEEDS-LAYOUT NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...    parentData: right=10.0; bottom=10.0; left=10.0; offset=Offset(0.0, 0.0)
...    constraints: MISSING
...    size: MISSING
...    direction: horizontal
...    mainAxisAlignment: center
...    mainAxisSize: max
...    crossAxisAlignment: center
...    textDirection: ltr
...    verticalDirection: down
...    child 1: RenderSemanticsAnnotations#7cef6 NEEDS-LAYOUT NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...      parentData: offset=Offset(0.0, 0.0); flex=null; fit=null
...      constraints: MISSING
...      semantic boundary
...      size: MISSING
...      child: _RenderInputPadding#ab8a5 NEEDS-LAYOUT NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...        parentData: <none>
...        constraints: MISSING
...        size: MISSING
...        child: RenderConstrainedBox#3cf07 NEEDS-LAYOUT NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...          parentData: offset=Offset(0.0, 0.0)
...          constraints: MISSING
...          size: MISSING
...          additionalConstraints: BoxConstraints(40.0<=w<=Infinity, 40.0<=h<=Infinity)
...    child 2: RenderConstrainedBox#2c596 NEEDS-LAYOUT NEEDS-PAINT
...      parentData: offset=Offset(0.0, 0.0); flex=null; fit=null
...      constraints: MISSING
...      size: MISSING
...      additionalConstraints: BoxConstraints(w=20.0, 0.0<=h<=Infinity)
...    child 3: RenderSemanticsAnnotations#f8cb5 NEEDS-LAYOUT NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...      parentData: offset=Offset(0.0, 0.0); flex=null; fit=null
...      constraints: MISSING
...      semantic boundary
...      size: MISSING
...      child: _RenderInputPadding#80f6d NEEDS-LAYOUT NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...        parentData: <none>
...        constraints: MISSING
...        size: MISSING
...        child: RenderConstrainedBox#a5878 NEEDS-LAYOUT NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...          parentData: offset=Offset(0.0, 0.0)
...          constraints: MISSING
...          size: MISSING
...          additionalConstraints: BoxConstraints(40.0<=w<=Infinity, 40.0<=h<=Infinity)
====================================================================================================

======== Exception caught by rendering library =====================================================
The following assertion was thrown during performLayout():
RenderBox was not laid out: RenderStack#e1f37 relayoutBoundary=up11 NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
'package:flutter/src/rendering/box.dart':
Failed assertion: line 1965 pos 12: 'hasSize'


Either the assertion indicates an error in the framework itself, or we should provide substantially more information in this error message to help you determine and fix the underlying cause.
In either case, please report this assertion by filing a bug on GitHub:
  https://github.com/flutter/flutter/issues/new?template=2_bug.yml

The relevant error-causing widget was: 
  ClipRRect ClipRRect:file:///F:/real/lib/page/home_page.dart:825:36
When the exception was thrown, this was the stack: 
#2      RenderBox.size (package:flutter/src/rendering/box.dart:1965:12)
#3      RenderProxyBoxMixin.performLayout (package:flutter/src/rendering/proxy_box.dart:104:65)
#4      _RenderCustomClip.performLayout (package:flutter/src/rendering/proxy_box.dart:1431:11)
#5      RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#6      RenderBox.layout (package:flutter/src/rendering/box.dart:2382:11)
#7      ChildLayoutHelper.layoutChild (package:flutter/src/rendering/layout_helper.dart:52:11)
#8      RenderFlex._computeSizes (package:flutter/src/rendering/flex.dart:868:45)
#9      RenderFlex.performLayout (package:flutter/src/rendering/flex.dart:903:32)
#10     RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#11     RenderBox.layout (package:flutter/src/rendering/box.dart:2382:11)
#12     ChildLayoutHelper.layoutChild (package:flutter/src/rendering/layout_helper.dart:52:11)
#13     RenderFlex._computeSizes (package:flutter/src/rendering/flex.dart:808:43)
#14     RenderFlex.performLayout (package:flutter/src/rendering/flex.dart:903:32)
#15     RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#16     RenderBox.layout (package:flutter/src/rendering/box.dart:2382:11)
#17     RenderPadding.performLayout (package:flutter/src/rendering/shifted_box.dart:238:12)
#18     RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#19     RenderBox.layout (package:flutter/src/rendering/box.dart:2382:11)
#20     RenderProxyBoxMixin.performLayout (package:flutter/src/rendering/proxy_box.dart:104:21)
#21     RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#22     RenderBox.layout (package:flutter/src/rendering/box.dart:2382:11)
#23     RenderPadding.performLayout (package:flutter/src/rendering/shifted_box.dart:238:12)
#24     RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#25     RenderBox.layout (package:flutter/src/rendering/box.dart:2382:11)
#26     RenderProxyBoxMixin.performLayout (package:flutter/src/rendering/proxy_box.dart:104:21)
#27     RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#28     RenderBox.layout (package:flutter/src/rendering/box.dart:2382:11)
#29     RenderProxyBoxMixin.performLayout (package:flutter/src/rendering/proxy_box.dart:104:21)
#30     RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#31     RenderBox.layout (package:flutter/src/rendering/box.dart:2382:11)
#32     RenderSliverList.performLayout.advance (package:flutter/src/rendering/sliver_list.dart:251:18)
#33     RenderSliverList.performLayout (package:flutter/src/rendering/sliver_list.dart:283:12)
#34     RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#35     RenderSliverEdgeInsetsPadding.performLayout (package:flutter/src/rendering/sliver_padding.dart:139:12)
#36     RenderSliverPadding.performLayout (package:flutter/src/rendering/sliver_padding.dart:361:11)
#37     RenderObject.layout (package:flutter/src/rendering/object.dart:2493:7)
#38     RenderViewportBase.layoutChildSequence (package:flutter/src/rendering/viewport.dart:534:13)
#39     RenderViewport._attemptLayout (package:flutter/src/rendering/viewport.dart:1512:12)
#40     RenderViewport.performLayout (package:flutter/src/rendering/viewport.dart:1421:20)
#41     RenderObject._layoutWithoutResize (package:flutter/src/rendering/object.dart:2332:7)
#42     PipelineOwner.flushLayout (package:flutter/src/rendering/object.dart:1013:18)
#43     RendererBinding.drawFrame (package:flutter/src/rendering/binding.dart:494:19)
#44     WidgetsBinding.drawFrame (package:flutter/src/widgets/binding.dart:918:13)
#45     RendererBinding._handlePersistentFrameCallback (package:flutter/src/rendering/binding.dart:360:5)
#46     SchedulerBinding._invokeFrameCallback (package:flutter/src/scheduler/binding.dart:1297:15)
#47     SchedulerBinding.handleDrawFrame (package:flutter/src/scheduler/binding.dart:1227:9)
#48     SchedulerBinding._handleDrawFrame (package:flutter/src/scheduler/binding.dart:1085:5)
#49     _invoke (dart:ui/hooks.dart:170:13)
#50     PlatformDispatcher._drawFrame (dart:ui/platform_dispatcher.dart:401:5)
#51     _drawFrame (dart:ui/hooks.dart:140:31)
(elided 2 frames from class _AssertionError)
The following RenderObject was being processed when the exception was fired: RenderClipRRect#c151c relayoutBoundary=up10 NEEDS-LAYOUT NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...  parentData: offset=Offset(0.0, 0.0); flex=1; fit=FlexFit.tight (can use size)
...  constraints: BoxConstraints(w=438.0, 0.0<=h<=Infinity)
...  size: Size(438.0, 36.0)
RenderObject: RenderClipRRect#c151c relayoutBoundary=up10 NEEDS-LAYOUT NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
  parentData: offset=Offset(0.0, 0.0); flex=1; fit=FlexFit.tight (can use size)
  constraints: BoxConstraints(w=438.0, 0.0<=h<=Infinity)
  size: Size(438.0, 36.0)
...  child: RenderStack#e1f37 relayoutBoundary=up11 NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...    parentData: <none> (can use size)
...    constraints: BoxConstraints(w=438.0, 0.0<=h<=Infinity)
...    size: MISSING
...    alignment: Alignment.bottomCenter
...    textDirection: ltr
...    fit: loose
...    child 1: _RenderLayoutBuilder#30fbf relayoutBoundary=up12 NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...      parentData: not positioned; offset=Offset(0.0, 0.0) (can use size)
...      constraints: BoxConstraints(0.0<=w<=438.0, 0.0<=h<=Infinity)
...      size: MISSING
...      child: RenderPositionedBox#2c602 relayoutBoundary=up13 NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...        parentData: offset=Offset(0.0, 0.0) (can use size)
...        constraints: BoxConstraints(0.0<=w<=438.0, 0.0<=h<=Infinity)
...        size: MISSING
...        alignment: Alignment.center
...        textDirection: ltr
...        widthFactor: expand
...        heightFactor: expand
...        child: RenderConstrainedBox#1d9f7 relayoutBoundary=up14 NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...          parentData: offset=Offset(0.0, 0.0) (can use size)
...          constraints: BoxConstraints(0.0<=w<=438.0, 0.0<=h<=Infinity)
...          size: MISSING
...          additionalConstraints: BoxConstraints(w=438.0, h=Infinity)
...    child 2: RenderFlex#47cb0 NEEDS-LAYOUT NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...      parentData: right=10.0; bottom=10.0; left=10.0; offset=Offset(0.0, 0.0)
...      constraints: MISSING
...      size: MISSING
...      direction: horizontal
...      mainAxisAlignment: center
...      mainAxisSize: max
...      crossAxisAlignment: center
...      textDirection: ltr
...      verticalDirection: down
...      child 1: RenderSemanticsAnnotations#7cef6 NEEDS-LAYOUT NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...        parentData: offset=Offset(0.0, 0.0); flex=null; fit=null
...        constraints: MISSING
...        semantic boundary
...        size: MISSING
...        child: _RenderInputPadding#ab8a5 NEEDS-LAYOUT NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...          parentData: <none>
...          constraints: MISSING
...          size: MISSING
...      child 2: RenderConstrainedBox#2c596 NEEDS-LAYOUT NEEDS-PAINT
...        parentData: offset=Offset(0.0, 0.0); flex=null; fit=null
...        constraints: MISSING
...        size: MISSING
...        additionalConstraints: BoxConstraints(w=20.0, 0.0<=h<=Infinity)
...      child 3: RenderSemanticsAnnotations#f8cb5 NEEDS-LAYOUT NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...        parentData: offset=Offset(0.0, 0.0); flex=null; fit=null
...        constraints: MISSING
...        semantic boundary
...        size: MISSING
...        child: _RenderInputPadding#80f6d NEEDS-LAYOUT NEEDS-PAINT NEEDS-COMPOSITING-BITS-UPDATE
...          parentData: <none>
...          constraints: MISSING
...          size: MISSING
