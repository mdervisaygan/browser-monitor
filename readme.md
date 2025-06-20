# WIP

## Browser APIs

<!-- browserapis:start -->
### chrome-stable
  
#### 137.0.7151.119 (`2025-6-17`) 
No browser API changes.

  
#### 137.0.7151.103 (`2025-6-10`) 
No browser API changes.

  
#### 137.0.7151.68 (`2025-6-2`) 
No browser API changes.

  
#### 137.0.7151.55 (`2025-5-27`) ⚡
Added 8 APIs, removed 3 (see: [diff](./browser_apis/chrome-stable_136.0.7103.113_to_137.0.7151.55.diff), [json](./browser_apis/chrome-stable_136.0.7103.113_to_137.0.7151.55.json), [full list](./browser_apis/chrome-stable_137.0.7151.55.json))
 ```diff
--- ./browser_apis/chrome-stable_136.0.7103.113.json	2025-05-27 18:01:41.946330478 +0000
+++ ./browser_apis/chrome-stable_137.0.7151.55.json	2025-05-27 18:02:07.205659919 +0000
@@ -1,10 +1,7 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 8707,
+  "browserApiCount": 8712,
   "browserApis": [
-    "AICreateMonitor",
-    "AICreateMonitor.prototype",
-    "AICreateMonitor.prototype.ondownloadprogress",
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
     "AbsoluteOrientationSensor.prototype.constructor",
@@ -2969,6 +2966,7 @@
     "ImageData.prototype.colorSpace",
     "ImageData.prototype.data",
     "ImageData.prototype.height",
+    "ImageData.prototype.pixelFormat",
     "ImageData.prototype.width",
     "ImageDecoder",
     "ImageDecoder.isTypeSupported",
@@ -6139,12 +6137,14 @@
     "Selection.prototype.collapseToStart",
     "Selection.prototype.containsNode",
     "Selection.prototype.deleteFromDocument",
+    "Selection.prototype.direction",
     "Selection.prototype.empty",
     "Selection.prototype.extend",
     "Selection.prototype.extentNode",
     "Selection.prototype.extentOffset",
     "Selection.prototype.focusNode",
     "Selection.prototype.focusOffset",
+    "Selection.prototype.getComposedRanges",
     "Selection.prototype.getRangeAt",
     "Selection.prototype.isCollapsed",
     "Selection.prototype.modify",
@@ -7142,6 +7142,10 @@
     "WebAssembly.Module.prototype",
     "WebAssembly.RuntimeError",
     "WebAssembly.RuntimeError.prototype",
+    "WebAssembly.SuspendError",
+    "WebAssembly.SuspendError.prototype",
+    "WebAssembly.Suspending",
+    "WebAssembly.Suspending.prototype",
     "WebAssembly.Table",
     "WebAssembly.Table.prototype",
     "WebAssembly.Table.prototype.get",
@@ -7154,6 +7158,7 @@
     "WebAssembly.compileStreaming",
     "WebAssembly.instantiate",
     "WebAssembly.instantiateStreaming",
+    "WebAssembly.promising",
     "WebAssembly.validate",
     "WebGL2RenderingContext",
     "WebGL2RenderingContext.prototype",
```

  
#### 136.0.7103.113 (`2025-5-14`) 
No browser API changes.

  
#### 136.0.7103.92 (`2025-5-6`) 
No browser API changes.

  
#### 136.0.7103.59 (`2025-4-29`) ⚡
Added 14 APIs, removed 0 (see: [diff](./browser_apis/chrome-stable_135.0.7049.114_to_136.0.7103.59.diff), [json](./browser_apis/chrome-stable_135.0.7049.114_to_136.0.7103.59.json), [full list](./browser_apis/chrome-stable_136.0.7103.59.json))
 ```diff
--- ./browser_apis/chrome-stable_135.0.7049.114.json	2025-04-29 19:00:50.345427135 +0000
+++ ./browser_apis/chrome-stable_136.0.7103.59.json	2025-04-29 19:01:11.517358989 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 8693,
+  "browserApiCount": 8707,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -909,6 +909,7 @@
     "CanvasRenderingContext2D.prototype.isContextLost",
     "CanvasRenderingContext2D.prototype.isPointInPath",
     "CanvasRenderingContext2D.prototype.isPointInStroke",
+    "CanvasRenderingContext2D.prototype.lang",
     "CanvasRenderingContext2D.prototype.letterSpacing",
     "CanvasRenderingContext2D.prototype.lineCap",
     "CanvasRenderingContext2D.prototype.lineDashOffset",
@@ -946,7 +947,14 @@
     "CanvasRenderingContext2D.prototype.wordSpacing",
     "CaptureController",
     "CaptureController.prototype",
+    "CaptureController.prototype.decreaseZoomLevel",
+    "CaptureController.prototype.forwardWheel",
+    "CaptureController.prototype.getSupportedZoomLevels",
+    "CaptureController.prototype.increaseZoomLevel",
+    "CaptureController.prototype.onzoomlevelchange",
+    "CaptureController.prototype.resetZoomLevel",
     "CaptureController.prototype.setFocusBehavior",
+    "CaptureController.prototype.zoomLevel",
     "CaretPosition",
     "CaretPosition.prototype",
     "CaretPosition.prototype.getClientRect",
@@ -1635,6 +1643,7 @@
     "GPUAdapterInfo.prototype.architecture",
     "GPUAdapterInfo.prototype.description",
     "GPUAdapterInfo.prototype.device",
+    "GPUAdapterInfo.prototype.isFallbackAdapter",
     "GPUAdapterInfo.prototype.subgroupMaxSize",
     "GPUAdapterInfo.prototype.subgroupMinSize",
     "GPUAdapterInfo.prototype.vendor",
@@ -2883,6 +2892,7 @@
     "IdentityCredential",
     "IdentityCredential.disconnect",
     "IdentityCredential.prototype",
+    "IdentityCredential.prototype.configURL",
     "IdentityCredential.prototype.isAutoSelected",
     "IdentityCredential.prototype.token",
     "IdentityCredentialError",
@@ -4063,6 +4073,7 @@
     "OffscreenCanvasRenderingContext2D.prototype.isContextLost",
     "OffscreenCanvasRenderingContext2D.prototype.isPointInPath",
     "OffscreenCanvasRenderingContext2D.prototype.isPointInStroke",
+    "OffscreenCanvasRenderingContext2D.prototype.lang",
     "OffscreenCanvasRenderingContext2D.prototype.letterSpacing",
     "OffscreenCanvasRenderingContext2D.prototype.lineCap",
     "OffscreenCanvasRenderingContext2D.prototype.lineDashOffset",
@@ -5169,6 +5180,7 @@
     "RegExp.$9",
     "RegExp.$_",
     "RegExp.# WIP

## Browser APIs

",
+    "RegExp.escape",
     "RegExp.input",
     "RegExp.lastMatch",
     "RegExp.lastParen",
@@ -5278,6 +5290,8 @@
     "SVGAElement",
     "SVGAElement.prototype",
     "SVGAElement.prototype.href",
+    "SVGAElement.prototype.rel",
+    "SVGAElement.prototype.relList",
     "SVGAElement.prototype.target",
     "SVGAngle",
     "SVGAngle.prototype",
```

  
#### 135.0.7049.114 (`2025-4-22`) 
No browser API changes.

  
#### 135.0.7049.95 (`2025-4-15`) 
No browser API changes.

  
#### 135.0.7049.84 (`2025-4-8`) 
No browser API changes.

  
#### 135.0.7049.52 (`2025-4-1`) ⚡
Added 86 APIs, removed 3 (see: [diff](./browser_apis/chrome-stable_134.0.6998.165_to_135.0.7049.52.diff), [json](./browser_apis/chrome-stable_134.0.6998.165_to_135.0.7049.52.json), [full list](./browser_apis/chrome-stable_135.0.7049.52.json))
 ```diff
--- ./browser_apis/chrome-stable_134.0.6998.165.json	2025-04-01 17:00:48.549868049 +0000
+++ ./browser_apis/chrome-stable_135.0.7049.52.json	2025-04-01 17:01:10.773133258 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 8610,
+  "browserApiCount": 8693,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -101,6 +101,14 @@
     "ArrayBuffer.prototype.slice",
     "ArrayBuffer.prototype.transfer",
     "ArrayBuffer.prototype.transferToFixedLength",
+    "AsyncDisposableStack",
+    "AsyncDisposableStack.prototype",
+    "AsyncDisposableStack.prototype.adopt",
+    "AsyncDisposableStack.prototype.defer",
+    "AsyncDisposableStack.prototype.disposeAsync",
+    "AsyncDisposableStack.prototype.disposed",
+    "AsyncDisposableStack.prototype.move",
+    "AsyncDisposableStack.prototype.use",
     "Atomics",
     "Atomics.add",
     "Atomics.and",
@@ -983,6 +991,10 @@
     "CloseWatcher.prototype.oncancel",
     "CloseWatcher.prototype.onclose",
     "CloseWatcher.prototype.requestClose",
+    "CommandEvent",
+    "CommandEvent.prototype",
+    "CommandEvent.prototype.command",
+    "CommandEvent.prototype.source",
     "Comment",
     "Comment.prototype",
     "CompositionEvent",
@@ -1182,6 +1194,7 @@
     "DataView.prototype.byteOffset",
     "DataView.prototype.getBigInt64",
     "DataView.prototype.getBigUint64",
+    "DataView.prototype.getFloat16",
     "DataView.prototype.getFloat32",
     "DataView.prototype.getFloat64",
     "DataView.prototype.getInt16",
@@ -1192,6 +1205,7 @@
     "DataView.prototype.getUint8",
     "DataView.prototype.setBigInt64",
     "DataView.prototype.setBigUint64",
+    "DataView.prototype.setFloat16",
     "DataView.prototype.setFloat32",
     "DataView.prototype.setFloat64",
     "DataView.prototype.setInt16",
@@ -1287,6 +1301,14 @@
     "DevicePosture.prototype",
     "DevicePosture.prototype.onchange",
     "DevicePosture.prototype.type",
+    "DisposableStack",
+    "DisposableStack.prototype",
+    "DisposableStack.prototype.adopt",
+    "DisposableStack.prototype.defer",
+    "DisposableStack.prototype.dispose",
+    "DisposableStack.prototype.disposed",
+    "DisposableStack.prototype.move",
+    "DisposableStack.prototype.use",
     "DocumentPictureInPicture",
     "DocumentPictureInPicture.prototype",
     "DocumentPictureInPicture.prototype.onenter",
@@ -1337,6 +1359,7 @@
     "EditContext.prototype.updateText",
     "ElementInternals",
     "ElementInternals.prototype",
+    "ElementInternals.prototype.ariaActiveDescendantElement",
     "ElementInternals.prototype.ariaAtomic",
     "ElementInternals.prototype.ariaAutoComplete",
     "ElementInternals.prototype.ariaBrailleLabel",
@@ -1347,15 +1370,21 @@
     "ElementInternals.prototype.ariaColIndex",
     "ElementInternals.prototype.ariaColIndexText",
     "ElementInternals.prototype.ariaColSpan",
+    "ElementInternals.prototype.ariaControlsElements",
     "ElementInternals.prototype.ariaCurrent",
+    "ElementInternals.prototype.ariaDescribedByElements",
     "ElementInternals.prototype.ariaDescription",
+    "ElementInternals.prototype.ariaDetailsElements",
     "ElementInternals.prototype.ariaDisabled",
+    "ElementInternals.prototype.ariaErrorMessageElements",
     "ElementInternals.prototype.ariaExpanded",
+    "ElementInternals.prototype.ariaFlowToElements",
     "ElementInternals.prototype.ariaHasPopup",
     "ElementInternals.prototype.ariaHidden",
     "ElementInternals.prototype.ariaInvalid",
     "ElementInternals.prototype.ariaKeyShortcuts",
     "ElementInternals.prototype.ariaLabel",
+    "ElementInternals.prototype.ariaLabelledByElements",
     "ElementInternals.prototype.ariaLevel",
     "ElementInternals.prototype.ariaLive",
     "ElementInternals.prototype.ariaModal",
@@ -1465,6 +1494,9 @@
     "FencedFrameConfig",
     "FencedFrameConfig.prototype",
     "FencedFrameConfig.prototype.setSharedStorageContext",
+    "FetchLaterResult",
+    "FetchLaterResult.prototype",
+    "FetchLaterResult.prototype.activated",
     "File",
     "File.prototype",
     "File.prototype.arrayBuffer",
@@ -1533,6 +1565,8 @@
     "FinalizationRegistry.prototype",
     "FinalizationRegistry.prototype.register",
     "FinalizationRegistry.prototype.unregister",
+    "Float16Array",
+    "Float16Array.prototype",
     "Float32Array",
     "Float32Array.prototype",
     "Float64Array",
@@ -1813,7 +1847,6 @@
     "GPUSupportedLimits.prototype.maxComputeWorkgroupsPerDimension",
     "GPUSupportedLimits.prototype.maxDynamicStorageBuffersPerPipelineLayout",
     "GPUSupportedLimits.prototype.maxDynamicUniformBuffersPerPipelineLayout",
-    "GPUSupportedLimits.prototype.maxInterStageShaderComponents",
     "GPUSupportedLimits.prototype.maxInterStageShaderVariables",
     "GPUSupportedLimits.prototype.maxSampledTexturesPerShaderStage",
     "GPUSupportedLimits.prototype.maxSamplersPerShaderStage",
@@ -2038,6 +2071,8 @@
     "HTMLButtonElement",
     "HTMLButtonElement.prototype",
     "HTMLButtonElement.prototype.checkValidity",
+    "HTMLButtonElement.prototype.command",
+    "HTMLButtonElement.prototype.commandForElement",
     "HTMLButtonElement.prototype.disabled",
     "HTMLButtonElement.prototype.form",
     "HTMLButtonElement.prototype.formAction",
@@ -2503,6 +2538,8 @@
     "HTMLSelectElement.prototype.validity",
     "HTMLSelectElement.prototype.value",
     "HTMLSelectElement.prototype.willValidate",
+    "HTMLSelectedContentElement",
+    "HTMLSelectedContentElement.prototype",
     "HTMLSlotElement",
     "HTMLSlotElement.prototype",
     "HTMLSlotElement.prototype.assign",
@@ -3269,6 +3306,7 @@
     "Math.cosh",
     "Math.exp",
     "Math.expm1",
+    "Math.f16round",
     "Math.floor",
     "Math.fround",
     "Math.hypot",
@@ -3313,6 +3351,7 @@
     "MathMLElement.prototype.onchange",
     "MathMLElement.prototype.onclick",
     "MathMLElement.prototype.onclose",
+    "MathMLElement.prototype.oncommand",
     "MathMLElement.prototype.oncontentvisibilityautostatechange",
     "MathMLElement.prototype.oncontextlost",
     "MathMLElement.prototype.oncontextmenu",
@@ -3641,7 +3680,6 @@
     "NavigateEvent",
     "NavigateEvent.prototype",
     "NavigateEvent.prototype.canIntercept",
-    "NavigateEvent.prototype.canTransition",
     "NavigateEvent.prototype.destination",
     "NavigateEvent.prototype.downloadRequest",
     "NavigateEvent.prototype.formData",
@@ -3652,6 +3690,7 @@
     "NavigateEvent.prototype.navigationType",
     "NavigateEvent.prototype.scroll",
     "NavigateEvent.prototype.signal",
+    "NavigateEvent.prototype.sourceElement",
     "NavigateEvent.prototype.userInitiated",
     "Navigation",
     "Navigation.prototype",
@@ -3918,6 +3957,28 @@
     "Object.seal",
     "Object.setPrototypeOf",
     "Object.values",
+    "Observable",
+    "Observable.from",
+    "Observable.prototype",
+    "Observable.prototype.catch",
+    "Observable.prototype.drop",
+    "Observable.prototype.every",
+    "Observable.prototype.filter",
+    "Observable.prototype.finally",
+    "Observable.prototype.find",
+    "Observable.prototype.first",
+    "Observable.prototype.flatMap",
+    "Observable.prototype.forEach",
+    "Observable.prototype.inspect",
+    "Observable.prototype.last",
+    "Observable.prototype.map",
+    "Observable.prototype.reduce",
+    "Observable.prototype.some",
+    "Observable.prototype.subscribe",
+    "Observable.prototype.switchMap",
+    "Observable.prototype.take",
+    "Observable.prototype.takeUntil",
+    "Observable.prototype.toArray",
     "OfflineAudioCompletionEvent",
     "OfflineAudioCompletionEvent.prototype",
     "OfflineAudioCompletionEvent.prototype.renderedBuffer",
@@ -4045,6 +4106,7 @@
     "Option.prototype.constructor.prototype.after",
     "Option.prototype.constructor.prototype.animate",
     "Option.prototype.constructor.prototype.append",
+    "Option.prototype.constructor.prototype.ariaActiveDescendantElement",
     "Option.prototype.constructor.prototype.ariaAtomic",
     "Option.prototype.constructor.prototype.ariaAutoComplete",
     "Option.prototype.constructor.prototype.ariaBrailleLabel",
@@ -4055,15 +4117,21 @@
     "Option.prototype.constructor.prototype.ariaColIndex",
     "Option.prototype.constructor.prototype.ariaColIndexText",
     "Option.prototype.constructor.prototype.ariaColSpan",
+    "Option.prototype.constructor.prototype.ariaControlsElements",
     "Option.prototype.constructor.prototype.ariaCurrent",
+    "Option.prototype.constructor.prototype.ariaDescribedByElements",
     "Option.prototype.constructor.prototype.ariaDescription",
+    "Option.prototype.constructor.prototype.ariaDetailsElements",
     "Option.prototype.constructor.prototype.ariaDisabled",
+    "Option.prototype.constructor.prototype.ariaErrorMessageElements",
     "Option.prototype.constructor.prototype.ariaExpanded",
+    "Option.prototype.constructor.prototype.ariaFlowToElements",
     "Option.prototype.constructor.prototype.ariaHasPopup",
     "Option.prototype.constructor.prototype.ariaHidden",
     "Option.prototype.constructor.prototype.ariaInvalid",
     "Option.prototype.constructor.prototype.ariaKeyShortcuts",
     "Option.prototype.constructor.prototype.ariaLabel",
+    "Option.prototype.constructor.prototype.ariaLabelledByElements",
     "Option.prototype.constructor.prototype.ariaLevel",
     "Option.prototype.constructor.prototype.ariaLive",
     "Option.prototype.constructor.prototype.ariaModal",
@@ -4144,6 +4212,7 @@
     "Option.prototype.constructor.prototype.constructor.prototype.removeEventListener",
     "Option.prototype.constructor.prototype.constructor.prototype.replaceChild",
     "Option.prototype.constructor.prototype.constructor.prototype.textContent",
+    "Option.prototype.constructor.prototype.constructor.prototype.when",
     "Option.prototype.constructor.prototype.contentEditable",
     "Option.prototype.constructor.prototype.currentCSSZoom",
     "Option.prototype.constructor.prototype.dataset",
@@ -4213,6 +4282,7 @@
     "Option.prototype.constructor.prototype.onchange",
     "Option.prototype.constructor.prototype.onclick",
     "Option.prototype.constructor.prototype.onclose",
+    "Option.prototype.constructor.prototype.oncommand",
     "Option.prototype.constructor.prototype.oncontentvisibilityautostatechange",
     "Option.prototype.constructor.prototype.oncontextlost",
     "Option.prototype.constructor.prototype.oncontextmenu",
@@ -5892,6 +5962,7 @@
     "SVGViewElement.prototype.onchange",
     "SVGViewElement.prototype.onclick",
     "SVGViewElement.prototype.onclose",
+    "SVGViewElement.prototype.oncommand",
     "SVGViewElement.prototype.oncontentvisibilityautostatechange",
     "SVGViewElement.prototype.oncontextlost",
     "SVGViewElement.prototype.oncontextmenu",
@@ -6413,6 +6484,14 @@
     "SubmitEvent",
     "SubmitEvent.prototype",
     "SubmitEvent.prototype.submitter",
+    "Subscriber",
+    "Subscriber.prototype",
+    "Subscriber.prototype.active",
+    "Subscriber.prototype.addTeardown",
+    "Subscriber.prototype.complete",
+    "Subscriber.prototype.error",
+    "Subscriber.prototype.next",
+    "Subscriber.prototype.signal",
     "SubtleCrypto",
     "SubtleCrypto.prototype",
     "SubtleCrypto.prototype.decrypt",
@@ -6427,6 +6506,8 @@
     "SubtleCrypto.prototype.unwrapKey",
     "SubtleCrypto.prototype.verify",
     "SubtleCrypto.prototype.wrapKey",
+    "SuppressedError",
+    "SuppressedError.prototype",
     "Symbol",
     "Symbol.for",
     "Symbol.keyFor",
@@ -7802,6 +7883,7 @@
     "XMLDocument.prototype.onchange",
     "XMLDocument.prototype.onclick",
     "XMLDocument.prototype.onclose",
+    "XMLDocument.prototype.oncommand",
     "XMLDocument.prototype.oncontentvisibilityautostatechange",
     "XMLDocument.prototype.oncontextlost",
     "XMLDocument.prototype.oncontextmenu",
@@ -8160,7 +8242,6 @@
     "XRSystem.prototype.isSessionSupported",
     "XRSystem.prototype.ondevicechange",
     "XRSystem.prototype.requestSession",
-    "XRSystem.prototype.supportsSession",
     "XRTransientInputHitTestResult",
     "XRTransientInputHitTestResult.prototype",
     "XRTransientInputHitTestResult.prototype.inputSource",
@@ -8284,6 +8365,7 @@
     "external",
     "fence",
     "fetch",
+    "fetchLater",
     "find",
     "focus",
     "frameElement",
@@ -8332,6 +8414,7 @@
     "onchange",
     "onclick",
     "onclose",
+    "oncommand",
     "oncontentvisibilityautostatechange",
     "oncontextlost",
     "oncontextmenu",
```

  
#### 134.0.6998.165 (`2025-3-21`) 
No browser API changes.

  
#### 134.0.6998.117 (`2025-3-19`) 
No browser API changes.

  
#### 134.0.6998.88 (`2025-3-10`) ⚡
Added 0 APIs, removed 18 (see: [diff](./browser_apis/chrome-stable_134.0.6998.35_to_134.0.6998.88.diff), [json](./browser_apis/chrome-stable_134.0.6998.35_to_134.0.6998.88.json), [full list](./browser_apis/chrome-stable_134.0.6998.88.json))
 ```diff
--- ./browser_apis/chrome-stable_134.0.6998.35.json	2025-03-10 21:00:54.325485187 +0000
+++ ./browser_apis/chrome-stable_134.0.6998.88.json	2025-03-10 21:01:13.620570180 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 8628,
+  "browserApiCount": 8610,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -101,14 +101,6 @@
     "ArrayBuffer.prototype.slice",
     "ArrayBuffer.prototype.transfer",
     "ArrayBuffer.prototype.transferToFixedLength",
-    "AsyncDisposableStack",
-    "AsyncDisposableStack.prototype",
-    "AsyncDisposableStack.prototype.adopt",
-    "AsyncDisposableStack.prototype.defer",
-    "AsyncDisposableStack.prototype.disposeAsync",
-    "AsyncDisposableStack.prototype.disposed",
-    "AsyncDisposableStack.prototype.move",
-    "AsyncDisposableStack.prototype.use",
     "Atomics",
     "Atomics.add",
     "Atomics.and",
@@ -1295,14 +1287,6 @@
     "DevicePosture.prototype",
     "DevicePosture.prototype.onchange",
     "DevicePosture.prototype.type",
-    "DisposableStack",
-    "DisposableStack.prototype",
-    "DisposableStack.prototype.adopt",
-    "DisposableStack.prototype.defer",
-    "DisposableStack.prototype.dispose",
-    "DisposableStack.prototype.disposed",
-    "DisposableStack.prototype.move",
-    "DisposableStack.prototype.use",
     "DocumentPictureInPicture",
     "DocumentPictureInPicture.prototype",
     "DocumentPictureInPicture.prototype.onenter",
@@ -6443,8 +6427,6 @@
     "SubtleCrypto.prototype.unwrapKey",
     "SubtleCrypto.prototype.verify",
     "SubtleCrypto.prototype.wrapKey",
-    "SuppressedError",
-    "SuppressedError.prototype",
     "Symbol",
     "Symbol.for",
     "Symbol.keyFor",
```

  
#### 134.0.6998.35 (`2025-3-4`) ⚡
Added 43 APIs, removed 0 (see: [diff](./browser_apis/chrome-stable_133.0.6943.141_to_134.0.6998.35.diff), [json](./browser_apis/chrome-stable_133.0.6943.141_to_134.0.6998.35.json), [full list](./browser_apis/chrome-stable_134.0.6998.35.json))
 ```diff
--- ./browser_apis/chrome-stable_133.0.6943.141.json	2025-03-04 22:00:54.678954580 +0000
+++ ./browser_apis/chrome-stable_134.0.6998.35.json	2025-03-04 22:01:14.302041265 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 8585,
+  "browserApiCount": 8628,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -101,6 +101,14 @@
     "ArrayBuffer.prototype.slice",
     "ArrayBuffer.prototype.transfer",
     "ArrayBuffer.prototype.transferToFixedLength",
+    "AsyncDisposableStack",
+    "AsyncDisposableStack.prototype",
+    "AsyncDisposableStack.prototype.adopt",
+    "AsyncDisposableStack.prototype.defer",
+    "AsyncDisposableStack.prototype.disposeAsync",
+    "AsyncDisposableStack.prototype.disposed",
+    "AsyncDisposableStack.prototype.move",
+    "AsyncDisposableStack.prototype.use",
     "Atomics",
     "Atomics.add",
     "Atomics.and",
@@ -504,6 +512,15 @@
     "CSSFontFaceRule",
     "CSSFontFaceRule.prototype",
     "CSSFontFaceRule.prototype.style",
+    "CSSFontFeatureValuesRule",
+    "CSSFontFeatureValuesRule.prototype",
+    "CSSFontFeatureValuesRule.prototype.annotation",
+    "CSSFontFeatureValuesRule.prototype.characterVariant",
+    "CSSFontFeatureValuesRule.prototype.fontFamily",
+    "CSSFontFeatureValuesRule.prototype.ornaments",
+    "CSSFontFeatureValuesRule.prototype.styleset",
+    "CSSFontFeatureValuesRule.prototype.stylistic",
+    "CSSFontFeatureValuesRule.prototype.swash",
     "CSSFontPaletteValuesRule",
     "CSSFontPaletteValuesRule.prototype",
     "CSSFontPaletteValuesRule.prototype.basePalette",
@@ -1278,6 +1295,14 @@
     "DevicePosture.prototype",
     "DevicePosture.prototype.onchange",
     "DevicePosture.prototype.type",
+    "DisposableStack",
+    "DisposableStack.prototype",
+    "DisposableStack.prototype.adopt",
+    "DisposableStack.prototype.defer",
+    "DisposableStack.prototype.dispose",
+    "DisposableStack.prototype.disposed",
+    "DisposableStack.prototype.move",
+    "DisposableStack.prototype.use",
     "DocumentPictureInPicture",
     "DocumentPictureInPicture.prototype",
     "DocumentPictureInPicture.prototype.onenter",
@@ -1399,6 +1424,7 @@
     "EncodedVideoChunk.prototype.type",
     "Error",
     "Error.captureStackTrace",
+    "Error.isError",
     "Error.prototype",
     "Error.prototype.toString",
     "ErrorEvent",
@@ -1591,6 +1617,8 @@
     "GPUAdapterInfo.prototype.architecture",
     "GPUAdapterInfo.prototype.description",
     "GPUAdapterInfo.prototype.device",
+    "GPUAdapterInfo.prototype.subgroupMaxSize",
+    "GPUAdapterInfo.prototype.subgroupMinSize",
     "GPUAdapterInfo.prototype.vendor",
     "GPUBindGroup",
     "GPUBindGroup.prototype",
@@ -2069,7 +2097,9 @@
     "HTMLDialogElement",
     "HTMLDialogElement.prototype",
     "HTMLDialogElement.prototype.close",
+    "HTMLDialogElement.prototype.closedBy",
     "HTMLDialogElement.prototype.open",
+    "HTMLDialogElement.prototype.requestClose",
     "HTMLDialogElement.prototype.returnValue",
     "HTMLDialogElement.prototype.show",
     "HTMLDialogElement.prototype.showModal",
@@ -3977,6 +4007,7 @@
     "OffscreenCanvasRenderingContext2D.prototype.fontKerning",
     "OffscreenCanvasRenderingContext2D.prototype.fontStretch",
     "OffscreenCanvasRenderingContext2D.prototype.fontVariantCaps",
+    "OffscreenCanvasRenderingContext2D.prototype.getContextAttributes",
     "OffscreenCanvasRenderingContext2D.prototype.getImageData",
     "OffscreenCanvasRenderingContext2D.prototype.getLineDash",
     "OffscreenCanvasRenderingContext2D.prototype.getTransform",
@@ -6169,6 +6200,7 @@
     "SharedStorage",
     "SharedStorage.prototype",
     "SharedStorage.prototype.append",
+    "SharedStorage.prototype.batchUpdate",
     "SharedStorage.prototype.clear",
     "SharedStorage.prototype.createWorklet",
     "SharedStorage.prototype.delete",
@@ -6177,6 +6209,15 @@
     "SharedStorage.prototype.selectURL",
     "SharedStorage.prototype.set",
     "SharedStorage.prototype.worklet",
+    "SharedStorageAppendMethod",
+    "SharedStorageAppendMethod.prototype",
+    "SharedStorageAppendMethod.prototype.constructor",
+    "SharedStorageClearMethod",
+    "SharedStorageClearMethod.prototype",
+    "SharedStorageDeleteMethod",
+    "SharedStorageDeleteMethod.prototype",
+    "SharedStorageSetMethod",
+    "SharedStorageSetMethod.prototype",
     "SharedStorageWorklet",
     "SharedStorageWorklet.prototype",
     "SharedStorageWorklet.prototype.addModule",
@@ -6402,6 +6443,8 @@
     "SubtleCrypto.prototype.unwrapKey",
     "SubtleCrypto.prototype.verify",
     "SubtleCrypto.prototype.wrapKey",
+    "SuppressedError",
+    "SuppressedError.prototype",
     "Symbol",
     "Symbol.for",
     "Symbol.keyFor",
```

  
#### 133.0.6943.141 (`2025-2-25`) 
No browser API changes.

  
#### 133.0.6943.126 (`2025-2-18`) 
No browser API changes.

  
#### 133.0.6943.98 (`2025-2-12`) 
No browser API changes.

  
#### 133.0.6943.53 (`2025-2-4`) ⚡
Added 36 APIs, removed 7 (see: [diff](./browser_apis/chrome-stable_132.0.6834.159_to_133.0.6943.53.diff), [json](./browser_apis/chrome-stable_132.0.6834.159_to_133.0.6943.53.json), [full list](./browser_apis/chrome-stable_133.0.6943.53.json))
 ```diff
--- ./browser_apis/chrome-stable_132.0.6834.159.json	2025-02-05 01:11:13.881068144 +0000
+++ ./browser_apis/chrome-stable_133.0.6943.53.json	2025-02-05 01:11:34.161258859 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 8556,
+  "browserApiCount": 8585,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -110,6 +110,7 @@
     "Atomics.load",
     "Atomics.notify",
     "Atomics.or",
+    "Atomics.pause",
     "Atomics.store",
     "Atomics.sub",
     "Atomics.wait",
@@ -396,6 +397,20 @@
     "ByteLengthQueuingStrategy.prototype.size",
     "CDATASection",
     "CDATASection.prototype",
+    "CSPViolationReportBody",
+    "CSPViolationReportBody.prototype",
+    "CSPViolationReportBody.prototype.blockedURL",
+    "CSPViolationReportBody.prototype.columnNumber",
+    "CSPViolationReportBody.prototype.disposition",
+    "CSPViolationReportBody.prototype.documentURL",
+    "CSPViolationReportBody.prototype.effectiveDirective",
+    "CSPViolationReportBody.prototype.lineNumber",
+    "CSPViolationReportBody.prototype.originalPolicy",
+    "CSPViolationReportBody.prototype.referrer",
+    "CSPViolationReportBody.prototype.sample",
+    "CSPViolationReportBody.prototype.sourceFile",
+    "CSPViolationReportBody.prototype.statusCode",
+    "CSPViolationReportBody.prototype.toJSON",
     "CSS",
     "CSS.Hz",
     "CSS.Q",
@@ -756,6 +771,7 @@
     "CSSTransition.prototype.oncancel",
     "CSSTransition.prototype.onfinish",
     "CSSTransition.prototype.onremove",
+    "CSSTransition.prototype.overallProgress",
     "CSSTransition.prototype.pause",
     "CSSTransition.prototype.pending",
     "CSSTransition.prototype.persist",
@@ -1272,9 +1288,6 @@
     "DocumentPictureInPictureEvent.prototype.window",
     "DocumentTimeline",
     "DocumentTimeline.prototype",
-    "DocumentTimeline.prototype.constructor",
-    "DocumentTimeline.prototype.currentTime",
-    "DocumentTimeline.prototype.duration",
     "DocumentType",
     "DocumentType.prototype",
     "DocumentType.prototype.after",
@@ -1496,6 +1509,10 @@
     "FileSystemFileHandle.prototype.createWritable",
     "FileSystemFileHandle.prototype.getFile",
     "FileSystemFileHandle.prototype.move",
+    "FileSystemObserver",
+    "FileSystemObserver.prototype",
+    "FileSystemObserver.prototype.disconnect",
+    "FileSystemObserver.prototype.observe",
     "FileSystemWritableFileStream",
     "FileSystemWritableFileStream.prototype",
     "FileSystemWritableFileStream.prototype.mode",
@@ -1947,6 +1964,7 @@
     "HTMLAreaElement",
     "HTMLAreaElement.prototype",
     "HTMLAreaElement.prototype.alt",
+    "HTMLAreaElement.prototype.attributionSrc",
     "HTMLAreaElement.prototype.coords",
     "HTMLAreaElement.prototype.download",
     "HTMLAreaElement.prototype.hash",
@@ -2842,6 +2860,7 @@
     "Image.prototype.alt",
     "Image.prototype.attributionSrc",
     "Image.prototype.border",
+    "Image.prototype.browsingTopics",
     "Image.prototype.complete",
     "Image.prototype.constructor",
     "Image.prototype.crossOrigin",
@@ -4151,6 +4170,7 @@
     "Option.prototype.constructor.prototype.lastElementChild",
     "Option.prototype.constructor.prototype.localName",
     "Option.prototype.constructor.prototype.matches",
+    "Option.prototype.constructor.prototype.moveBefore",
     "Option.prototype.constructor.prototype.namespaceURI",
     "Option.prototype.constructor.prototype.nextElementSibling",
     "Option.prototype.constructor.prototype.nonce",
@@ -4536,6 +4556,7 @@
     "PerformanceResourceTiming.prototype.domainLookupStart",
     "PerformanceResourceTiming.prototype.encodedBodySize",
     "PerformanceResourceTiming.prototype.fetchStart",
+    "PerformanceResourceTiming.prototype.finalResponseHeadersStart",
     "PerformanceResourceTiming.prototype.firstInterimResponseStart",
     "PerformanceResourceTiming.prototype.initiatorType",
     "PerformanceResourceTiming.prototype.nextHopProtocol",
@@ -4743,6 +4764,7 @@
     "Proxy",
     "Proxy.revocable",
     "PublicKeyCredential",
+    "PublicKeyCredential.getClientCapabilities",
     "PublicKeyCredential.isConditionalMediationAvailable",
     "PublicKeyCredential.isUserVerifyingPlatformAuthenticatorAvailable",
     "PublicKeyCredential.parseCreationOptionsFromJSON",
@@ -5093,6 +5115,9 @@
     "RemotePlayback.prototype.prompt",
     "RemotePlayback.prototype.state",
     "RemotePlayback.prototype.watchAvailability",
+    "ReportBody",
+    "ReportBody.prototype",
+    "ReportBody.prototype.toJSON",
     "ReportingObserver",
     "ReportingObserver.prototype",
     "ReportingObserver.prototype.disconnect",
@@ -5988,10 +6013,6 @@
     "ScriptProcessorNode.prototype",
     "ScriptProcessorNode.prototype.bufferSize",
     "ScriptProcessorNode.prototype.onaudioprocess",
-    "ScrollTimeline",
-    "ScrollTimeline.prototype",
-    "ScrollTimeline.prototype.axis",
-    "ScrollTimeline.prototype.source",
     "SecurityPolicyViolationEvent",
     "SecurityPolicyViolationEvent.prototype",
     "SecurityPolicyViolationEvent.prototype.blockedURI",
@@ -6133,6 +6154,7 @@
     "ShadowRoot.prototype.innerHTML",
     "ShadowRoot.prototype.lastElementChild",
     "ShadowRoot.prototype.mode",
+    "ShadowRoot.prototype.moveBefore",
     "ShadowRoot.prototype.onslotchange",
     "ShadowRoot.prototype.pictureInPictureElement",
     "ShadowRoot.prototype.pointerLockElement",
@@ -6872,7 +6894,13 @@
     "VideoPlaybackQuality.prototype.totalVideoFrames",
     "ViewTimeline",
     "ViewTimeline.prototype",
+    "ViewTimeline.prototype.axis",
+    "ViewTimeline.prototype.constructor",
+    "ViewTimeline.prototype.constructor.prototype",
+    "ViewTimeline.prototype.constructor.prototype.currentTime",
+    "ViewTimeline.prototype.constructor.prototype.duration",
     "ViewTimeline.prototype.endOffset",
+    "ViewTimeline.prototype.source",
     "ViewTimeline.prototype.startOffset",
     "ViewTimeline.prototype.subject",
     "ViewTransition",
@@ -7729,6 +7757,7 @@
     "XMLDocument.prototype.lastModified",
     "XMLDocument.prototype.linkColor",
     "XMLDocument.prototype.links",
+    "XMLDocument.prototype.moveBefore",
     "XMLDocument.prototype.onabort",
     "XMLDocument.prototype.onanimationend",
     "XMLDocument.prototype.onanimationiteration",
```

  
#### 132.0.6834.159 (`2025-1-28`) 
No browser API changes.

  
#### 132.0.6834.110 (`2025-1-22`) 
No browser API changes.

  
#### 132.0.6834.83 (`2025-1-14`) ⚡
Added 20 APIs, removed 0 (see: [diff](./browser_apis/chrome-stable_131.0.6778.264_to_132.0.6834.83.diff), [json](./browser_apis/chrome-stable_131.0.6778.264_to_132.0.6834.83.json), [full list](./browser_apis/chrome-stable_132.0.6834.83.json))
 ```diff
--- ./browser_apis/chrome-stable_131.0.6778.264.json	2025-01-15 01:10:17.276958977 +0000
+++ ./browser_apis/chrome-stable_132.0.6834.83.json	2025-01-15 01:10:57.609065180 +0000
@@ -1,7 +1,10 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 8536,
+  "browserApiCount": 8556,
   "browserApis": [
+    "AICreateMonitor",
+    "AICreateMonitor.prototype",
+    "AICreateMonitor.prototype.ondownloadprogress",
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
     "AbsoluteOrientationSensor.prototype.constructor",
@@ -386,6 +389,7 @@
     "BrowserCaptureMediaStreamTrack",
     "BrowserCaptureMediaStreamTrack.prototype",
     "BrowserCaptureMediaStreamTrack.prototype.cropTo",
+    "BrowserCaptureMediaStreamTrack.prototype.restrictTo",
     "ByteLengthQueuingStrategy",
     "ByteLengthQueuingStrategy.prototype",
     "ByteLengthQueuingStrategy.prototype.highWaterMark",
@@ -1254,6 +1258,10 @@
     "DeviceOrientationEvent.prototype.alpha",
     "DeviceOrientationEvent.prototype.beta",
     "DeviceOrientationEvent.prototype.gamma",
+    "DevicePosture",
+    "DevicePosture.prototype",
+    "DevicePosture.prototype.onchange",
+    "DevicePosture.prototype.type",
     "DocumentPictureInPicture",
     "DocumentPictureInPicture.prototype",
     "DocumentPictureInPicture.prototype.onenter",
@@ -1639,6 +1647,7 @@
     "GPUComputePipeline.prototype.label",
     "GPUDevice",
     "GPUDevice.prototype",
+    "GPUDevice.prototype.adapterInfo",
     "GPUDevice.prototype.createBindGroup",
     "GPUDevice.prototype.createBindGroupLayout",
     "GPUDevice.prototype.createBuffer",
@@ -2815,6 +2824,7 @@
     "IdentityProvider.close",
     "IdentityProvider.getUserInfo",
     "IdentityProvider.prototype",
+    "IdentityProvider.resolve",
     "IdleDeadline",
     "IdleDeadline.prototype",
     "IdleDeadline.prototype.didTimeout",
@@ -3683,11 +3693,13 @@
     "Navigator.prototype.deprecatedRunAdAuctionEnforcesKAnonymity",
     "Navigator.prototype.deprecatedURNToURL",
     "Navigator.prototype.deviceMemory",
+    "Navigator.prototype.devicePosture",
     "Navigator.prototype.doNotTrack",
     "Navigator.prototype.geolocation",
     "Navigator.prototype.getBattery",
     "Navigator.prototype.getGamepads",
     "Navigator.prototype.getInstalledRelatedApps",
+    "Navigator.prototype.getInterestGroupAdAuctionData",
     "Navigator.prototype.getUserMedia",
     "Navigator.prototype.gpu",
     "Navigator.prototype.hardwareConcurrency",
@@ -4741,6 +4753,9 @@
     "PublicKeyCredential.prototype.rawId",
     "PublicKeyCredential.prototype.response",
     "PublicKeyCredential.prototype.toJSON",
+    "PublicKeyCredential.signalAllAcceptedCredentials",
+    "PublicKeyCredential.signalCurrentUserDetails",
+    "PublicKeyCredential.signalUnknownCredential",
     "PushManager",
     "PushManager.prototype",
     "PushManager.prototype.getSubscription",
@@ -5089,6 +5104,7 @@
     "Request.prototype.blob",
     "Request.prototype.body",
     "Request.prototype.bodyUsed",
+    "Request.prototype.bytes",
     "Request.prototype.cache",
     "Request.prototype.clone",
     "Request.prototype.credentials",
@@ -5133,6 +5149,7 @@
     "Response.prototype.blob",
     "Response.prototype.body",
     "Response.prototype.bodyUsed",
+    "Response.prototype.bytes",
     "Response.prototype.clone",
     "Response.prototype.formData",
     "Response.prototype.headers",
@@ -5145,6 +5162,9 @@
     "Response.prototype.type",
     "Response.prototype.url",
     "Response.redirect",
+    "RestrictionTarget",
+    "RestrictionTarget.fromElement",
+    "RestrictionTarget.prototype",
     "SVGAElement",
     "SVGAElement.prototype",
     "SVGAElement.prototype.href",
```

  
#### 131.0.6778.264 (`2025-1-7`) 
No browser API changes.

  
#### 131.0.6778.204 (`2024-12-18`) 
No browser API changes.

  
#### 131.0.6778.139 (`2024-12-10`) 
No browser API changes.

  
#### 131.0.6778.108 (`2024-12-3`) 
No browser API changes.

  
#### 131.0.6778.85 (`2024-11-19`) 
No browser API changes.

  
#### 131.0.6778.69 (`2024-11-12`) ⚡
Added 24 APIs, removed 5 (see: [diff](./browser_apis/chrome-stable_130.0.6723.116_to_131.0.6778.69.diff), [json](./browser_apis/chrome-stable_130.0.6723.116_to_131.0.6778.69.json), [full list](./browser_apis/chrome-stable_131.0.6778.69.json))
 ```diff
--- ./browser_apis/chrome-stable_130.0.6723.116.json	2024-11-13 01:11:00.980981093 +0000
+++ ./browser_apis/chrome-stable_131.0.6778.69.json	2024-11-13 01:11:33.945230359 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 8517,
+  "browserApiCount": 8536,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -521,6 +521,10 @@
     "CSSLayerStatementRule",
     "CSSLayerStatementRule.prototype",
     "CSSLayerStatementRule.prototype.nameList",
+    "CSSMarginRule",
+    "CSSMarginRule.prototype",
+    "CSSMarginRule.prototype.name",
+    "CSSMarginRule.prototype.style",
     "CSSMathClamp",
     "CSSMathClamp.prototype",
     "CSSMathClamp.prototype.lower",
@@ -581,14 +585,12 @@
     "CSSPositionTryDescriptors.prototype.inline-size",
     "CSSPositionTryDescriptors.prototype.inlineSize",
     "CSSPositionTryDescriptors.prototype.inset",
-    "CSSPositionTryDescriptors.prototype.inset-area",
     "CSSPositionTryDescriptors.prototype.inset-block",
     "CSSPositionTryDescriptors.prototype.inset-block-end",
     "CSSPositionTryDescriptors.prototype.inset-block-start",
     "CSSPositionTryDescriptors.prototype.inset-inline",
     "CSSPositionTryDescriptors.prototype.inset-inline-end",
     "CSSPositionTryDescriptors.prototype.inset-inline-start",
-    "CSSPositionTryDescriptors.prototype.insetArea",
     "CSSPositionTryDescriptors.prototype.insetBlock",
     "CSSPositionTryDescriptors.prototype.insetBlockEnd",
     "CSSPositionTryDescriptors.prototype.insetBlockStart",
@@ -1558,7 +1560,6 @@
     "GPUAdapter.prototype.info",
     "GPUAdapter.prototype.isFallbackAdapter",
     "GPUAdapter.prototype.limits",
-    "GPUAdapter.prototype.requestAdapterInfo",
     "GPUAdapter.prototype.requestDevice",
     "GPUAdapterInfo",
     "GPUAdapterInfo.prototype",
@@ -1587,6 +1588,7 @@
     "GPUCanvasContext.prototype",
     "GPUCanvasContext.prototype.canvas",
     "GPUCanvasContext.prototype.configure",
+    "GPUCanvasContext.prototype.getConfiguration",
     "GPUCanvasContext.prototype.getCurrentTexture",
     "GPUCanvasContext.prototype.unconfigure",
     "GPUColorWrite",
@@ -4118,7 +4120,6 @@
     "Option.prototype.constructor.prototype.getElementsByTagName",
     "Option.prototype.constructor.prototype.getElementsByTagNameNS",
     "Option.prototype.constructor.prototype.getHTML",
-    "Option.prototype.constructor.prototype.getInnerHTML",
     "Option.prototype.constructor.prototype.hasAttribute",
     "Option.prototype.constructor.prototype.hasAttributeNS",
     "Option.prototype.constructor.prototype.hasAttributes",
@@ -5092,6 +5093,7 @@
     "Request.prototype.clone",
     "Request.prototype.credentials",
     "Request.prototype.destination",
+    "Request.prototype.duplex",
     "Request.prototype.formData",
     "Request.prototype.headers",
     "Request.prototype.integrity",
@@ -6106,7 +6108,6 @@
     "ShadowRoot.prototype.getAnimations",
     "ShadowRoot.prototype.getElementById",
     "ShadowRoot.prototype.getHTML",
-    "ShadowRoot.prototype.getInnerHTML",
     "ShadowRoot.prototype.getSelection",
     "ShadowRoot.prototype.host",
     "ShadowRoot.prototype.innerHTML",
@@ -7959,14 +7960,25 @@
     "XRFrame",
     "XRFrame.prototype",
     "XRFrame.prototype.createAnchor",
+    "XRFrame.prototype.fillJointRadii",
+    "XRFrame.prototype.fillPoses",
     "XRFrame.prototype.getDepthInformation",
     "XRFrame.prototype.getHitTestResults",
     "XRFrame.prototype.getHitTestResultsForTransientInput",
+    "XRFrame.prototype.getJointPose",
     "XRFrame.prototype.getLightEstimate",
     "XRFrame.prototype.getPose",
     "XRFrame.prototype.getViewerPose",
     "XRFrame.prototype.session",
     "XRFrame.prototype.trackedAnchors",
+    "XRHand",
+    "XRHand.prototype",
+    "XRHand.prototype.entries",
+    "XRHand.prototype.forEach",
+    "XRHand.prototype.get",
+    "XRHand.prototype.keys",
+    "XRHand.prototype.size",
+    "XRHand.prototype.values",
     "XRHitTestResult",
     "XRHitTestResult.prototype",
     "XRHitTestResult.prototype.createAnchor",
@@ -7978,6 +7990,7 @@
     "XRInputSource.prototype",
     "XRInputSource.prototype.gamepad",
     "XRInputSource.prototype.gripSpace",
+    "XRInputSource.prototype.hand",
     "XRInputSource.prototype.handedness",
     "XRInputSource.prototype.profiles",
     "XRInputSource.prototype.targetRayMode",
@@ -7994,6 +8007,12 @@
     "XRInputSourcesChangeEvent.prototype.added",
     "XRInputSourcesChangeEvent.prototype.removed",
     "XRInputSourcesChangeEvent.prototype.session",
+    "XRJointPose",
+    "XRJointPose.prototype",
+    "XRJointPose.prototype.radius",
+    "XRJointSpace",
+    "XRJointSpace.prototype",
+    "XRJointSpace.prototype.jointName",
     "XRLayer",
     "XRLayer.prototype",
     "XRLightEstimate",
```

  
#### 130.0.6723.116 (`2024-11-5`) 
No browser API changes.

  
#### 130.0.6723.91 (`2024-10-29`) 
No browser API changes.

  
### chrome-unstable
  
#### 139.0.7246.0 (`2025-6-20`) ⚡
Added 3 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_139.0.7232.3_to_139.0.7246.0.diff), [json](./browser_apis/chrome-unstable_139.0.7232.3_to_139.0.7246.0.json), [full list](./browser_apis/chrome-unstable_139.0.7246.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_139.0.7232.3.json	2025-06-20 08:00:47.221967071 +0000
+++ ./browser_apis/chrome-unstable_139.0.7246.0.json	2025-06-20 08:01:32.631061693 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8786,
+  "browserApiCount": 8789,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -6368,6 +6368,8 @@
     "SpeechGrammarList.prototype.item",
     "SpeechGrammarList.prototype.length",
     "SpeechRecognition",
+    "SpeechRecognition.available",
+    "SpeechRecognition.install",
     "SpeechRecognition.prototype",
     "SpeechRecognition.prototype.abort",
     "SpeechRecognition.prototype.continuous",
@@ -6386,6 +6388,7 @@
     "SpeechRecognition.prototype.onspeechend",
     "SpeechRecognition.prototype.onspeechstart",
     "SpeechRecognition.prototype.onstart",
+    "SpeechRecognition.prototype.processLocally",
     "SpeechRecognition.prototype.start",
     "SpeechRecognition.prototype.stop",
     "SpeechRecognitionErrorEvent",
```

  
#### 139.0.7232.3 (`2025-6-12`) ⚡
Added 72 APIs, removed 39 (see: [diff](./browser_apis/chrome-unstable_139.0.7219.3_to_139.0.7232.3.diff), [json](./browser_apis/chrome-unstable_139.0.7219.3_to_139.0.7232.3.json), [full list](./browser_apis/chrome-unstable_139.0.7232.3.json))
 ```diff
--- ./browser_apis/chrome-unstable_139.0.7219.3.json	2025-06-12 17:01:18.967946345 +0000
+++ ./browser_apis/chrome-unstable_139.0.7232.3.json	2025-06-12 17:01:43.480876809 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8753,
+  "browserApiCount": 8786,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -6357,6 +6357,45 @@
     "SourceBufferList.prototype.length",
     "SourceBufferList.prototype.onaddsourcebuffer",
     "SourceBufferList.prototype.onremovesourcebuffer",
+    "SpeechGrammar",
+    "SpeechGrammar.prototype",
+    "SpeechGrammar.prototype.src",
+    "SpeechGrammar.prototype.weight",
+    "SpeechGrammarList",
+    "SpeechGrammarList.prototype",
+    "SpeechGrammarList.prototype.addFromString",
+    "SpeechGrammarList.prototype.addFromUri",
+    "SpeechGrammarList.prototype.item",
+    "SpeechGrammarList.prototype.length",
+    "SpeechRecognition",
+    "SpeechRecognition.prototype",
+    "SpeechRecognition.prototype.abort",
+    "SpeechRecognition.prototype.continuous",
+    "SpeechRecognition.prototype.grammars",
+    "SpeechRecognition.prototype.interimResults",
+    "SpeechRecognition.prototype.lang",
+    "SpeechRecognition.prototype.maxAlternatives",
+    "SpeechRecognition.prototype.onaudioend",
+    "SpeechRecognition.prototype.onaudiostart",
+    "SpeechRecognition.prototype.onend",
+    "SpeechRecognition.prototype.onerror",
+    "SpeechRecognition.prototype.onnomatch",
+    "SpeechRecognition.prototype.onresult",
+    "SpeechRecognition.prototype.onsoundend",
+    "SpeechRecognition.prototype.onsoundstart",
+    "SpeechRecognition.prototype.onspeechend",
+    "SpeechRecognition.prototype.onspeechstart",
+    "SpeechRecognition.prototype.onstart",
+    "SpeechRecognition.prototype.start",
+    "SpeechRecognition.prototype.stop",
+    "SpeechRecognitionErrorEvent",
+    "SpeechRecognitionErrorEvent.prototype",
+    "SpeechRecognitionErrorEvent.prototype.error",
+    "SpeechRecognitionErrorEvent.prototype.message",
+    "SpeechRecognitionEvent",
+    "SpeechRecognitionEvent.prototype",
+    "SpeechRecognitionEvent.prototype.resultIndex",
+    "SpeechRecognitionEvent.prototype.results",
     "SpeechSynthesis",
     "SpeechSynthesis.prototype",
     "SpeechSynthesis.prototype.cancel",
@@ -6555,6 +6594,22 @@
     "SubtleCrypto.prototype.unwrapKey",
     "SubtleCrypto.prototype.verify",
     "SubtleCrypto.prototype.wrapKey",
+    "Summarizer",
+    "Summarizer.availability",
+    "Summarizer.create",
+    "Summarizer.prototype",
+    "Summarizer.prototype.destroy",
+    "Summarizer.prototype.expectedContextLanguages",
+    "Summarizer.prototype.expectedInputLanguages",
+    "Summarizer.prototype.format",
+    "Summarizer.prototype.inputQuota",
+    "Summarizer.prototype.length",
+    "Summarizer.prototype.measureInputUsage",
+    "Summarizer.prototype.outputLanguage",
+    "Summarizer.prototype.sharedContext",
+    "Summarizer.prototype.summarize",
+    "Summarizer.prototype.summarizeStreaming",
+    "Summarizer.prototype.type",
     "SuppressedError",
     "SuppressedError.prototype",
     "Symbol",
@@ -6750,6 +6805,17 @@
     "TransitionEvent.prototype.elapsedTime",
     "TransitionEvent.prototype.propertyName",
     "TransitionEvent.prototype.pseudoElement",
+    "Translator",
+    "Translator.availability",
+    "Translator.create",
+    "Translator.prototype",
+    "Translator.prototype.destroy",
+    "Translator.prototype.inputQuota",
+    "Translator.prototype.measureInputUsage",
+    "Translator.prototype.sourceLanguage",
+    "Translator.prototype.targetLanguage",
+    "Translator.prototype.translate",
+    "Translator.prototype.translateStreaming",
     "TreeWalker",
     "TreeWalker.prototype",
     "TreeWalker.prototype.currentNode",
@@ -8163,7 +8229,9 @@
     "XRCPUDepthInformation.prototype.getDepthInMeters",
     "XRCPUDepthInformation.prototype.height",
     "XRCPUDepthInformation.prototype.normDepthBufferFromNormView",
+    "XRCPUDepthInformation.prototype.projectionMatrix",
     "XRCPUDepthInformation.prototype.rawValueToMeters",
+    "XRCPUDepthInformation.prototype.transform",
     "XRCPUDepthInformation.prototype.width",
     "XRCamera",
     "XRCamera.prototype",
@@ -8267,7 +8335,9 @@
     "XRSession",
     "XRSession.prototype",
     "XRSession.prototype.cancelAnimationFrame",
+    "XRSession.prototype.depthActive",
     "XRSession.prototype.depthDataFormat",
+    "XRSession.prototype.depthType",
     "XRSession.prototype.depthUsage",
     "XRSession.prototype.domOverlayState",
     "XRSession.prototype.enabledFeatures",
@@ -8284,6 +8354,7 @@
     "XRSession.prototype.onsqueezeend",
     "XRSession.prototype.onsqueezestart",
     "XRSession.prototype.onvisibilitychange",
+    "XRSession.prototype.pauseDepthSensing",
     "XRSession.prototype.preferredReflectionFormat",
     "XRSession.prototype.renderState",
     "XRSession.prototype.requestAnimationFrame",
@@ -8291,6 +8362,7 @@
     "XRSession.prototype.requestHitTestSourceForTransientInput",
     "XRSession.prototype.requestLightProbe",
     "XRSession.prototype.requestReferenceSpace",
+    "XRSession.prototype.resumeDepthSensing",
     "XRSession.prototype.updateRenderState",
     "XRSession.prototype.visibilityState",
     "XRSessionEvent",
@@ -8695,45 +8767,6 @@
     "webkitRequestAnimationFrame",
     "webkitRequestFileSystem",
     "webkitResolveLocalFileSystemURL",
-    "webkitSpeechGrammar",
-    "webkitSpeechGrammar.prototype",
-    "webkitSpeechGrammar.prototype.src",
-    "webkitSpeechGrammar.prototype.weight",
-    "webkitSpeechGrammarList",
-    "webkitSpeechGrammarList.prototype",
-    "webkitSpeechGrammarList.prototype.addFromString",
-    "webkitSpeechGrammarList.prototype.addFromUri",
-    "webkitSpeechGrammarList.prototype.item",
-    "webkitSpeechGrammarList.prototype.length",
-    "webkitSpeechRecognition",
-    "webkitSpeechRecognition.prototype",
-    "webkitSpeechRecognition.prototype.abort",
-    "webkitSpeechRecognition.prototype.continuous",
-    "webkitSpeechRecognition.prototype.grammars",
-    "webkitSpeechRecognition.prototype.interimResults",
-    "webkitSpeechRecognition.prototype.lang",
-    "webkitSpeechRecognition.prototype.maxAlternatives",
-    "webkitSpeechRecognition.prototype.onaudioend",
-    "webkitSpeechRecognition.prototype.onaudiostart",
-    "webkitSpeechRecognition.prototype.onend",
-    "webkitSpeechRecognition.prototype.onerror",
-    "webkitSpeechRecognition.prototype.onnomatch",
-    "webkitSpeechRecognition.prototype.onresult",
-    "webkitSpeechRecognition.prototype.onsoundend",
-    "webkitSpeechRecognition.prototype.onsoundstart",
-    "webkitSpeechRecognition.prototype.onspeechend",
-    "webkitSpeechRecognition.prototype.onspeechstart",
-    "webkitSpeechRecognition.prototype.onstart",
-    "webkitSpeechRecognition.prototype.start",
-    "webkitSpeechRecognition.prototype.stop",
-    "webkitSpeechRecognitionError",
-    "webkitSpeechRecognitionError.prototype",
-    "webkitSpeechRecognitionError.prototype.error",
-    "webkitSpeechRecognitionError.prototype.message",
-    "webkitSpeechRecognitionEvent",
-    "webkitSpeechRecognitionEvent.prototype",
-    "webkitSpeechRecognitionEvent.prototype.resultIndex",
-    "webkitSpeechRecognitionEvent.prototype.results",
     "webkitURL",
     "webkitURL.canParse",
     "webkitURL.createObjectURL",
```

  
#### 139.0.7219.3 (`2025-6-5`) ⚡
Added 11 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_139.0.7207.2_to_139.0.7219.3.diff), [json](./browser_apis/chrome-unstable_139.0.7207.2_to_139.0.7219.3.json), [full list](./browser_apis/chrome-unstable_139.0.7219.3.json))
 ```diff
--- ./browser_apis/chrome-unstable_139.0.7207.2.json	2025-06-06 00:02:40.325521745 +0000
+++ ./browser_apis/chrome-unstable_139.0.7219.3.json	2025-06-06 00:03:12.741833406 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8742,
+  "browserApiCount": 8753,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -524,6 +524,17 @@
     "CSSFontPaletteValuesRule.prototype.fontFamily",
     "CSSFontPaletteValuesRule.prototype.name",
     "CSSFontPaletteValuesRule.prototype.overrideColors",
+    "CSSFunctionDeclarations",
+    "CSSFunctionDeclarations.prototype",
+    "CSSFunctionDeclarations.prototype.style",
+    "CSSFunctionDescriptors",
+    "CSSFunctionDescriptors.prototype",
+    "CSSFunctionDescriptors.prototype.result",
+    "CSSFunctionRule",
+    "CSSFunctionRule.prototype",
+    "CSSFunctionRule.prototype.getParameters",
+    "CSSFunctionRule.prototype.name",
+    "CSSFunctionRule.prototype.returnType",
     "CSSImageValue",
     "CSSImageValue.prototype",
     "CSSImportRule",
```

  
#### 139.0.7207.2 (`2025-5-30`) ⚡
Added 5 APIs, removed 1 (see: [diff](./browser_apis/chrome-unstable_138.0.7191.0_to_139.0.7207.2.diff), [json](./browser_apis/chrome-unstable_138.0.7191.0_to_139.0.7207.2.json), [full list](./browser_apis/chrome-unstable_139.0.7207.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_138.0.7191.0.json	2025-05-30 17:01:05.731014161 +0000
+++ ./browser_apis/chrome-unstable_139.0.7207.2.json	2025-05-30 17:01:31.719206442 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8738,
+  "browserApiCount": 8742,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -1996,6 +1996,7 @@
     "HTMLAnchorElement.prototype.host",
     "HTMLAnchorElement.prototype.hostname",
     "HTMLAnchorElement.prototype.href",
+    "HTMLAnchorElement.prototype.hrefTranslate",
     "HTMLAnchorElement.prototype.hreflang",
     "HTMLAnchorElement.prototype.name",
     "HTMLAnchorElement.prototype.origin",
@@ -4910,6 +4911,10 @@
     "PushSubscriptionOptions.prototype",
     "PushSubscriptionOptions.prototype.applicationServerKey",
     "PushSubscriptionOptions.prototype.userVisibleOnly",
+    "QuotaExceededError",
+    "QuotaExceededError.prototype",
+    "QuotaExceededError.prototype.quota",
+    "QuotaExceededError.prototype.requested",
     "RTCCertificate",
     "RTCCertificate.prototype",
     "RTCCertificate.prototype.expires",
@@ -5262,7 +5267,6 @@
     "Request.prototype.referrer",
     "Request.prototype.referrerPolicy",
     "Request.prototype.signal",
-    "Request.prototype.targetAddressSpace",
     "Request.prototype.text",
     "Request.prototype.url",
     "ResizeObserver",
```

  
#### 138.0.7191.0 (`2025-5-22`) ⚡
Added 17 APIs, removed 5 (see: [diff](./browser_apis/chrome-unstable_138.0.7180.2_to_138.0.7191.0.diff), [json](./browser_apis/chrome-unstable_138.0.7180.2_to_138.0.7191.0.json), [full list](./browser_apis/chrome-unstable_138.0.7191.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_138.0.7180.2.json	2025-05-22 17:00:48.010498484 +0000
+++ ./browser_apis/chrome-unstable_138.0.7191.0.json	2025-05-22 17:01:13.979909644 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8726,
+  "browserApiCount": 8738,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -759,14 +759,9 @@
     "CSSSupportsRule.prototype.conditionText",
     "CSSSupportsRule.prototype.constructor",
     "CSSSupportsRule.prototype.constructor.prototype",
-    "CSSSupportsRule.prototype.constructor.prototype.constructor",
     "CSSSupportsRule.prototype.constructor.prototype.cssRules",
-    "CSSSupportsRule.prototype.constructor.prototype.cssText",
     "CSSSupportsRule.prototype.constructor.prototype.deleteRule",
     "CSSSupportsRule.prototype.constructor.prototype.insertRule",
-    "CSSSupportsRule.prototype.constructor.prototype.parentRule",
-    "CSSSupportsRule.prototype.constructor.prototype.parentStyleSheet",
-    "CSSSupportsRule.prototype.constructor.prototype.type",
     "CSSTransformValue",
     "CSSTransformValue.prototype",
     "CSSTransformValue.prototype.is2D",
@@ -839,7 +834,12 @@
     "CSSVariableReferenceValue.prototype.variable",
     "CSSViewTransitionRule",
     "CSSViewTransitionRule.prototype",
+    "CSSViewTransitionRule.prototype.constructor",
+    "CSSViewTransitionRule.prototype.cssText",
     "CSSViewTransitionRule.prototype.navigation",
+    "CSSViewTransitionRule.prototype.parentRule",
+    "CSSViewTransitionRule.prototype.parentStyleSheet",
+    "CSSViewTransitionRule.prototype.type",
     "CSSViewTransitionRule.prototype.types",
     "Cache",
     "Cache.prototype",
@@ -1040,6 +1040,9 @@
     "CountQueuingStrategy.prototype",
     "CountQueuingStrategy.prototype.highWaterMark",
     "CountQueuingStrategy.prototype.size",
+    "CreateMonitor",
+    "CreateMonitor.prototype",
+    "CreateMonitor.prototype.ondownloadprogress",
     "Credential",
     "Credential.prototype",
     "Credential.prototype.id",
@@ -3204,6 +3207,15 @@
     "KeyframeEffect.prototype.setKeyframes",
     "KeyframeEffect.prototype.target",
     "KeyframeEffect.prototype.updateTiming",
+    "LanguageDetector",
+    "LanguageDetector.availability",
+    "LanguageDetector.create",
+    "LanguageDetector.prototype",
+    "LanguageDetector.prototype.destroy",
+    "LanguageDetector.prototype.detect",
+    "LanguageDetector.prototype.expectedInputLanguages",
+    "LanguageDetector.prototype.inputQuota",
+    "LanguageDetector.prototype.measureInputUsage",
     "LargestContentfulPaint",
     "LargestContentfulPaint.prototype",
     "LargestContentfulPaint.prototype.element",
```

  
#### 138.0.7180.2 (`2025-5-16`) ⚡
Added 12 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_138.0.7166.2_to_138.0.7180.2.diff), [json](./browser_apis/chrome-unstable_138.0.7166.2_to_138.0.7180.2.json), [full list](./browser_apis/chrome-unstable_138.0.7180.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_138.0.7166.2.json	2025-05-16 20:00:55.425793783 +0000
+++ ./browser_apis/chrome-unstable_138.0.7180.2.json	2025-05-16 20:02:04.209267936 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8714,
+  "browserApiCount": 8726,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -3018,6 +3018,13 @@
     "Int32Array.prototype",
     "Int8Array",
     "Int8Array.prototype",
+    "IntegrityViolationReportBody",
+    "IntegrityViolationReportBody.prototype",
+    "IntegrityViolationReportBody.prototype.blockedURL",
+    "IntegrityViolationReportBody.prototype.destination",
+    "IntegrityViolationReportBody.prototype.documentURL",
+    "IntegrityViolationReportBody.prototype.reportOnly",
+    "IntegrityViolationReportBody.prototype.toJSON",
     "IntersectionObserver",
     "IntersectionObserver.prototype",
     "IntersectionObserver.prototype.delay",
@@ -3950,6 +3957,7 @@
     "Object.prototype.__defineGetter__.arguments",
     "Object.prototype.__defineGetter__.bind",
     "Object.prototype.__defineGetter__.call",
+    "Object.prototype.__defineGetter__.caller",
     "Object.prototype.__defineGetter__.constructor",
     "Object.prototype.__defineGetter__.toString",
     "Object.prototype.__defineSetter__",
@@ -7043,6 +7051,9 @@
     "ViewTransitionTypeSet.prototype.keys",
     "ViewTransitionTypeSet.prototype.size",
     "ViewTransitionTypeSet.prototype.values",
+    "Viewport",
+    "Viewport.prototype",
+    "Viewport.prototype.segments",
     "VirtualKeyboard",
     "VirtualKeyboard.prototype",
     "VirtualKeyboard.prototype.boundingRect",
@@ -8588,6 +8599,7 @@
     "top",
     "trustedTypes",
     "unescape",
+    "viewport",
     "visualViewport",
     "webkitCancelAnimationFrame",
     "webkitMediaStream",
```

  
#### 138.0.7166.2 (`2025-5-8`) ⚡
Added 2 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_138.0.7153.0_to_138.0.7166.2.diff), [json](./browser_apis/chrome-unstable_138.0.7153.0_to_138.0.7166.2.json), [full list](./browser_apis/chrome-unstable_138.0.7166.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_138.0.7153.0.json	2025-05-08 19:00:47.190317401 +0000
+++ ./browser_apis/chrome-unstable_138.0.7166.2.json	2025-05-08 19:01:49.201089121 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8712,
+  "browserApiCount": 8714,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -7003,7 +7003,9 @@
     "VideoFrame.prototype.displayHeight",
     "VideoFrame.prototype.displayWidth",
     "VideoFrame.prototype.duration",
+    "VideoFrame.prototype.flip",
     "VideoFrame.prototype.format",
+    "VideoFrame.prototype.rotation",
     "VideoFrame.prototype.timestamp",
     "VideoFrame.prototype.visibleRect",
     "VideoPlaybackQuality",
```

  
#### 138.0.7153.0 (`2025-5-2`) ⚡
Added 0 APIs, removed 2 (see: [diff](./browser_apis/chrome-unstable_137.0.7141.3_to_138.0.7153.0.diff), [json](./browser_apis/chrome-unstable_137.0.7141.3_to_138.0.7153.0.json), [full list](./browser_apis/chrome-unstable_138.0.7153.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_137.0.7141.3.json	2025-05-02 17:00:48.812851333 +0000
+++ ./browser_apis/chrome-unstable_138.0.7153.0.json	2025-05-02 17:01:10.891932901 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8714,
+  "browserApiCount": 8712,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -7003,9 +7003,7 @@
     "VideoFrame.prototype.displayHeight",
     "VideoFrame.prototype.displayWidth",
     "VideoFrame.prototype.duration",
-    "VideoFrame.prototype.flip",
     "VideoFrame.prototype.format",
-    "VideoFrame.prototype.rotation",
     "VideoFrame.prototype.timestamp",
     "VideoFrame.prototype.visibleRect",
     "VideoPlaybackQuality",
```

  
#### 137.0.7141.3 (`2025-4-24`) ⚡
Added 6 APIs, removed 3 (see: [diff](./browser_apis/chrome-unstable_137.0.7127.2_to_137.0.7141.3.diff), [json](./browser_apis/chrome-unstable_137.0.7127.2_to_137.0.7141.3.json), [full list](./browser_apis/chrome-unstable_137.0.7141.3.json))
 ```diff
--- ./browser_apis/chrome-unstable_137.0.7127.2.json	2025-04-24 18:01:02.474216514 +0000
+++ ./browser_apis/chrome-unstable_137.0.7141.3.json	2025-04-24 18:01:26.956610333 +0000
@@ -1,10 +1,7 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8711,
+  "browserApiCount": 8714,
   "browserApis": [
-    "AICreateMonitor",
-    "AICreateMonitor.prototype",
-    "AICreateMonitor.prototype.ondownloadprogress",
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
     "AbsoluteOrientationSensor.prototype.constructor",
@@ -2969,6 +2966,7 @@
     "ImageData.prototype.colorSpace",
     "ImageData.prototype.data",
     "ImageData.prototype.height",
+    "ImageData.prototype.pixelFormat",
     "ImageData.prototype.width",
     "ImageDecoder",
     "ImageDecoder.isTypeSupported",
@@ -7146,6 +7144,10 @@
     "WebAssembly.Module.prototype",
     "WebAssembly.RuntimeError",
     "WebAssembly.RuntimeError.prototype",
+    "WebAssembly.SuspendError",
+    "WebAssembly.SuspendError.prototype",
+    "WebAssembly.Suspending",
+    "WebAssembly.Suspending.prototype",
     "WebAssembly.Table",
     "WebAssembly.Table.prototype",
     "WebAssembly.Table.prototype.get",
@@ -7158,6 +7160,7 @@
     "WebAssembly.compileStreaming",
     "WebAssembly.instantiate",
     "WebAssembly.instantiateStreaming",
+    "WebAssembly.promising",
     "WebAssembly.validate",
     "WebGL2RenderingContext",
     "WebGL2RenderingContext.prototype",
```

  
#### 137.0.7127.2 (`2025-4-17`) ⚡
Added 2 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_137.0.7117.2_to_137.0.7127.2.diff), [json](./browser_apis/chrome-unstable_137.0.7117.2_to_137.0.7127.2.json), [full list](./browser_apis/chrome-unstable_137.0.7127.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_137.0.7117.2.json	2025-04-17 20:00:51.591322713 +0000
+++ ./browser_apis/chrome-unstable_137.0.7127.2.json	2025-04-17 20:01:19.146306795 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8709,
+  "browserApiCount": 8711,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -7005,7 +7005,9 @@
     "VideoFrame.prototype.displayHeight",
     "VideoFrame.prototype.displayWidth",
     "VideoFrame.prototype.duration",
+    "VideoFrame.prototype.flip",
     "VideoFrame.prototype.format",
+    "VideoFrame.prototype.rotation",
     "VideoFrame.prototype.timestamp",
     "VideoFrame.prototype.visibleRect",
     "VideoPlaybackQuality",
```

  
#### 137.0.7117.2 (`2025-4-10`) 
No browser API changes.

  
#### 137.0.7106.2 (`2025-4-4`) ⚡
Added 4 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_136.0.7091.2_to_137.0.7106.2.diff), [json](./browser_apis/chrome-unstable_136.0.7091.2_to_137.0.7106.2.json), [full list](./browser_apis/chrome-unstable_137.0.7106.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_136.0.7091.2.json	2025-04-04 19:00:48.444736096 +0000
+++ ./browser_apis/chrome-unstable_137.0.7106.2.json	2025-04-04 19:01:44.111806527 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8705,
+  "browserApiCount": 8709,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -1643,6 +1643,7 @@
     "GPUAdapterInfo.prototype.architecture",
     "GPUAdapterInfo.prototype.description",
     "GPUAdapterInfo.prototype.device",
+    "GPUAdapterInfo.prototype.isFallbackAdapter",
     "GPUAdapterInfo.prototype.subgroupMaxSize",
     "GPUAdapterInfo.prototype.subgroupMinSize",
     "GPUAdapterInfo.prototype.vendor",
@@ -2891,6 +2892,7 @@
     "IdentityCredential",
     "IdentityCredential.disconnect",
     "IdentityCredential.prototype",
+    "IdentityCredential.prototype.configURL",
     "IdentityCredential.prototype.isAutoSelected",
     "IdentityCredential.prototype.token",
     "IdentityCredentialError",
@@ -6137,12 +6139,14 @@
     "Selection.prototype.collapseToStart",
     "Selection.prototype.containsNode",
     "Selection.prototype.deleteFromDocument",
+    "Selection.prototype.direction",
     "Selection.prototype.empty",
     "Selection.prototype.extend",
     "Selection.prototype.extentNode",
     "Selection.prototype.extentOffset",
     "Selection.prototype.focusNode",
     "Selection.prototype.focusOffset",
+    "Selection.prototype.getComposedRanges",
     "Selection.prototype.getRangeAt",
     "Selection.prototype.isCollapsed",
     "Selection.prototype.modify",
```

  
#### 136.0.7091.2 (`2025-3-27`) ⚡
Added 7 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_136.0.7081.2_to_136.0.7091.2.diff), [json](./browser_apis/chrome-unstable_136.0.7081.2_to_136.0.7091.2.json), [full list](./browser_apis/chrome-unstable_136.0.7091.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_136.0.7081.2.json	2025-03-27 19:00:44.056460207 +0000
+++ ./browser_apis/chrome-unstable_136.0.7091.2.json	2025-03-27 19:01:09.071587763 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8698,
+  "browserApiCount": 8705,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -947,7 +947,14 @@
     "CanvasRenderingContext2D.prototype.wordSpacing",
     "CaptureController",
     "CaptureController.prototype",
+    "CaptureController.prototype.decreaseZoomLevel",
+    "CaptureController.prototype.forwardWheel",
+    "CaptureController.prototype.getSupportedZoomLevels",
+    "CaptureController.prototype.increaseZoomLevel",
+    "CaptureController.prototype.onzoomlevelchange",
+    "CaptureController.prototype.resetZoomLevel",
     "CaptureController.prototype.setFocusBehavior",
+    "CaptureController.prototype.zoomLevel",
     "CaretPosition",
     "CaretPosition.prototype",
     "CaretPosition.prototype.getClientRect",
```

  
#### 136.0.7081.2 (`2025-3-24`) ⚡
Added 2 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_136.0.7064.0_to_136.0.7081.2.diff), [json](./browser_apis/chrome-unstable_136.0.7064.0_to_136.0.7081.2.json), [full list](./browser_apis/chrome-unstable_136.0.7081.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_136.0.7064.0.json	2025-03-24 19:00:44.910849414 +0000
+++ ./browser_apis/chrome-unstable_136.0.7081.2.json	2025-03-24 19:01:35.605827719 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8696,
+  "browserApiCount": 8698,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -909,6 +909,7 @@
     "CanvasRenderingContext2D.prototype.isContextLost",
     "CanvasRenderingContext2D.prototype.isPointInPath",
     "CanvasRenderingContext2D.prototype.isPointInStroke",
+    "CanvasRenderingContext2D.prototype.lang",
     "CanvasRenderingContext2D.prototype.letterSpacing",
     "CanvasRenderingContext2D.prototype.lineCap",
     "CanvasRenderingContext2D.prototype.lineDashOffset",
@@ -4063,6 +4064,7 @@
     "OffscreenCanvasRenderingContext2D.prototype.isContextLost",
     "OffscreenCanvasRenderingContext2D.prototype.isPointInPath",
     "OffscreenCanvasRenderingContext2D.prototype.isPointInStroke",
+    "OffscreenCanvasRenderingContext2D.prototype.lang",
     "OffscreenCanvasRenderingContext2D.prototype.letterSpacing",
     "OffscreenCanvasRenderingContext2D.prototype.lineCap",
     "OffscreenCanvasRenderingContext2D.prototype.lineDashOffset",
```

  
#### 136.0.7064.0 (`2025-3-13`) ⚡
Added 31 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_136.0.7052.2_to_136.0.7064.0.diff), [json](./browser_apis/chrome-unstable_136.0.7052.2_to_136.0.7064.0.json), [full list](./browser_apis/chrome-unstable_136.0.7064.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_136.0.7052.2.json	2025-03-13 20:00:51.079360284 +0000
+++ ./browser_apis/chrome-unstable_136.0.7064.0.json	2025-03-13 20:02:04.150540970 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8665,
+  "browserApiCount": 8696,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -3957,6 +3957,28 @@
     "Object.seal",
     "Object.setPrototypeOf",
     "Object.values",
+    "Observable",
+    "Observable.from",
+    "Observable.prototype",
+    "Observable.prototype.catch",
+    "Observable.prototype.drop",
+    "Observable.prototype.every",
+    "Observable.prototype.filter",
+    "Observable.prototype.finally",
+    "Observable.prototype.find",
+    "Observable.prototype.first",
+    "Observable.prototype.flatMap",
+    "Observable.prototype.forEach",
+    "Observable.prototype.inspect",
+    "Observable.prototype.last",
+    "Observable.prototype.map",
+    "Observable.prototype.reduce",
+    "Observable.prototype.some",
+    "Observable.prototype.subscribe",
+    "Observable.prototype.switchMap",
+    "Observable.prototype.take",
+    "Observable.prototype.takeUntil",
+    "Observable.prototype.toArray",
     "OfflineAudioCompletionEvent",
     "OfflineAudioCompletionEvent.prototype",
     "OfflineAudioCompletionEvent.prototype.renderedBuffer",
@@ -4190,6 +4212,7 @@
     "Option.prototype.constructor.prototype.constructor.prototype.removeEventListener",
     "Option.prototype.constructor.prototype.constructor.prototype.replaceChild",
     "Option.prototype.constructor.prototype.constructor.prototype.textContent",
+    "Option.prototype.constructor.prototype.constructor.prototype.when",
     "Option.prototype.constructor.prototype.contentEditable",
     "Option.prototype.constructor.prototype.currentCSSZoom",
     "Option.prototype.constructor.prototype.dataset",
@@ -6464,6 +6487,14 @@
     "SubmitEvent",
     "SubmitEvent.prototype",
     "SubmitEvent.prototype.submitter",
+    "Subscriber",
+    "Subscriber.prototype",
+    "Subscriber.prototype.active",
+    "Subscriber.prototype.addTeardown",
+    "Subscriber.prototype.complete",
+    "Subscriber.prototype.error",
+    "Subscriber.prototype.next",
+    "Subscriber.prototype.signal",
     "SubtleCrypto",
     "SubtleCrypto.prototype",
     "SubtleCrypto.prototype.decrypt",
```

  
#### 136.0.7052.2 (`2025-3-7`) ⚡
Added 14 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_135.0.7039.0_to_136.0.7052.2.diff), [json](./browser_apis/chrome-unstable_135.0.7039.0_to_136.0.7052.2.json), [full list](./browser_apis/chrome-unstable_136.0.7052.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_135.0.7039.0.json	2025-03-07 19:01:06.989857607 +0000
+++ ./browser_apis/chrome-unstable_136.0.7052.2.json	2025-03-07 19:01:36.354983558 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8651,
+  "browserApiCount": 8665,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -991,6 +991,10 @@
     "CloseWatcher.prototype.oncancel",
     "CloseWatcher.prototype.onclose",
     "CloseWatcher.prototype.requestClose",
+    "CommandEvent",
+    "CommandEvent.prototype",
+    "CommandEvent.prototype.command",
+    "CommandEvent.prototype.source",
     "Comment",
     "Comment.prototype",
     "CompositionEvent",
@@ -2067,6 +2071,8 @@
     "HTMLButtonElement",
     "HTMLButtonElement.prototype",
     "HTMLButtonElement.prototype.checkValidity",
+    "HTMLButtonElement.prototype.command",
+    "HTMLButtonElement.prototype.commandForElement",
     "HTMLButtonElement.prototype.disabled",
     "HTMLButtonElement.prototype.form",
     "HTMLButtonElement.prototype.formAction",
@@ -3345,6 +3351,7 @@
     "MathMLElement.prototype.onchange",
     "MathMLElement.prototype.onclick",
     "MathMLElement.prototype.onclose",
+    "MathMLElement.prototype.oncommand",
     "MathMLElement.prototype.oncontentvisibilityautostatechange",
     "MathMLElement.prototype.oncontextlost",
     "MathMLElement.prototype.oncontextmenu",
@@ -4252,6 +4259,7 @@
     "Option.prototype.constructor.prototype.onchange",
     "Option.prototype.constructor.prototype.onclick",
     "Option.prototype.constructor.prototype.onclose",
+    "Option.prototype.constructor.prototype.oncommand",
     "Option.prototype.constructor.prototype.oncontentvisibilityautostatechange",
     "Option.prototype.constructor.prototype.oncontextlost",
     "Option.prototype.constructor.prototype.oncontextmenu",
@@ -5138,6 +5146,7 @@
     "RegExp.$9",
     "RegExp.$_",
     "RegExp.# WIP

## Browser APIs

",
+    "RegExp.escape",
     "RegExp.input",
     "RegExp.lastMatch",
     "RegExp.lastParen",
@@ -5247,6 +5256,8 @@
     "SVGAElement",
     "SVGAElement.prototype",
     "SVGAElement.prototype.href",
+    "SVGAElement.prototype.rel",
+    "SVGAElement.prototype.relList",
     "SVGAElement.prototype.target",
     "SVGAngle",
     "SVGAngle.prototype",
@@ -5931,6 +5942,7 @@
     "SVGViewElement.prototype.onchange",
     "SVGViewElement.prototype.onclick",
     "SVGViewElement.prototype.onclose",
+    "SVGViewElement.prototype.oncommand",
     "SVGViewElement.prototype.oncontentvisibilityautostatechange",
     "SVGViewElement.prototype.oncontextlost",
     "SVGViewElement.prototype.oncontextmenu",
@@ -7843,6 +7855,7 @@
     "XMLDocument.prototype.onchange",
     "XMLDocument.prototype.onclick",
     "XMLDocument.prototype.onclose",
+    "XMLDocument.prototype.oncommand",
     "XMLDocument.prototype.oncontentvisibilityautostatechange",
     "XMLDocument.prototype.oncontextlost",
     "XMLDocument.prototype.oncontextmenu",
@@ -8373,6 +8386,7 @@
     "onchange",
     "onclick",
     "onclose",
+    "oncommand",
     "oncontentvisibilityautostatechange",
     "oncontextlost",
     "oncontextmenu",
```

  
#### 135.0.7039.0 (`2025-3-3`) ⚡
Added 9 APIs, removed 2 (see: [diff](./browser_apis/chrome-unstable_135.0.7023.0_to_135.0.7039.0.diff), [json](./browser_apis/chrome-unstable_135.0.7023.0_to_135.0.7039.0.json), [full list](./browser_apis/chrome-unstable_135.0.7039.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_135.0.7023.0.json	2025-03-03 23:00:54.880970520 +0000
+++ ./browser_apis/chrome-unstable_135.0.7039.0.json	2025-03-03 23:01:32.824662655 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8644,
+  "browserApiCount": 8651,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -1190,6 +1190,7 @@
     "DataView.prototype.byteOffset",
     "DataView.prototype.getBigInt64",
     "DataView.prototype.getBigUint64",
+    "DataView.prototype.getFloat16",
     "DataView.prototype.getFloat32",
     "DataView.prototype.getFloat64",
     "DataView.prototype.getInt16",
@@ -1200,6 +1201,7 @@
     "DataView.prototype.getUint8",
     "DataView.prototype.setBigInt64",
     "DataView.prototype.setBigUint64",
+    "DataView.prototype.setFloat16",
     "DataView.prototype.setFloat32",
     "DataView.prototype.setFloat64",
     "DataView.prototype.setInt16",
@@ -1488,6 +1490,9 @@
     "FencedFrameConfig",
     "FencedFrameConfig.prototype",
     "FencedFrameConfig.prototype.setSharedStorageContext",
+    "FetchLaterResult",
+    "FetchLaterResult.prototype",
+    "FetchLaterResult.prototype.activated",
     "File",
     "File.prototype",
     "File.prototype.arrayBuffer",
@@ -1556,6 +1561,8 @@
     "FinalizationRegistry.prototype",
     "FinalizationRegistry.prototype.register",
     "FinalizationRegistry.prototype.unregister",
+    "Float16Array",
+    "Float16Array.prototype",
     "Float32Array",
     "Float32Array.prototype",
     "Float64Array",
@@ -3293,6 +3300,7 @@
     "Math.cosh",
     "Math.exp",
     "Math.expm1",
+    "Math.f16round",
     "Math.floor",
     "Math.fround",
     "Math.hypot",
@@ -3665,7 +3673,6 @@
     "NavigateEvent",
     "NavigateEvent.prototype",
     "NavigateEvent.prototype.canIntercept",
-    "NavigateEvent.prototype.canTransition",
     "NavigateEvent.prototype.destination",
     "NavigateEvent.prototype.downloadRequest",
     "NavigateEvent.prototype.formData",
@@ -8194,7 +8201,6 @@
     "XRSystem.prototype.isSessionSupported",
     "XRSystem.prototype.ondevicechange",
     "XRSystem.prototype.requestSession",
-    "XRSystem.prototype.supportsSession",
     "XRTransientInputHitTestResult",
     "XRTransientInputHitTestResult.prototype",
     "XRTransientInputHitTestResult.prototype.inputSource",
@@ -8318,6 +8324,7 @@
     "external",
     "fence",
     "fetch",
+    "fetchLater",
     "find",
     "focus",
     "frameElement",
```

  
#### 135.0.7023.0 (`2025-2-20`) ⚡
Added 17 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_135.0.7012.4_to_135.0.7023.0.diff), [json](./browser_apis/chrome-unstable_135.0.7012.4_to_135.0.7023.0.json), [full list](./browser_apis/chrome-unstable_135.0.7023.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_135.0.7012.4.json	2025-02-20 22:01:17.454891600 +0000
+++ ./browser_apis/chrome-unstable_135.0.7023.0.json	2025-02-20 22:02:27.630590846 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8627,
+  "browserApiCount": 8644,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -1353,6 +1353,7 @@
     "EditContext.prototype.updateText",
     "ElementInternals",
     "ElementInternals.prototype",
+    "ElementInternals.prototype.ariaActiveDescendantElement",
     "ElementInternals.prototype.ariaAtomic",
     "ElementInternals.prototype.ariaAutoComplete",
     "ElementInternals.prototype.ariaBrailleLabel",
@@ -1363,15 +1364,21 @@
     "ElementInternals.prototype.ariaColIndex",
     "ElementInternals.prototype.ariaColIndexText",
     "ElementInternals.prototype.ariaColSpan",
+    "ElementInternals.prototype.ariaControlsElements",
     "ElementInternals.prototype.ariaCurrent",
+    "ElementInternals.prototype.ariaDescribedByElements",
     "ElementInternals.prototype.ariaDescription",
+    "ElementInternals.prototype.ariaDetailsElements",
     "ElementInternals.prototype.ariaDisabled",
+    "ElementInternals.prototype.ariaErrorMessageElements",
     "ElementInternals.prototype.ariaExpanded",
+    "ElementInternals.prototype.ariaFlowToElements",
     "ElementInternals.prototype.ariaHasPopup",
     "ElementInternals.prototype.ariaHidden",
     "ElementInternals.prototype.ariaInvalid",
     "ElementInternals.prototype.ariaKeyShortcuts",
     "ElementInternals.prototype.ariaLabel",
+    "ElementInternals.prototype.ariaLabelledByElements",
     "ElementInternals.prototype.ariaLevel",
     "ElementInternals.prototype.ariaLive",
     "ElementInternals.prototype.ariaModal",
@@ -2518,6 +2525,8 @@
     "HTMLSelectElement.prototype.validity",
     "HTMLSelectElement.prototype.value",
     "HTMLSelectElement.prototype.willValidate",
+    "HTMLSelectedContentElement",
+    "HTMLSelectedContentElement.prototype",
     "HTMLSlotElement",
     "HTMLSlotElement.prototype",
     "HTMLSlotElement.prototype.assign",
@@ -3667,6 +3676,7 @@
     "NavigateEvent.prototype.navigationType",
     "NavigateEvent.prototype.scroll",
     "NavigateEvent.prototype.signal",
+    "NavigateEvent.prototype.sourceElement",
     "NavigateEvent.prototype.userInitiated",
     "Navigation",
     "Navigation.prototype",
@@ -4060,6 +4070,7 @@
     "Option.prototype.constructor.prototype.after",
     "Option.prototype.constructor.prototype.animate",
     "Option.prototype.constructor.prototype.append",
+    "Option.prototype.constructor.prototype.ariaActiveDescendantElement",
     "Option.prototype.constructor.prototype.ariaAtomic",
     "Option.prototype.constructor.prototype.ariaAutoComplete",
     "Option.prototype.constructor.prototype.ariaBrailleLabel",
@@ -4070,15 +4081,21 @@
     "Option.prototype.constructor.prototype.ariaColIndex",
     "Option.prototype.constructor.prototype.ariaColIndexText",
     "Option.prototype.constructor.prototype.ariaColSpan",
+    "Option.prototype.constructor.prototype.ariaControlsElements",
     "Option.prototype.constructor.prototype.ariaCurrent",
+    "Option.prototype.constructor.prototype.ariaDescribedByElements",
     "Option.prototype.constructor.prototype.ariaDescription",
+    "Option.prototype.constructor.prototype.ariaDetailsElements",
     "Option.prototype.constructor.prototype.ariaDisabled",
+    "Option.prototype.constructor.prototype.ariaErrorMessageElements",
     "Option.prototype.constructor.prototype.ariaExpanded",
+    "Option.prototype.constructor.prototype.ariaFlowToElements",
     "Option.prototype.constructor.prototype.ariaHasPopup",
     "Option.prototype.constructor.prototype.ariaHidden",
     "Option.prototype.constructor.prototype.ariaInvalid",
     "Option.prototype.constructor.prototype.ariaKeyShortcuts",
     "Option.prototype.constructor.prototype.ariaLabel",
+    "Option.prototype.constructor.prototype.ariaLabelledByElements",
     "Option.prototype.constructor.prototype.ariaLevel",
     "Option.prototype.constructor.prototype.ariaLive",
     "Option.prototype.constructor.prototype.ariaModal",
```

  
#### 135.0.7012.4 (`2025-2-13`) ⚡
Added 0 APIs, removed 1 (see: [diff](./browser_apis/chrome-unstable_135.0.6999.2_to_135.0.7012.4.diff), [json](./browser_apis/chrome-unstable_135.0.6999.2_to_135.0.7012.4.json), [full list](./browser_apis/chrome-unstable_135.0.7012.4.json))
 ```diff
--- ./browser_apis/chrome-unstable_135.0.6999.2.json	2025-02-14 01:11:23.576987714 +0000
+++ ./browser_apis/chrome-unstable_135.0.7012.4.json	2025-02-14 01:11:44.536787841 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8628,
+  "browserApiCount": 8627,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -1829,7 +1829,6 @@
     "GPUSupportedLimits.prototype.maxComputeWorkgroupsPerDimension",
     "GPUSupportedLimits.prototype.maxDynamicStorageBuffersPerPipelineLayout",
     "GPUSupportedLimits.prototype.maxDynamicUniformBuffersPerPipelineLayout",
-    "GPUSupportedLimits.prototype.maxInterStageShaderComponents",
     "GPUSupportedLimits.prototype.maxInterStageShaderVariables",
     "GPUSupportedLimits.prototype.maxSampledTexturesPerShaderStage",
     "GPUSupportedLimits.prototype.maxSamplersPerShaderStage",
```

  
#### 135.0.6999.2 (`2025-2-6`) 
No browser API changes.

  
#### 134.0.6988.2 (`2025-1-31`) ⚡
Added 13 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_134.0.6974.3_to_134.0.6988.2.diff), [json](./browser_apis/chrome-unstable_134.0.6974.3_to_134.0.6988.2.json), [full list](./browser_apis/chrome-unstable_134.0.6988.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_134.0.6974.3.json	2025-02-01 01:14:00.170095101 +0000
+++ ./browser_apis/chrome-unstable_134.0.6988.2.json	2025-02-01 01:14:35.730521471 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8615,
+  "browserApiCount": 8628,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -2097,7 +2097,9 @@
     "HTMLDialogElement",
     "HTMLDialogElement.prototype",
     "HTMLDialogElement.prototype.close",
+    "HTMLDialogElement.prototype.closedBy",
     "HTMLDialogElement.prototype.open",
+    "HTMLDialogElement.prototype.requestClose",
     "HTMLDialogElement.prototype.returnValue",
     "HTMLDialogElement.prototype.show",
     "HTMLDialogElement.prototype.showModal",
@@ -4005,6 +4007,7 @@
     "OffscreenCanvasRenderingContext2D.prototype.fontKerning",
     "OffscreenCanvasRenderingContext2D.prototype.fontStretch",
     "OffscreenCanvasRenderingContext2D.prototype.fontVariantCaps",
+    "OffscreenCanvasRenderingContext2D.prototype.getContextAttributes",
     "OffscreenCanvasRenderingContext2D.prototype.getImageData",
     "OffscreenCanvasRenderingContext2D.prototype.getLineDash",
     "OffscreenCanvasRenderingContext2D.prototype.getTransform",
@@ -6197,6 +6200,7 @@
     "SharedStorage",
     "SharedStorage.prototype",
     "SharedStorage.prototype.append",
+    "SharedStorage.prototype.batchUpdate",
     "SharedStorage.prototype.clear",
     "SharedStorage.prototype.createWorklet",
     "SharedStorage.prototype.delete",
@@ -6205,6 +6209,15 @@
     "SharedStorage.prototype.selectURL",
     "SharedStorage.prototype.set",
     "SharedStorage.prototype.worklet",
+    "SharedStorageAppendMethod",
+    "SharedStorageAppendMethod.prototype",
+    "SharedStorageAppendMethod.prototype.constructor",
+    "SharedStorageClearMethod",
+    "SharedStorageClearMethod.prototype",
+    "SharedStorageDeleteMethod",
+    "SharedStorageDeleteMethod.prototype",
+    "SharedStorageSetMethod",
+    "SharedStorageSetMethod.prototype",
     "SharedStorageWorklet",
     "SharedStorageWorklet.prototype",
     "SharedStorageWorklet.prototype.addModule",
```

  
#### 134.0.6974.3 (`2025-1-24`) ⚡
Added 11 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_134.0.6958.2_to_134.0.6974.3.diff), [json](./browser_apis/chrome-unstable_134.0.6958.2_to_134.0.6974.3.json), [full list](./browser_apis/chrome-unstable_134.0.6974.3.json))
 ```diff
--- ./browser_apis/chrome-unstable_134.0.6958.2.json	2025-01-25 01:06:31.095530173 +0000
+++ ./browser_apis/chrome-unstable_134.0.6974.3.json	2025-01-25 01:07:06.543253723 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8604,
+  "browserApiCount": 8615,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -512,6 +512,15 @@
     "CSSFontFaceRule",
     "CSSFontFaceRule.prototype",
     "CSSFontFaceRule.prototype.style",
+    "CSSFontFeatureValuesRule",
+    "CSSFontFeatureValuesRule.prototype",
+    "CSSFontFeatureValuesRule.prototype.annotation",
+    "CSSFontFeatureValuesRule.prototype.characterVariant",
+    "CSSFontFeatureValuesRule.prototype.fontFamily",
+    "CSSFontFeatureValuesRule.prototype.ornaments",
+    "CSSFontFeatureValuesRule.prototype.styleset",
+    "CSSFontFeatureValuesRule.prototype.stylistic",
+    "CSSFontFeatureValuesRule.prototype.swash",
     "CSSFontPaletteValuesRule",
     "CSSFontPaletteValuesRule.prototype",
     "CSSFontPaletteValuesRule.prototype.basePalette",
@@ -1608,6 +1617,8 @@
     "GPUAdapterInfo.prototype.architecture",
     "GPUAdapterInfo.prototype.description",
     "GPUAdapterInfo.prototype.device",
+    "GPUAdapterInfo.prototype.subgroupMaxSize",
+    "GPUAdapterInfo.prototype.subgroupMinSize",
     "GPUAdapterInfo.prototype.vendor",
     "GPUBindGroup",
     "GPUBindGroup.prototype",
```

  
#### 134.0.6958.2 (`2025-1-16`) ⚡
Added 23 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_133.0.6943.6_to_134.0.6958.2.diff), [json](./browser_apis/chrome-unstable_133.0.6943.6_to_134.0.6958.2.json), [full list](./browser_apis/chrome-unstable_134.0.6958.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_133.0.6943.6.json	2025-01-17 01:09:33.253330925 +0000
+++ ./browser_apis/chrome-unstable_134.0.6958.2.json	2025-01-17 01:10:43.062095356 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8581,
+  "browserApiCount": 8604,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -101,6 +101,14 @@
     "ArrayBuffer.prototype.slice",
     "ArrayBuffer.prototype.transfer",
     "ArrayBuffer.prototype.transferToFixedLength",
+    "AsyncDisposableStack",
+    "AsyncDisposableStack.prototype",
+    "AsyncDisposableStack.prototype.adopt",
+    "AsyncDisposableStack.prototype.defer",
+    "AsyncDisposableStack.prototype.disposeAsync",
+    "AsyncDisposableStack.prototype.disposed",
+    "AsyncDisposableStack.prototype.move",
+    "AsyncDisposableStack.prototype.use",
     "Atomics",
     "Atomics.add",
     "Atomics.and",
@@ -1278,6 +1286,14 @@
     "DevicePosture.prototype",
     "DevicePosture.prototype.onchange",
     "DevicePosture.prototype.type",
+    "DisposableStack",
+    "DisposableStack.prototype",
+    "DisposableStack.prototype.adopt",
+    "DisposableStack.prototype.defer",
+    "DisposableStack.prototype.dispose",
+    "DisposableStack.prototype.disposed",
+    "DisposableStack.prototype.move",
+    "DisposableStack.prototype.use",
     "DocumentPictureInPicture",
     "DocumentPictureInPicture.prototype",
     "DocumentPictureInPicture.prototype.onenter",
@@ -1399,6 +1415,7 @@
     "EncodedVideoChunk.prototype.type",
     "Error",
     "Error.captureStackTrace",
+    "Error.isError",
     "Error.prototype",
     "Error.prototype.toString",
     "ErrorEvent",
@@ -1509,6 +1526,10 @@
     "FileSystemFileHandle.prototype.createWritable",
     "FileSystemFileHandle.prototype.getFile",
     "FileSystemFileHandle.prototype.move",
+    "FileSystemObserver",
+    "FileSystemObserver.prototype",
+    "FileSystemObserver.prototype.disconnect",
+    "FileSystemObserver.prototype.observe",
     "FileSystemWritableFileStream",
     "FileSystemWritableFileStream.prototype",
     "FileSystemWritableFileStream.prototype.mode",
@@ -6398,6 +6419,8 @@
     "SubtleCrypto.prototype.unwrapKey",
     "SubtleCrypto.prototype.verify",
     "SubtleCrypto.prototype.wrapKey",
+    "SuppressedError",
+    "SuppressedError.prototype",
     "Symbol",
     "Symbol.for",
     "Symbol.keyFor",
```

  
#### 133.0.6943.6 (`2025-1-9`) ⚡
Added 4 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_133.0.6905.0_to_133.0.6943.6.diff), [json](./browser_apis/chrome-unstable_133.0.6905.0_to_133.0.6943.6.json), [full list](./browser_apis/chrome-unstable_133.0.6943.6.json))
 ```diff
--- ./browser_apis/chrome-unstable_133.0.6905.0.json	2025-01-10 01:13:38.007431384 +0000
+++ ./browser_apis/chrome-unstable_133.0.6943.6.json	2025-01-10 01:14:05.067539804 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8577,
+  "browserApiCount": 8581,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -2856,6 +2856,7 @@
     "Image.prototype.alt",
     "Image.prototype.attributionSrc",
     "Image.prototype.border",
+    "Image.prototype.browsingTopics",
     "Image.prototype.complete",
     "Image.prototype.constructor",
     "Image.prototype.crossOrigin",
@@ -4165,6 +4166,7 @@
     "Option.prototype.constructor.prototype.lastElementChild",
     "Option.prototype.constructor.prototype.localName",
     "Option.prototype.constructor.prototype.matches",
+    "Option.prototype.constructor.prototype.moveBefore",
     "Option.prototype.constructor.prototype.namespaceURI",
     "Option.prototype.constructor.prototype.nextElementSibling",
     "Option.prototype.constructor.prototype.nonce",
@@ -6148,6 +6150,7 @@
     "ShadowRoot.prototype.innerHTML",
     "ShadowRoot.prototype.lastElementChild",
     "ShadowRoot.prototype.mode",
+    "ShadowRoot.prototype.moveBefore",
     "ShadowRoot.prototype.onslotchange",
     "ShadowRoot.prototype.pictureInPictureElement",
     "ShadowRoot.prototype.pointerLockElement",
@@ -7750,6 +7753,7 @@
     "XMLDocument.prototype.lastModified",
     "XMLDocument.prototype.linkColor",
     "XMLDocument.prototype.links",
+    "XMLDocument.prototype.moveBefore",
     "XMLDocument.prototype.onabort",
     "XMLDocument.prototype.onanimationend",
     "XMLDocument.prototype.onanimationiteration",
```

  
#### 133.0.6905.0 (`2024-12-20`) 
No browser API changes.

  
#### 133.0.6888.2 (`2024-12-12`) ⚡
Added 2 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_133.0.6876.4_to_133.0.6888.2.diff), [json](./browser_apis/chrome-unstable_133.0.6876.4_to_133.0.6888.2.json), [full list](./browser_apis/chrome-unstable_133.0.6888.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_133.0.6876.4.json	2024-12-13 01:18:52.651775575 +0000
+++ ./browser_apis/chrome-unstable_133.0.6888.2.json	2024-12-13 01:19:47.091860938 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8575,
+  "browserApiCount": 8577,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -1960,6 +1960,7 @@
     "HTMLAreaElement",
     "HTMLAreaElement.prototype",
     "HTMLAreaElement.prototype.alt",
+    "HTMLAreaElement.prototype.attributionSrc",
     "HTMLAreaElement.prototype.coords",
     "HTMLAreaElement.prototype.download",
     "HTMLAreaElement.prototype.hash",
@@ -4757,6 +4758,7 @@
     "Proxy",
     "Proxy.revocable",
     "PublicKeyCredential",
+    "PublicKeyCredential.getClientCapabilities",
     "PublicKeyCredential.isConditionalMediationAvailable",
     "PublicKeyCredential.isUserVerifyingPlatformAuthenticatorAvailable",
     "PublicKeyCredential.parseCreationOptionsFromJSON",
```

  
#### 133.0.6876.4 (`2024-12-5`) ⚡
Added 26 APIs, removed 7 (see: [diff](./browser_apis/chrome-unstable_133.0.6847.2_to_133.0.6876.4.diff), [json](./browser_apis/chrome-unstable_133.0.6847.2_to_133.0.6876.4.json), [full list](./browser_apis/chrome-unstable_133.0.6876.4.json))
 ```diff
--- ./browser_apis/chrome-unstable_133.0.6847.2.json	2024-12-06 01:17:17.174768734 +0000
+++ ./browser_apis/chrome-unstable_133.0.6876.4.json	2024-12-06 01:17:49.166737937 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8556,
+  "browserApiCount": 8575,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -110,6 +110,7 @@
     "Atomics.load",
     "Atomics.notify",
     "Atomics.or",
+    "Atomics.pause",
     "Atomics.store",
     "Atomics.sub",
     "Atomics.wait",
@@ -396,6 +397,20 @@
     "ByteLengthQueuingStrategy.prototype.size",
     "CDATASection",
     "CDATASection.prototype",
+    "CSPViolationReportBody",
+    "CSPViolationReportBody.prototype",
+    "CSPViolationReportBody.prototype.blockedURL",
+    "CSPViolationReportBody.prototype.columnNumber",
+    "CSPViolationReportBody.prototype.disposition",
+    "CSPViolationReportBody.prototype.documentURL",
+    "CSPViolationReportBody.prototype.effectiveDirective",
+    "CSPViolationReportBody.prototype.lineNumber",
+    "CSPViolationReportBody.prototype.originalPolicy",
+    "CSPViolationReportBody.prototype.referrer",
+    "CSPViolationReportBody.prototype.sample",
+    "CSPViolationReportBody.prototype.sourceFile",
+    "CSPViolationReportBody.prototype.statusCode",
+    "CSPViolationReportBody.prototype.toJSON",
     "CSS",
     "CSS.Hz",
     "CSS.Q",
@@ -756,6 +771,7 @@
     "CSSTransition.prototype.oncancel",
     "CSSTransition.prototype.onfinish",
     "CSSTransition.prototype.onremove",
+    "CSSTransition.prototype.overallProgress",
     "CSSTransition.prototype.pause",
     "CSSTransition.prototype.pending",
     "CSSTransition.prototype.persist",
@@ -1272,9 +1288,6 @@
     "DocumentPictureInPictureEvent.prototype.window",
     "DocumentTimeline",
     "DocumentTimeline.prototype",
-    "DocumentTimeline.prototype.constructor",
-    "DocumentTimeline.prototype.currentTime",
-    "DocumentTimeline.prototype.duration",
     "DocumentType",
     "DocumentType.prototype",
     "DocumentType.prototype.after",
@@ -4536,6 +4549,7 @@
     "PerformanceResourceTiming.prototype.domainLookupStart",
     "PerformanceResourceTiming.prototype.encodedBodySize",
     "PerformanceResourceTiming.prototype.fetchStart",
+    "PerformanceResourceTiming.prototype.finalResponseHeadersStart",
     "PerformanceResourceTiming.prototype.firstInterimResponseStart",
     "PerformanceResourceTiming.prototype.initiatorType",
     "PerformanceResourceTiming.prototype.nextHopProtocol",
@@ -5093,6 +5107,9 @@
     "RemotePlayback.prototype.prompt",
     "RemotePlayback.prototype.state",
     "RemotePlayback.prototype.watchAvailability",
+    "ReportBody",
+    "ReportBody.prototype",
+    "ReportBody.prototype.toJSON",
     "ReportingObserver",
     "ReportingObserver.prototype",
     "ReportingObserver.prototype.disconnect",
@@ -5988,10 +6005,6 @@
     "ScriptProcessorNode.prototype",
     "ScriptProcessorNode.prototype.bufferSize",
     "ScriptProcessorNode.prototype.onaudioprocess",
-    "ScrollTimeline",
-    "ScrollTimeline.prototype",
-    "ScrollTimeline.prototype.axis",
-    "ScrollTimeline.prototype.source",
     "SecurityPolicyViolationEvent",
     "SecurityPolicyViolationEvent.prototype",
     "SecurityPolicyViolationEvent.prototype.blockedURI",
@@ -6872,7 +6885,13 @@
     "VideoPlaybackQuality.prototype.totalVideoFrames",
     "ViewTimeline",
     "ViewTimeline.prototype",
+    "ViewTimeline.prototype.axis",
+    "ViewTimeline.prototype.constructor",
+    "ViewTimeline.prototype.constructor.prototype",
+    "ViewTimeline.prototype.constructor.prototype.currentTime",
+    "ViewTimeline.prototype.constructor.prototype.duration",
     "ViewTimeline.prototype.endOffset",
+    "ViewTimeline.prototype.source",
     "ViewTimeline.prototype.startOffset",
     "ViewTimeline.prototype.subject",
     "ViewTransition",
```

  
#### 133.0.6847.2 (`2024-11-21`) ⚡
Added 4 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_133.0.6835.3_to_133.0.6847.2.diff), [json](./browser_apis/chrome-unstable_133.0.6835.3_to_133.0.6847.2.json), [full list](./browser_apis/chrome-unstable_133.0.6847.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_133.0.6835.3.json	2024-11-22 01:15:24.339585110 +0000
+++ ./browser_apis/chrome-unstable_133.0.6847.2.json	2024-11-22 01:16:19.780654637 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8552,
+  "browserApiCount": 8556,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -389,6 +389,7 @@
     "BrowserCaptureMediaStreamTrack",
     "BrowserCaptureMediaStreamTrack.prototype",
     "BrowserCaptureMediaStreamTrack.prototype.cropTo",
+    "BrowserCaptureMediaStreamTrack.prototype.restrictTo",
     "ByteLengthQueuingStrategy",
     "ByteLengthQueuingStrategy.prototype",
     "ByteLengthQueuingStrategy.prototype.highWaterMark",
@@ -5161,6 +5162,9 @@
     "Response.prototype.type",
     "Response.prototype.url",
     "Response.redirect",
+    "RestrictionTarget",
+    "RestrictionTarget.fromElement",
+    "RestrictionTarget.prototype",
     "SVGAElement",
     "SVGAElement.prototype",
     "SVGAElement.prototype.href",
```

  
#### 133.0.6835.3 (`2024-11-14`) ⚡
Added 3 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_132.0.6821.2_to_133.0.6835.3.diff), [json](./browser_apis/chrome-unstable_132.0.6821.2_to_133.0.6835.3.json), [full list](./browser_apis/chrome-unstable_133.0.6835.3.json))
 ```diff
--- ./browser_apis/chrome-unstable_132.0.6821.2.json	2024-11-15 01:15:29.136658000 +0000
+++ ./browser_apis/chrome-unstable_133.0.6835.3.json	2024-11-15 01:15:50.068761723 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8549,
+  "browserApiCount": 8552,
   "browserApis": [
     "AICreateMonitor",
     "AICreateMonitor.prototype",
@@ -1646,6 +1646,7 @@
     "GPUComputePipeline.prototype.label",
     "GPUDevice",
     "GPUDevice.prototype",
+    "GPUDevice.prototype.adapterInfo",
     "GPUDevice.prototype.createBindGroup",
     "GPUDevice.prototype.createBindGroupLayout",
     "GPUDevice.prototype.createBuffer",
@@ -2822,6 +2823,7 @@
     "IdentityProvider.close",
     "IdentityProvider.getUserInfo",
     "IdentityProvider.prototype",
+    "IdentityProvider.resolve",
     "IdleDeadline",
     "IdleDeadline.prototype",
     "IdleDeadline.prototype.didTimeout",
@@ -3696,6 +3698,7 @@
     "Navigator.prototype.getBattery",
     "Navigator.prototype.getGamepads",
     "Navigator.prototype.getInstalledRelatedApps",
+    "Navigator.prototype.getInterestGroupAdAuctionData",
     "Navigator.prototype.getUserMedia",
     "Navigator.prototype.gpu",
     "Navigator.prototype.hardwareConcurrency",
```

  
#### 132.0.6821.2 (`2024-11-7`) 
No browser API changes.

  <!-- browserapis:end -->
