# WIP

## Browser APIs

<!-- browserapis:start -->
### chrome-stable
  
#### 141.0.7390.76 (`2025-10-9`) 
No browser API changes.

  
#### 141.0.7390.65 (`2025-10-7`) ⚡
Added 0 APIs, removed 1 (see: [diff](./browser_apis/chrome-stable_141.0.7390.54_to_141.0.7390.65.diff), [json](./browser_apis/chrome-stable_141.0.7390.54_to_141.0.7390.65.json), [full list](./browser_apis/chrome-stable_141.0.7390.65.json))
 ```diff
--- ./browser_apis/chrome-stable_141.0.7390.54.json	2025-10-07 20:00:56.318563537 +0000
+++ ./browser_apis/chrome-stable_141.0.7390.65.json	2025-10-07 20:01:44.879844049 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 8825,
+  "browserApiCount": 8824,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -5306,7 +5306,6 @@
     "Request.prototype.referrer",
     "Request.prototype.referrerPolicy",
     "Request.prototype.signal",
-    "Request.prototype.targetAddressSpace",
     "Request.prototype.text",
     "Request.prototype.url",
     "ResizeObserver",
```

  
#### 141.0.7390.54 (`2025-9-30`) ⚡
Added 24 APIs, removed 0 (see: [diff](./browser_apis/chrome-stable_140.0.7339.207_to_141.0.7390.54.diff), [json](./browser_apis/chrome-stable_140.0.7339.207_to_141.0.7390.54.json), [full list](./browser_apis/chrome-stable_141.0.7390.54.json))
 ```diff
--- ./browser_apis/chrome-stable_140.0.7339.207.json	2025-09-30 21:00:54.904425842 +0000
+++ ./browser_apis/chrome-stable_141.0.7390.54.json	2025-09-30 21:05:12.583449483 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 8801,
+  "browserApiCount": 8825,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -1320,6 +1320,12 @@
     "DevicePosture.prototype",
     "DevicePosture.prototype.onchange",
     "DevicePosture.prototype.type",
+    "DigitalCredential",
+    "DigitalCredential.prototype",
+    "DigitalCredential.prototype.data",
+    "DigitalCredential.prototype.protocol",
+    "DigitalCredential.prototype.toJSON",
+    "DigitalCredential.userAgentAllowsProtocol",
     "DisposableStack",
     "DisposableStack.prototype",
     "DisposableStack.prototype.adopt",
@@ -2827,6 +2833,7 @@
     "IDBIndex.prototype.get",
     "IDBIndex.prototype.getAll",
     "IDBIndex.prototype.getAllKeys",
+    "IDBIndex.prototype.getAllRecords",
     "IDBIndex.prototype.getKey",
     "IDBIndex.prototype.keyPath",
     "IDBIndex.prototype.multiEntry",
@@ -2858,6 +2865,7 @@
     "IDBObjectStore.prototype.get",
     "IDBObjectStore.prototype.getAll",
     "IDBObjectStore.prototype.getAllKeys",
+    "IDBObjectStore.prototype.getAllRecords",
     "IDBObjectStore.prototype.getKey",
     "IDBObjectStore.prototype.index",
     "IDBObjectStore.prototype.indexNames",
@@ -2871,6 +2879,11 @@
     "IDBOpenDBRequest.prototype",
     "IDBOpenDBRequest.prototype.onblocked",
     "IDBOpenDBRequest.prototype.onupgradeneeded",
+    "IDBRecord",
+    "IDBRecord.prototype",
+    "IDBRecord.prototype.key",
+    "IDBRecord.prototype.primaryKey",
+    "IDBRecord.prototype.value",
     "IDBRequest",
     "IDBRequest.prototype",
     "IDBRequest.prototype.error",
@@ -3776,6 +3789,9 @@
     "NavigationHistoryEntry.prototype.ondispose",
     "NavigationHistoryEntry.prototype.sameDocument",
     "NavigationHistoryEntry.prototype.url",
+    "NavigationPrecommitController",
+    "NavigationPrecommitController.prototype",
+    "NavigationPrecommitController.prototype.redirect",
     "NavigationPreloadManager",
     "NavigationPreloadManager.prototype",
     "NavigationPreloadManager.prototype.disable",
@@ -3784,6 +3800,7 @@
     "NavigationPreloadManager.prototype.setHeaderValue",
     "NavigationTransition",
     "NavigationTransition.prototype",
+    "NavigationTransition.prototype.committed",
     "NavigationTransition.prototype.finished",
     "NavigationTransition.prototype.from",
     "NavigationTransition.prototype.navigationType",
@@ -4179,6 +4196,7 @@
     "Option.prototype.constructor.prototype.ariaModal",
     "Option.prototype.constructor.prototype.ariaMultiLine",
     "Option.prototype.constructor.prototype.ariaMultiSelectable",
+    "Option.prototype.constructor.prototype.ariaNotify",
     "Option.prototype.constructor.prototype.ariaOrientation",
     "Option.prototype.constructor.prototype.ariaPlaceholder",
     "Option.prototype.constructor.prototype.ariaPosInSet",
@@ -5060,7 +5078,10 @@
     "RTCRtpReceiver.prototype.playoutDelayHint",
     "RTCRtpReceiver.prototype.rtcpTransport",
     "RTCRtpReceiver.prototype.track",
+    "RTCRtpReceiver.prototype.transform",
     "RTCRtpReceiver.prototype.transport",
+    "RTCRtpScriptTransform",
+    "RTCRtpScriptTransform.prototype",
     "RTCRtpSender",
     "RTCRtpSender.getCapabilities",
     "RTCRtpSender.prototype",
@@ -5073,6 +5094,7 @@
     "RTCRtpSender.prototype.setParameters",
     "RTCRtpSender.prototype.setStreams",
     "RTCRtpSender.prototype.track",
+    "RTCRtpSender.prototype.transform",
     "RTCRtpSender.prototype.transport",
     "RTCRtpTransceiver",
     "RTCRtpTransceiver.prototype",
@@ -5284,6 +5306,7 @@
     "Request.prototype.referrer",
     "Request.prototype.referrerPolicy",
     "Request.prototype.signal",
+    "Request.prototype.targetAddressSpace",
     "Request.prototype.text",
     "Request.prototype.url",
     "ResizeObserver",
@@ -7925,6 +7948,7 @@
     "XMLDocument.prototype.anchors",
     "XMLDocument.prototype.append",
     "XMLDocument.prototype.applets",
+    "XMLDocument.prototype.ariaNotify",
     "XMLDocument.prototype.bgColor",
     "XMLDocument.prototype.body",
     "XMLDocument.prototype.browsingTopics",
```

  
#### 140.0.7339.207 (`2025-9-23`) 
No browser API changes.

  
#### 140.0.7339.185 (`2025-9-17`) 
No browser API changes.

  
#### 140.0.7339.127 (`2025-9-9`) 
No browser API changes.

  
#### 140.0.7339.80 (`2025-9-2`) ⚡
Added 16 APIs, removed 5 (see: [diff](./browser_apis/chrome-stable_139.0.7258.154_to_140.0.7339.80.diff), [json](./browser_apis/chrome-stable_139.0.7258.154_to_140.0.7339.80.json), [full list](./browser_apis/chrome-stable_140.0.7339.80.json))
 ```diff
--- ./browser_apis/chrome-stable_139.0.7258.154.json	2025-09-02 22:00:56.062762837 +0000
+++ ./browser_apis/chrome-stable_140.0.7339.80.json	2025-09-02 22:01:42.857884595 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 8790,
+  "browserApiCount": 8801,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -1616,6 +1616,7 @@
     "FontFace.prototype.style",
     "FontFace.prototype.unicodeRange",
     "FontFace.prototype.variant",
+    "FontFace.prototype.variationSettings",
     "FontFace.prototype.weight",
     "FontFaceSetLoadEvent",
     "FontFaceSetLoadEvent.prototype",
@@ -1646,7 +1647,6 @@
     "GPUAdapter.prototype",
     "GPUAdapter.prototype.features",
     "GPUAdapter.prototype.info",
-    "GPUAdapter.prototype.isFallbackAdapter",
     "GPUAdapter.prototype.limits",
     "GPUAdapter.prototype.requestDevice",
     "GPUAdapterInfo",
@@ -2773,6 +2773,7 @@
     "HighlightRegistry.prototype.forEach",
     "HighlightRegistry.prototype.get",
     "HighlightRegistry.prototype.has",
+    "HighlightRegistry.prototype.highlightsFromPoint",
     "HighlightRegistry.prototype.keys",
     "HighlightRegistry.prototype.set",
     "HighlightRegistry.prototype.size",
@@ -4698,6 +4699,10 @@
     "PerformanceResourceTiming.prototype.serverTiming",
     "PerformanceResourceTiming.prototype.toJSON",
     "PerformanceResourceTiming.prototype.transferSize",
+    "PerformanceResourceTiming.prototype.workerCacheLookupStart",
+    "PerformanceResourceTiming.prototype.workerFinalSourceType",
+    "PerformanceResourceTiming.prototype.workerMatchedSourceType",
+    "PerformanceResourceTiming.prototype.workerRouterEvaluationStart",
     "PerformanceResourceTiming.prototype.workerStart",
     "PerformanceScriptTiming",
     "PerformanceScriptTiming.prototype",
@@ -6764,6 +6769,7 @@
     "ToggleEvent.prototype",
     "ToggleEvent.prototype.newState",
     "ToggleEvent.prototype.oldState",
+    "ToggleEvent.prototype.source",
     "Touch",
     "Touch.prototype",
     "Touch.prototype.clientX",
@@ -6991,6 +6997,8 @@
     "Uint32Array",
     "Uint32Array.prototype",
     "Uint8Array",
+    "Uint8Array.fromBase64",
+    "Uint8Array.fromHex",
     "Uint8Array.prototype",
     "Uint8Array.prototype.at",
     "Uint8Array.prototype.buffer",
@@ -7020,10 +7028,14 @@
     "Uint8Array.prototype.reduceRight",
     "Uint8Array.prototype.reverse",
     "Uint8Array.prototype.set",
+    "Uint8Array.prototype.setFromBase64",
+    "Uint8Array.prototype.setFromHex",
     "Uint8Array.prototype.slice",
     "Uint8Array.prototype.some",
     "Uint8Array.prototype.sort",
     "Uint8Array.prototype.subarray",
+    "Uint8Array.prototype.toBase64",
+    "Uint8Array.prototype.toHex",
     "Uint8Array.prototype.toLocaleString",
     "Uint8Array.prototype.toReversed",
     "Uint8Array.prototype.toSorted",
@@ -8296,7 +8308,10 @@
     "XRInputSourcesChangeEvent.prototype.session",
     "XRJointPose",
     "XRJointPose.prototype",
+    "XRJointPose.prototype.constructor",
+    "XRJointPose.prototype.emulatedPosition",
     "XRJointPose.prototype.radius",
+    "XRJointPose.prototype.transform",
     "XRJointSpace",
     "XRJointSpace.prototype",
     "XRJointSpace.prototype.jointName",
@@ -8311,10 +8326,6 @@
     "XRLightProbe.prototype",
     "XRLightProbe.prototype.onreflectionchange",
     "XRLightProbe.prototype.probeSpace",
-    "XRPose",
-    "XRPose.prototype",
-    "XRPose.prototype.emulatedPosition",
-    "XRPose.prototype.transform",
     "XRRay",
     "XRRay.prototype",
     "XRRay.prototype.direction",
```

  
#### 139.0.7258.154 (`2025-8-26`) 
No browser API changes.

  
#### 139.0.7258.138 (`2025-8-19`) 
No browser API changes.

  
#### 139.0.7258.127 (`2025-8-12`) 
No browser API changes.

  
#### 139.0.7258.66 (`2025-8-5`) ⚡
Added 60 APIs, removed 39 (see: [diff](./browser_apis/chrome-stable_138.0.7204.183_to_139.0.7258.66.diff), [json](./browser_apis/chrome-stable_138.0.7204.183_to_139.0.7258.66.json), [full list](./browser_apis/chrome-stable_139.0.7258.66.json))
 ```diff
--- ./browser_apis/chrome-stable_138.0.7204.183.json	2025-08-05 19:03:49.140953461 +0000
+++ ./browser_apis/chrome-stable_139.0.7258.66.json	2025-08-05 19:04:13.123984164 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 8769,
+  "browserApiCount": 8790,
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
@@ -4553,6 +4564,7 @@
     "PaymentRequest.prototype.shippingOption",
     "PaymentRequest.prototype.shippingType",
     "PaymentRequest.prototype.show",
+    "PaymentRequest.securePaymentConfirmationAvailability",
     "PaymentRequestUpdateEvent",
     "PaymentRequestUpdateEvent.prototype",
     "PaymentRequestUpdateEvent.prototype.updateWith",
@@ -6346,6 +6358,48 @@
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
+    "SpeechRecognition.available",
+    "SpeechRecognition.install",
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
+    "SpeechRecognition.prototype.processLocally",
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
@@ -8179,7 +8233,9 @@
     "XRCPUDepthInformation.prototype.getDepthInMeters",
     "XRCPUDepthInformation.prototype.height",
     "XRCPUDepthInformation.prototype.normDepthBufferFromNormView",
+    "XRCPUDepthInformation.prototype.projectionMatrix",
     "XRCPUDepthInformation.prototype.rawValueToMeters",
+    "XRCPUDepthInformation.prototype.transform",
     "XRCPUDepthInformation.prototype.width",
     "XRCamera",
     "XRCamera.prototype",
@@ -8283,7 +8339,9 @@
     "XRSession",
     "XRSession.prototype",
     "XRSession.prototype.cancelAnimationFrame",
+    "XRSession.prototype.depthActive",
     "XRSession.prototype.depthDataFormat",
+    "XRSession.prototype.depthType",
     "XRSession.prototype.depthUsage",
     "XRSession.prototype.domOverlayState",
     "XRSession.prototype.enabledFeatures",
@@ -8300,6 +8358,7 @@
     "XRSession.prototype.onsqueezeend",
     "XRSession.prototype.onsqueezestart",
     "XRSession.prototype.onvisibilitychange",
+    "XRSession.prototype.pauseDepthSensing",
     "XRSession.prototype.preferredReflectionFormat",
     "XRSession.prototype.renderState",
     "XRSession.prototype.requestAnimationFrame",
@@ -8307,6 +8366,7 @@
     "XRSession.prototype.requestHitTestSourceForTransientInput",
     "XRSession.prototype.requestLightProbe",
     "XRSession.prototype.requestReferenceSpace",
+    "XRSession.prototype.resumeDepthSensing",
     "XRSession.prototype.updateRenderState",
     "XRSession.prototype.visibilityState",
     "XRSessionEvent",
@@ -8711,45 +8771,6 @@
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

  
#### 138.0.7204.183 (`2025-7-29`) 
No browser API changes.

  
#### 138.0.7204.168 (`2025-7-22`) 
No browser API changes.

  
#### 138.0.7204.157 (`2025-7-15`) 
No browser API changes.

  
#### 138.0.7204.100 (`2025-7-8`) 
No browser API changes.

  
#### 138.0.7204.92 (`2025-6-30`) 
No browser API changes.

  
#### 138.0.7204.49 (`2025-6-24`) ⚡
Added 63 APIs, removed 6 (see: [diff](./browser_apis/chrome-stable_137.0.7151.119_to_138.0.7204.49.diff), [json](./browser_apis/chrome-stable_137.0.7151.119_to_138.0.7204.49.json), [full list](./browser_apis/chrome-stable_138.0.7204.49.json))
 ```diff
--- ./browser_apis/chrome-stable_137.0.7151.119.json	2025-06-24 19:00:48.045197681 +0000
+++ ./browser_apis/chrome-stable_138.0.7204.49.json	2025-06-24 19:01:29.821392367 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 8712,
+  "browserApiCount": 8769,
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
@@ -1993,6 +1996,7 @@
     "HTMLAnchorElement.prototype.host",
     "HTMLAnchorElement.prototype.hostname",
     "HTMLAnchorElement.prototype.href",
+    "HTMLAnchorElement.prototype.hrefTranslate",
     "HTMLAnchorElement.prototype.hreflang",
     "HTMLAnchorElement.prototype.name",
     "HTMLAnchorElement.prototype.origin",
@@ -3018,6 +3022,13 @@
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
@@ -3197,6 +3208,15 @@
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
@@ -3950,6 +3970,7 @@
     "Object.prototype.__defineGetter__.arguments",
     "Object.prototype.__defineGetter__.bind",
     "Object.prototype.__defineGetter__.call",
+    "Object.prototype.__defineGetter__.caller",
     "Object.prototype.__defineGetter__.constructor",
     "Object.prototype.__defineGetter__.toString",
     "Object.prototype.__defineSetter__",
@@ -4890,6 +4911,10 @@
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
@@ -5242,7 +5267,6 @@
     "Request.prototype.referrer",
     "Request.prototype.referrerPolicy",
     "Request.prototype.signal",
-    "Request.prototype.targetAddressSpace",
     "Request.prototype.text",
     "Request.prototype.url",
     "ResizeObserver",
@@ -6520,6 +6544,22 @@
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
@@ -6715,6 +6755,17 @@
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
@@ -7003,7 +7054,9 @@
     "VideoFrame.prototype.displayHeight",
     "VideoFrame.prototype.displayWidth",
     "VideoFrame.prototype.duration",
+    "VideoFrame.prototype.flip",
     "VideoFrame.prototype.format",
+    "VideoFrame.prototype.rotation",
     "VideoFrame.prototype.timestamp",
     "VideoFrame.prototype.visibleRect",
     "VideoPlaybackQuality",
@@ -7041,6 +7094,9 @@
     "ViewTransitionTypeSet.prototype.keys",
     "ViewTransitionTypeSet.prototype.size",
     "ViewTransitionTypeSet.prototype.values",
+    "Viewport",
+    "Viewport.prototype",
+    "Viewport.prototype.segments",
     "VirtualKeyboard",
     "VirtualKeyboard.prototype",
     "VirtualKeyboard.prototype.boundingRect",
@@ -8586,6 +8642,7 @@
     "top",
     "trustedTypes",
     "unescape",
+    "viewport",
     "visualViewport",
     "webkitCancelAnimationFrame",
     "webkitMediaStream",
```

  
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

  
### chrome-unstable
  
#### 143.0.7461.2 (`2025-10-10`) ⚡
Added 1 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_143.0.7445.0_to_143.0.7461.2.diff), [json](./browser_apis/chrome-unstable_143.0.7445.0_to_143.0.7461.2.json), [full list](./browser_apis/chrome-unstable_143.0.7461.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_143.0.7445.0.json	2025-10-10 17:00:52.263603700 +0000
+++ ./browser_apis/chrome-unstable_143.0.7461.2.json	2025-10-10 17:01:30.964913296 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8839,
+  "browserApiCount": 8840,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -5312,6 +5312,7 @@
     "Request.prototype.referrer",
     "Request.prototype.referrerPolicy",
     "Request.prototype.signal",
+    "Request.prototype.targetAddressSpace",
     "Request.prototype.text",
     "Request.prototype.url",
     "ResizeObserver",
```

  
#### 143.0.7445.0 (`2025-10-2`) ⚡
Added 1 APIs, removed 1 (see: [diff](./browser_apis/chrome-unstable_142.0.7432.0_to_143.0.7445.0.diff), [json](./browser_apis/chrome-unstable_142.0.7432.0_to_143.0.7445.0.json), [full list](./browser_apis/chrome-unstable_143.0.7445.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_142.0.7432.0.json	2025-10-02 22:00:50.540818821 +0000
+++ ./browser_apis/chrome-unstable_143.0.7445.0.json	2025-10-02 22:01:20.629042374 +0000
@@ -5312,7 +5312,6 @@
     "Request.prototype.referrer",
     "Request.prototype.referrerPolicy",
     "Request.prototype.signal",
-    "Request.prototype.targetAddressSpace",
     "Request.prototype.text",
     "Request.prototype.url",
     "ResizeObserver",
@@ -5357,6 +5356,7 @@
     "RestrictionTarget.prototype",
     "SVGAElement",
     "SVGAElement.prototype",
+    "SVGAElement.prototype.download",
     "SVGAElement.prototype.href",
     "SVGAElement.prototype.interestForElement",
     "SVGAElement.prototype.rel",
```

  
#### 142.0.7432.0 (`2025-9-25`) ⚡
Added 25 APIs, removed 18 (see: [diff](./browser_apis/chrome-unstable_142.0.7420.2_to_142.0.7432.0.diff), [json](./browser_apis/chrome-unstable_142.0.7420.2_to_142.0.7432.0.json), [full list](./browser_apis/chrome-unstable_142.0.7432.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_142.0.7420.2.json	2025-09-25 18:01:00.597455545 +0000
+++ ./browser_apis/chrome-unstable_142.0.7432.0.json	2025-09-25 18:04:22.148957916 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8832,
+  "browserApiCount": 8839,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -2015,6 +2015,7 @@
     "HTMLAnchorElement.prototype.href",
     "HTMLAnchorElement.prototype.hrefTranslate",
     "HTMLAnchorElement.prototype.hreflang",
+    "HTMLAnchorElement.prototype.interestForElement",
     "HTMLAnchorElement.prototype.name",
     "HTMLAnchorElement.prototype.origin",
     "HTMLAnchorElement.prototype.password",
@@ -2043,6 +2044,7 @@
     "HTMLAreaElement.prototype.host",
     "HTMLAreaElement.prototype.hostname",
     "HTMLAreaElement.prototype.href",
+    "HTMLAreaElement.prototype.interestForElement",
     "HTMLAreaElement.prototype.noHref",
     "HTMLAreaElement.prototype.origin",
     "HTMLAreaElement.prototype.password",
@@ -2107,6 +2109,7 @@
     "HTMLButtonElement.prototype.formMethod",
     "HTMLButtonElement.prototype.formNoValidate",
     "HTMLButtonElement.prototype.formTarget",
+    "HTMLButtonElement.prototype.interestForElement",
     "HTMLButtonElement.prototype.labels",
     "HTMLButtonElement.prototype.name",
     "HTMLButtonElement.prototype.popoverTargetAction",
@@ -3054,6 +3057,9 @@
     "IntegrityViolationReportBody.prototype.documentURL",
     "IntegrityViolationReportBody.prototype.reportOnly",
     "IntegrityViolationReportBody.prototype.toJSON",
+    "InterestEvent",
+    "InterestEvent.prototype",
+    "InterestEvent.prototype.source",
     "IntersectionObserver",
     "IntersectionObserver.prototype",
     "IntersectionObserver.prototype.delay",
@@ -5352,6 +5358,7 @@
     "SVGAElement",
     "SVGAElement.prototype",
     "SVGAElement.prototype.href",
+    "SVGAElement.prototype.interestForElement",
     "SVGAElement.prototype.rel",
     "SVGAElement.prototype.relList",
     "SVGAElement.prototype.target",
@@ -7857,9 +7864,27 @@
     "WheelEvent.prototype.clientY",
     "WheelEvent.prototype.constructor",
     "WheelEvent.prototype.constructor.prototype",
+    "WheelEvent.prototype.constructor.prototype.bubbles",
+    "WheelEvent.prototype.constructor.prototype.cancelBubble",
+    "WheelEvent.prototype.constructor.prototype.cancelable",
+    "WheelEvent.prototype.constructor.prototype.composed",
+    "WheelEvent.prototype.constructor.prototype.composedPath",
+    "WheelEvent.prototype.constructor.prototype.constructor",
+    "WheelEvent.prototype.constructor.prototype.currentTarget",
+    "WheelEvent.prototype.constructor.prototype.defaultPrevented",
     "WheelEvent.prototype.constructor.prototype.detail",
+    "WheelEvent.prototype.constructor.prototype.eventPhase",
+    "WheelEvent.prototype.constructor.prototype.initEvent",
     "WheelEvent.prototype.constructor.prototype.initUIEvent",
+    "WheelEvent.prototype.constructor.prototype.preventDefault",
+    "WheelEvent.prototype.constructor.prototype.returnValue",
     "WheelEvent.prototype.constructor.prototype.sourceCapabilities",
+    "WheelEvent.prototype.constructor.prototype.srcElement",
+    "WheelEvent.prototype.constructor.prototype.stopImmediatePropagation",
+    "WheelEvent.prototype.constructor.prototype.stopPropagation",
+    "WheelEvent.prototype.constructor.prototype.target",
+    "WheelEvent.prototype.constructor.prototype.timeStamp",
+    "WheelEvent.prototype.constructor.prototype.type",
     "WheelEvent.prototype.constructor.prototype.view",
     "WheelEvent.prototype.constructor.prototype.which",
     "WheelEvent.prototype.ctrlKey",
@@ -7898,25 +7923,7 @@
     "WindowControlsOverlay.prototype.visible",
     "WindowControlsOverlayGeometryChangeEvent",
     "WindowControlsOverlayGeometryChangeEvent.prototype",
-    "WindowControlsOverlayGeometryChangeEvent.prototype.bubbles",
-    "WindowControlsOverlayGeometryChangeEvent.prototype.cancelBubble",
-    "WindowControlsOverlayGeometryChangeEvent.prototype.cancelable",
-    "WindowControlsOverlayGeometryChangeEvent.prototype.composed",
-    "WindowControlsOverlayGeometryChangeEvent.prototype.composedPath",
-    "WindowControlsOverlayGeometryChangeEvent.prototype.constructor",
-    "WindowControlsOverlayGeometryChangeEvent.prototype.currentTarget",
-    "WindowControlsOverlayGeometryChangeEvent.prototype.defaultPrevented",
-    "WindowControlsOverlayGeometryChangeEvent.prototype.eventPhase",
-    "WindowControlsOverlayGeometryChangeEvent.prototype.initEvent",
-    "WindowControlsOverlayGeometryChangeEvent.prototype.preventDefault",
-    "WindowControlsOverlayGeometryChangeEvent.prototype.returnValue",
-    "WindowControlsOverlayGeometryChangeEvent.prototype.srcElement",
-    "WindowControlsOverlayGeometryChangeEvent.prototype.stopImmediatePropagation",
-    "WindowControlsOverlayGeometryChangeEvent.prototype.stopPropagation",
-    "WindowControlsOverlayGeometryChangeEvent.prototype.target",
-    "WindowControlsOverlayGeometryChangeEvent.prototype.timeStamp",
     "WindowControlsOverlayGeometryChangeEvent.prototype.titlebarAreaRect",
-    "WindowControlsOverlayGeometryChangeEvent.prototype.type",
     "WindowControlsOverlayGeometryChangeEvent.prototype.visible",
     "Worker",
     "Worker.prototype",
```

  
#### 142.0.7420.2 (`2025-9-19`) 
No browser API changes.

  
#### 142.0.7405.0 (`2025-9-11`) ⚡
Added 7 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_142.0.7393.6_to_142.0.7405.0.diff), [json](./browser_apis/chrome-unstable_142.0.7393.6_to_142.0.7405.0.json), [full list](./browser_apis/chrome-unstable_142.0.7405.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_142.0.7393.6.json	2025-09-11 21:00:52.352239984 +0000
+++ ./browser_apis/chrome-unstable_142.0.7405.0.json	2025-09-11 21:01:34.893265601 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8825,
+  "browserApiCount": 8832,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -5306,6 +5306,7 @@
     "Request.prototype.referrer",
     "Request.prototype.referrerPolicy",
     "Request.prototype.signal",
+    "Request.prototype.targetAddressSpace",
     "Request.prototype.text",
     "Request.prototype.url",
     "ResizeObserver",
@@ -5893,6 +5894,7 @@
     "SVGSVGElement.prototype.zoomAndPan",
     "SVGScriptElement",
     "SVGScriptElement.prototype",
+    "SVGScriptElement.prototype.async",
     "SVGScriptElement.prototype.href",
     "SVGScriptElement.prototype.type",
     "SVGSetElement",
@@ -6416,6 +6418,7 @@
     "SpeechRecognition.prototype.onspeechend",
     "SpeechRecognition.prototype.onspeechstart",
     "SpeechRecognition.prototype.onstart",
+    "SpeechRecognition.prototype.phrases",
     "SpeechRecognition.prototype.processLocally",
     "SpeechRecognition.prototype.start",
     "SpeechRecognition.prototype.stop",
@@ -6427,6 +6430,10 @@
     "SpeechRecognitionEvent.prototype",
     "SpeechRecognitionEvent.prototype.resultIndex",
     "SpeechRecognitionEvent.prototype.results",
+    "SpeechRecognitionPhrase",
+    "SpeechRecognitionPhrase.prototype",
+    "SpeechRecognitionPhrase.prototype.boost",
+    "SpeechRecognitionPhrase.prototype.phrase",
     "SpeechSynthesis",
     "SpeechSynthesis.prototype",
     "SpeechSynthesis.prototype.cancel",
```

  
#### 142.0.7393.6 (`2025-9-8`) ⚡
Added 11 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_141.0.7378.3_to_142.0.7393.6.diff), [json](./browser_apis/chrome-unstable_141.0.7378.3_to_142.0.7393.6.json), [full list](./browser_apis/chrome-unstable_142.0.7393.6.json))
 ```diff
--- ./browser_apis/chrome-unstable_141.0.7378.3.json	2025-09-08 22:01:00.959935212 +0000
+++ ./browser_apis/chrome-unstable_142.0.7393.6.json	2025-09-08 22:01:35.802060335 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8814,
+  "browserApiCount": 8825,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -1320,6 +1320,12 @@
     "DevicePosture.prototype",
     "DevicePosture.prototype.onchange",
     "DevicePosture.prototype.type",
+    "DigitalCredential",
+    "DigitalCredential.prototype",
+    "DigitalCredential.prototype.data",
+    "DigitalCredential.prototype.protocol",
+    "DigitalCredential.prototype.toJSON",
+    "DigitalCredential.userAgentAllowsProtocol",
     "DisposableStack",
     "DisposableStack.prototype",
     "DisposableStack.prototype.adopt",
@@ -5072,7 +5078,10 @@
     "RTCRtpReceiver.prototype.playoutDelayHint",
     "RTCRtpReceiver.prototype.rtcpTransport",
     "RTCRtpReceiver.prototype.track",
+    "RTCRtpReceiver.prototype.transform",
     "RTCRtpReceiver.prototype.transport",
+    "RTCRtpScriptTransform",
+    "RTCRtpScriptTransform.prototype",
     "RTCRtpSender",
     "RTCRtpSender.getCapabilities",
     "RTCRtpSender.prototype",
@@ -5085,6 +5094,7 @@
     "RTCRtpSender.prototype.setParameters",
     "RTCRtpSender.prototype.setStreams",
     "RTCRtpSender.prototype.track",
+    "RTCRtpSender.prototype.transform",
     "RTCRtpSender.prototype.transport",
     "RTCRtpTransceiver",
     "RTCRtpTransceiver.prototype",
@@ -7930,6 +7940,7 @@
     "XMLDocument.prototype",
     "XMLDocument.prototype.URL",
     "XMLDocument.prototype.activeElement",
+    "XMLDocument.prototype.activeViewTransition",
     "XMLDocument.prototype.adoptNode",
     "XMLDocument.prototype.adoptedStyleSheets",
     "XMLDocument.prototype.alinkColor",
```

  
#### 141.0.7378.3 (`2025-8-28`) ⚡
Added 6 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_141.0.7367.0_to_141.0.7378.3.diff), [json](./browser_apis/chrome-unstable_141.0.7367.0_to_141.0.7378.3.json), [full list](./browser_apis/chrome-unstable_141.0.7378.3.json))
 ```diff
--- ./browser_apis/chrome-unstable_141.0.7367.0.json	2025-08-28 18:00:57.036333100 +0000
+++ ./browser_apis/chrome-unstable_141.0.7378.3.json	2025-08-28 18:01:49.102735022 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8808,
+  "browserApiCount": 8814,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -3783,6 +3783,9 @@
     "NavigationHistoryEntry.prototype.ondispose",
     "NavigationHistoryEntry.prototype.sameDocument",
     "NavigationHistoryEntry.prototype.url",
+    "NavigationPrecommitController",
+    "NavigationPrecommitController.prototype",
+    "NavigationPrecommitController.prototype.redirect",
     "NavigationPreloadManager",
     "NavigationPreloadManager.prototype",
     "NavigationPreloadManager.prototype.disable",
@@ -3791,6 +3794,7 @@
     "NavigationPreloadManager.prototype.setHeaderValue",
     "NavigationTransition",
     "NavigationTransition.prototype",
+    "NavigationTransition.prototype.committed",
     "NavigationTransition.prototype.finished",
     "NavigationTransition.prototype.from",
     "NavigationTransition.prototype.navigationType",
@@ -4186,6 +4190,7 @@
     "Option.prototype.constructor.prototype.ariaModal",
     "Option.prototype.constructor.prototype.ariaMultiLine",
     "Option.prototype.constructor.prototype.ariaMultiSelectable",
+    "Option.prototype.constructor.prototype.ariaNotify",
     "Option.prototype.constructor.prototype.ariaOrientation",
     "Option.prototype.constructor.prototype.ariaPlaceholder",
     "Option.prototype.constructor.prototype.ariaPosInSet",
@@ -7932,6 +7937,7 @@
     "XMLDocument.prototype.anchors",
     "XMLDocument.prototype.append",
     "XMLDocument.prototype.applets",
+    "XMLDocument.prototype.ariaNotify",
     "XMLDocument.prototype.bgColor",
     "XMLDocument.prototype.body",
     "XMLDocument.prototype.browsingTopics",
```

  
#### 141.0.7367.0 (`2025-8-21`) 
No browser API changes.

  
#### 141.0.7354.0 (`2025-8-14`) 
No browser API changes.

  
#### 141.0.7340.0 (`2025-8-7`) ⚡
Added 7 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_140.0.7327.6_to_141.0.7340.0.diff), [json](./browser_apis/chrome-unstable_140.0.7327.6_to_141.0.7340.0.json), [full list](./browser_apis/chrome-unstable_141.0.7340.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_140.0.7327.6.json	2025-08-07 17:03:13.366565972 +0000
+++ ./browser_apis/chrome-unstable_141.0.7340.0.json	2025-08-07 17:03:43.085576095 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8801,
+  "browserApiCount": 8808,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -2827,6 +2827,7 @@
     "IDBIndex.prototype.get",
     "IDBIndex.prototype.getAll",
     "IDBIndex.prototype.getAllKeys",
+    "IDBIndex.prototype.getAllRecords",
     "IDBIndex.prototype.getKey",
     "IDBIndex.prototype.keyPath",
     "IDBIndex.prototype.multiEntry",
@@ -2858,6 +2859,7 @@
     "IDBObjectStore.prototype.get",
     "IDBObjectStore.prototype.getAll",
     "IDBObjectStore.prototype.getAllKeys",
+    "IDBObjectStore.prototype.getAllRecords",
     "IDBObjectStore.prototype.getKey",
     "IDBObjectStore.prototype.index",
     "IDBObjectStore.prototype.indexNames",
@@ -2871,6 +2873,11 @@
     "IDBOpenDBRequest.prototype",
     "IDBOpenDBRequest.prototype.onblocked",
     "IDBOpenDBRequest.prototype.onupgradeneeded",
+    "IDBRecord",
+    "IDBRecord.prototype",
+    "IDBRecord.prototype.key",
+    "IDBRecord.prototype.primaryKey",
+    "IDBRecord.prototype.value",
     "IDBRequest",
     "IDBRequest.prototype",
     "IDBRequest.prototype.error",
```

  
#### 140.0.7327.6 (`2025-7-31`) ⚡
Added 8 APIs, removed 4 (see: [diff](./browser_apis/chrome-unstable_140.0.7312.0_to_140.0.7327.6.diff), [json](./browser_apis/chrome-unstable_140.0.7312.0_to_140.0.7327.6.json), [full list](./browser_apis/chrome-unstable_140.0.7327.6.json))
 ```diff
--- ./browser_apis/chrome-unstable_140.0.7312.0.json	2025-07-31 18:01:06.570395750 +0000
+++ ./browser_apis/chrome-unstable_140.0.7327.6.json	2025-07-31 18:01:35.172051865 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8797,
+  "browserApiCount": 8801,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -4699,6 +4699,10 @@
     "PerformanceResourceTiming.prototype.serverTiming",
     "PerformanceResourceTiming.prototype.toJSON",
     "PerformanceResourceTiming.prototype.transferSize",
+    "PerformanceResourceTiming.prototype.workerCacheLookupStart",
+    "PerformanceResourceTiming.prototype.workerFinalSourceType",
+    "PerformanceResourceTiming.prototype.workerMatchedSourceType",
+    "PerformanceResourceTiming.prototype.workerRouterEvaluationStart",
     "PerformanceResourceTiming.prototype.workerStart",
     "PerformanceScriptTiming",
     "PerformanceScriptTiming.prototype",
@@ -6765,6 +6769,7 @@
     "ToggleEvent.prototype",
     "ToggleEvent.prototype.newState",
     "ToggleEvent.prototype.oldState",
+    "ToggleEvent.prototype.source",
     "Touch",
     "Touch.prototype",
     "Touch.prototype.clientX",
@@ -8303,7 +8308,10 @@
     "XRInputSourcesChangeEvent.prototype.session",
     "XRJointPose",
     "XRJointPose.prototype",
+    "XRJointPose.prototype.constructor",
+    "XRJointPose.prototype.emulatedPosition",
     "XRJointPose.prototype.radius",
+    "XRJointPose.prototype.transform",
     "XRJointSpace",
     "XRJointSpace.prototype",
     "XRJointSpace.prototype.jointName",
@@ -8318,10 +8326,6 @@
     "XRLightProbe.prototype",
     "XRLightProbe.prototype.onreflectionchange",
     "XRLightProbe.prototype.probeSpace",
-    "XRPose",
-    "XRPose.prototype",
-    "XRPose.prototype.emulatedPosition",
-    "XRPose.prototype.transform",
     "XRRay",
     "XRRay.prototype",
     "XRRay.prototype.direction",
```

  
#### 140.0.7312.0 (`2025-7-24`) 
No browser API changes.

  
#### 140.0.7299.0 (`2025-7-17`) ⚡
Added 8 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_140.0.7259.2_to_140.0.7299.0.diff), [json](./browser_apis/chrome-unstable_140.0.7259.2_to_140.0.7299.0.json), [full list](./browser_apis/chrome-unstable_140.0.7299.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_140.0.7259.2.json	2025-07-17 17:02:31.448524767 +0000
+++ ./browser_apis/chrome-unstable_140.0.7299.0.json	2025-07-17 17:02:56.118695931 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8789,
+  "browserApiCount": 8797,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -1616,6 +1616,7 @@
     "FontFace.prototype.style",
     "FontFace.prototype.unicodeRange",
     "FontFace.prototype.variant",
+    "FontFace.prototype.variationSettings",
     "FontFace.prototype.weight",
     "FontFaceSetLoadEvent",
     "FontFaceSetLoadEvent.prototype",
@@ -2772,6 +2773,7 @@
     "HighlightRegistry.prototype.forEach",
     "HighlightRegistry.prototype.get",
     "HighlightRegistry.prototype.has",
+    "HighlightRegistry.prototype.highlightsFromPoint",
     "HighlightRegistry.prototype.keys",
     "HighlightRegistry.prototype.set",
     "HighlightRegistry.prototype.size",
@@ -6990,6 +6992,8 @@
     "Uint32Array",
     "Uint32Array.prototype",
     "Uint8Array",
+    "Uint8Array.fromBase64",
+    "Uint8Array.fromHex",
     "Uint8Array.prototype",
     "Uint8Array.prototype.at",
     "Uint8Array.prototype.buffer",
@@ -7019,10 +7023,14 @@
     "Uint8Array.prototype.reduceRight",
     "Uint8Array.prototype.reverse",
     "Uint8Array.prototype.set",
+    "Uint8Array.prototype.setFromBase64",
+    "Uint8Array.prototype.setFromHex",
     "Uint8Array.prototype.slice",
     "Uint8Array.prototype.some",
     "Uint8Array.prototype.sort",
     "Uint8Array.prototype.subarray",
+    "Uint8Array.prototype.toBase64",
+    "Uint8Array.prototype.toHex",
     "Uint8Array.prototype.toLocaleString",
     "Uint8Array.prototype.toReversed",
     "Uint8Array.prototype.toSorted",
```

  
#### 140.0.7259.2 (`2025-6-26`) ⚡
Added 1 APIs, removed 1 (see: [diff](./browser_apis/chrome-unstable_139.0.7246.0_to_140.0.7259.2.diff), [json](./browser_apis/chrome-unstable_139.0.7246.0_to_140.0.7259.2.json), [full list](./browser_apis/chrome-unstable_140.0.7259.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_139.0.7246.0.json	2025-06-26 18:01:09.814173108 +0000
+++ ./browser_apis/chrome-unstable_140.0.7259.2.json	2025-06-26 18:01:34.350306757 +0000
@@ -1646,7 +1646,6 @@
     "GPUAdapter.prototype",
     "GPUAdapter.prototype.features",
     "GPUAdapter.prototype.info",
-    "GPUAdapter.prototype.isFallbackAdapter",
     "GPUAdapter.prototype.limits",
     "GPUAdapter.prototype.requestDevice",
     "GPUAdapterInfo",
@@ -4564,6 +4563,7 @@
     "PaymentRequest.prototype.shippingOption",
     "PaymentRequest.prototype.shippingType",
     "PaymentRequest.prototype.show",
+    "PaymentRequest.securePaymentConfirmationAvailability",
     "PaymentRequestUpdateEvent",
     "PaymentRequestUpdateEvent.prototype",
     "PaymentRequestUpdateEvent.prototype.updateWith",
```

  
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

  <!-- browserapis:end -->
