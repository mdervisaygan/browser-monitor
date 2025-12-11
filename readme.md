# WIP

## Browser APIs

<!-- browserapis:start -->
### chrome-stable
  
#### 143.0.7499.109 (`2025-12-10`) 
No browser API changes.

  
#### 143.0.7499.40 (`2025-12-2`) ⚡
Added 8 APIs, removed 7 (see: [diff](./browser_apis/chrome-stable_142.0.7444.175_to_143.0.7499.40.diff), [json](./browser_apis/chrome-stable_142.0.7444.175_to_143.0.7499.40.json), [full list](./browser_apis/chrome-stable_143.0.7499.40.json))
 ```diff
--- ./browser_apis/chrome-stable_142.0.7444.175.json	2025-12-02 19:02:33.560459989 +0000
+++ ./browser_apis/chrome-stable_143.0.7499.40.json	2025-12-02 19:03:07.196762870 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 8840,
+  "browserApiCount": 8841,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -2079,6 +2079,8 @@
     "HTMLBodyElement.prototype.onblur",
     "HTMLBodyElement.prototype.onerror",
     "HTMLBodyElement.prototype.onfocus",
+    "HTMLBodyElement.prototype.ongamepadconnected",
+    "HTMLBodyElement.prototype.ongamepaddisconnected",
     "HTMLBodyElement.prototype.onhashchange",
     "HTMLBodyElement.prototype.onlanguagechange",
     "HTMLBodyElement.prototype.onload",
@@ -2239,6 +2241,8 @@
     "HTMLFrameSetElement.prototype.onblur",
     "HTMLFrameSetElement.prototype.onerror",
     "HTMLFrameSetElement.prototype.onfocus",
+    "HTMLFrameSetElement.prototype.ongamepadconnected",
+    "HTMLFrameSetElement.prototype.ongamepaddisconnected",
     "HTMLFrameSetElement.prototype.onhashchange",
     "HTMLFrameSetElement.prototype.onlanguagechange",
     "HTMLFrameSetElement.prototype.onload",
@@ -3117,10 +3121,8 @@
     "Intl.Locale.prototype",
     "Intl.Locale.prototype.baseName",
     "Intl.Locale.prototype.calendar",
-    "Intl.Locale.prototype.calendars",
     "Intl.Locale.prototype.caseFirst",
     "Intl.Locale.prototype.collation",
-    "Intl.Locale.prototype.collations",
     "Intl.Locale.prototype.firstDayOfWeek",
     "Intl.Locale.prototype.getCalendars",
     "Intl.Locale.prototype.getCollations",
@@ -3130,19 +3132,14 @@
     "Intl.Locale.prototype.getTimeZones",
     "Intl.Locale.prototype.getWeekInfo",
     "Intl.Locale.prototype.hourCycle",
-    "Intl.Locale.prototype.hourCycles",
     "Intl.Locale.prototype.language",
     "Intl.Locale.prototype.maximize",
     "Intl.Locale.prototype.minimize",
     "Intl.Locale.prototype.numberingSystem",
-    "Intl.Locale.prototype.numberingSystems",
     "Intl.Locale.prototype.numeric",
     "Intl.Locale.prototype.region",
     "Intl.Locale.prototype.script",
-    "Intl.Locale.prototype.textInfo",
-    "Intl.Locale.prototype.timeZones",
     "Intl.Locale.prototype.toString",
-    "Intl.Locale.prototype.weekInfo",
     "Intl.NumberFormat",
     "Intl.NumberFormat.prototype",
     "Intl.NumberFormat.prototype.format",
@@ -4702,6 +4699,7 @@
     "PerformanceResourceTiming.prototype",
     "PerformanceResourceTiming.prototype.connectEnd",
     "PerformanceResourceTiming.prototype.connectStart",
+    "PerformanceResourceTiming.prototype.contentEncoding",
     "PerformanceResourceTiming.prototype.decodedBodySize",
     "PerformanceResourceTiming.prototype.deliveryType",
     "PerformanceResourceTiming.prototype.domainLookupEnd",
@@ -7838,6 +7836,7 @@
     "WebTransport.prototype.datagrams",
     "WebTransport.prototype.incomingBidirectionalStreams",
     "WebTransport.prototype.incomingUnidirectionalStreams",
+    "WebTransport.prototype.protocol",
     "WebTransport.prototype.ready",
     "WebTransportBidirectionalStream",
     "WebTransportBidirectionalStream.prototype",
@@ -8622,6 +8621,8 @@
     "onerror",
     "onfocus",
     "onformdata",
+    "ongamepadconnected",
+    "ongamepaddisconnected",
     "ongotpointercapture",
     "onhashchange",
     "oninput",
```

  
#### 142.0.7444.175 (`2025-11-17`) 
No browser API changes.

  
#### 142.0.7444.162 (`2025-11-11`) 
No browser API changes.

  
#### 142.0.7444.134 (`2025-11-5`) 
No browser API changes.

  
#### 142.0.7444.59 (`2025-10-28`) ⚡
Added 34 APIs, removed 18 (see: [diff](./browser_apis/chrome-stable_141.0.7390.122_to_142.0.7444.59.diff), [json](./browser_apis/chrome-stable_141.0.7390.122_to_142.0.7444.59.json), [full list](./browser_apis/chrome-stable_142.0.7444.59.json))
 ```diff
--- ./browser_apis/chrome-stable_141.0.7390.122.json	2025-10-28 22:00:57.010684385 +0000
+++ ./browser_apis/chrome-stable_142.0.7444.59.json	2025-10-28 22:01:31.792125161 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 8824,
+  "browserApiCount": 8840,
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
@@ -5306,6 +5312,7 @@
     "Request.prototype.referrer",
     "Request.prototype.referrerPolicy",
     "Request.prototype.signal",
+    "Request.prototype.targetAddressSpace",
     "Request.prototype.text",
     "Request.prototype.url",
     "ResizeObserver",
@@ -5350,7 +5357,9 @@
     "RestrictionTarget.prototype",
     "SVGAElement",
     "SVGAElement.prototype",
+    "SVGAElement.prototype.download",
     "SVGAElement.prototype.href",
+    "SVGAElement.prototype.interestForElement",
     "SVGAElement.prototype.rel",
     "SVGAElement.prototype.relList",
     "SVGAElement.prototype.target",
@@ -5893,6 +5902,7 @@
     "SVGSVGElement.prototype.zoomAndPan",
     "SVGScriptElement",
     "SVGScriptElement.prototype",
+    "SVGScriptElement.prototype.async",
     "SVGScriptElement.prototype.href",
     "SVGScriptElement.prototype.type",
     "SVGSetElement",
@@ -6416,6 +6426,7 @@
     "SpeechRecognition.prototype.onspeechend",
     "SpeechRecognition.prototype.onspeechstart",
     "SpeechRecognition.prototype.onstart",
+    "SpeechRecognition.prototype.phrases",
     "SpeechRecognition.prototype.processLocally",
     "SpeechRecognition.prototype.start",
     "SpeechRecognition.prototype.stop",
@@ -6427,6 +6438,10 @@
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
@@ -7850,9 +7865,27 @@
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
@@ -7891,25 +7924,7 @@
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
@@ -7940,6 +7955,7 @@
     "XMLDocument.prototype",
     "XMLDocument.prototype.URL",
     "XMLDocument.prototype.activeElement",
+    "XMLDocument.prototype.activeViewTransition",
     "XMLDocument.prototype.adoptNode",
     "XMLDocument.prototype.adoptedStyleSheets",
     "XMLDocument.prototype.alinkColor",
```

  
#### 141.0.7390.122 (`2025-10-21`) 
No browser API changes.

  
#### 141.0.7390.107 (`2025-10-14`) 
No browser API changes.

  
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

  
### chrome-unstable
  
#### 145.0.7572.2 (`2025-12-11`) ⚡
Added 24 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_145.0.7561.2_to_145.0.7572.2.diff), [json](./browser_apis/chrome-unstable_145.0.7561.2_to_145.0.7572.2.json), [full list](./browser_apis/chrome-unstable_145.0.7572.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_145.0.7561.2.json	2025-12-11 20:00:57.160218440 +0000
+++ ./browser_apis/chrome-unstable_145.0.7572.2.json	2025-12-11 20:01:31.144991969 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9123,
+  "browserApiCount": 9147,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -3273,6 +3273,8 @@
     "LargestContentfulPaint.prototype.element",
     "LargestContentfulPaint.prototype.id",
     "LargestContentfulPaint.prototype.loadTime",
+    "LargestContentfulPaint.prototype.paintTime",
+    "LargestContentfulPaint.prototype.presentationTime",
     "LargestContentfulPaint.prototype.renderTime",
     "LargestContentfulPaint.prototype.size",
     "LargestContentfulPaint.prototype.toJSON",
@@ -3364,6 +3366,8 @@
     "Map.prototype.entries",
     "Map.prototype.forEach",
     "Map.prototype.get",
+    "Map.prototype.getOrInsert",
+    "Map.prototype.getOrInsertComputed",
     "Map.prototype.has",
     "Map.prototype.keys",
     "Map.prototype.set",
@@ -3415,6 +3419,7 @@
     "MathMLElement.prototype.focus",
     "MathMLElement.prototype.nonce",
     "MathMLElement.prototype.onabort",
+    "MathMLElement.prototype.onanimationcancel",
     "MathMLElement.prototype.onanimationend",
     "MathMLElement.prototype.onanimationiteration",
     "MathMLElement.prototype.onanimationstart",
@@ -4350,6 +4355,7 @@
     "Option.prototype.constructor.prototype.offsetTop",
     "Option.prototype.constructor.prototype.offsetWidth",
     "Option.prototype.constructor.prototype.onabort",
+    "Option.prototype.constructor.prototype.onanimationcancel",
     "Option.prototype.constructor.prototype.onanimationend",
     "Option.prototype.constructor.prototype.onanimationiteration",
     "Option.prototype.constructor.prototype.onanimationstart",
@@ -4516,6 +4522,12 @@
     "Option.prototype.selected",
     "Option.prototype.text",
     "Option.prototype.value",
+    "Origin",
+    "Origin.from",
+    "Origin.prototype",
+    "Origin.prototype.isSameOrigin",
+    "Origin.prototype.isSameSite",
+    "Origin.prototype.opaque",
     "OscillatorNode",
     "OscillatorNode.prototype",
     "OscillatorNode.prototype.constructor",
@@ -4656,6 +4668,8 @@
     "PerformanceElementTiming.prototype.loadTime",
     "PerformanceElementTiming.prototype.naturalHeight",
     "PerformanceElementTiming.prototype.naturalWidth",
+    "PerformanceElementTiming.prototype.paintTime",
+    "PerformanceElementTiming.prototype.presentationTime",
     "PerformanceElementTiming.prototype.renderTime",
     "PerformanceElementTiming.prototype.toJSON",
     "PerformanceElementTiming.prototype.url",
@@ -4671,6 +4685,8 @@
     "PerformanceLongAnimationFrameTiming.prototype",
     "PerformanceLongAnimationFrameTiming.prototype.blockingDuration",
     "PerformanceLongAnimationFrameTiming.prototype.firstUIEventTimestamp",
+    "PerformanceLongAnimationFrameTiming.prototype.paintTime",
+    "PerformanceLongAnimationFrameTiming.prototype.presentationTime",
     "PerformanceLongAnimationFrameTiming.prototype.renderStart",
     "PerformanceLongAnimationFrameTiming.prototype.scripts",
     "PerformanceLongAnimationFrameTiming.prototype.styleAndLayoutStart",
@@ -4719,6 +4735,9 @@
     "PerformanceObserverEntryList.prototype.getEntriesByType",
     "PerformancePaintTiming",
     "PerformancePaintTiming.prototype",
+    "PerformancePaintTiming.prototype.paintTime",
+    "PerformancePaintTiming.prototype.presentationTime",
+    "PerformancePaintTiming.prototype.toJSON",
     "PerformanceResourceTiming",
     "PerformanceResourceTiming.prototype",
     "PerformanceResourceTiming.prototype.connectEnd",
@@ -6058,6 +6077,7 @@
     "SVGViewElement.prototype.focus",
     "SVGViewElement.prototype.nonce",
     "SVGViewElement.prototype.onabort",
+    "SVGViewElement.prototype.onanimationcancel",
     "SVGViewElement.prototype.onanimationend",
     "SVGViewElement.prototype.onanimationiteration",
     "SVGViewElement.prototype.onanimationstart",
@@ -7532,6 +7552,8 @@
     "WeakMap.prototype",
     "WeakMap.prototype.delete",
     "WeakMap.prototype.get",
+    "WeakMap.prototype.getOrInsert",
+    "WeakMap.prototype.getOrInsertComputed",
     "WeakMap.prototype.has",
     "WeakMap.prototype.set",
     "WeakRef",
@@ -8317,6 +8339,7 @@
     "XMLDocument.prototype.links",
     "XMLDocument.prototype.moveBefore",
     "XMLDocument.prototype.onabort",
+    "XMLDocument.prototype.onanimationcancel",
     "XMLDocument.prototype.onanimationend",
     "XMLDocument.prototype.onanimationiteration",
     "XMLDocument.prototype.onanimationstart",
@@ -8861,6 +8884,7 @@
     "offscreenBuffering",
     "onabort",
     "onafterprint",
+    "onanimationcancel",
     "onanimationend",
     "onanimationiteration",
     "onanimationstart",
```

  
#### 145.0.7561.2 (`2025-12-5`) 
No browser API changes.

  
#### 144.0.7559.3 (`2025-12-3`) ⚡
Added 27 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_144.0.7534.0_to_144.0.7559.3.diff), [json](./browser_apis/chrome-unstable_144.0.7534.0_to_144.0.7559.3.json), [full list](./browser_apis/chrome-unstable_144.0.7559.3.json))
 ```diff
--- ./browser_apis/chrome-unstable_144.0.7534.0.json	2025-12-03 22:00:51.452920700 +0000
+++ ./browser_apis/chrome-unstable_144.0.7559.3.json	2025-12-03 22:04:50.138311605 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9096,
+  "browserApiCount": 9123,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -2267,6 +2267,21 @@
     "HTMLFrameSetElement.prototype.onunhandledrejection",
     "HTMLFrameSetElement.prototype.onunload",
     "HTMLFrameSetElement.prototype.rows",
+    "HTMLGeolocationElement",
+    "HTMLGeolocationElement.prototype",
+    "HTMLGeolocationElement.prototype.accuracymode",
+    "HTMLGeolocationElement.prototype.autolocate",
+    "HTMLGeolocationElement.prototype.error",
+    "HTMLGeolocationElement.prototype.initialPermissionStatus",
+    "HTMLGeolocationElement.prototype.invalidReason",
+    "HTMLGeolocationElement.prototype.isValid",
+    "HTMLGeolocationElement.prototype.onlocation",
+    "HTMLGeolocationElement.prototype.onpromptaction",
+    "HTMLGeolocationElement.prototype.onpromptdismiss",
+    "HTMLGeolocationElement.prototype.onvalidationstatuschange",
+    "HTMLGeolocationElement.prototype.permissionStatus",
+    "HTMLGeolocationElement.prototype.position",
+    "HTMLGeolocationElement.prototype.watch",
     "HTMLHRElement",
     "HTMLHRElement.prototype",
     "HTMLHRElement.prototype.align",
@@ -4621,6 +4636,7 @@
     "Performance.prototype.getEntries",
     "Performance.prototype.getEntriesByName",
     "Performance.prototype.getEntriesByType",
+    "Performance.prototype.interactionCount",
     "Performance.prototype.mark",
     "Performance.prototype.measure",
     "Performance.prototype.memory",
@@ -7547,6 +7563,8 @@
     "WebAssembly.Memory.prototype",
     "WebAssembly.Memory.prototype.buffer",
     "WebAssembly.Memory.prototype.grow",
+    "WebAssembly.Memory.prototype.toFixedLengthBuffer",
+    "WebAssembly.Memory.prototype.toResizableBuffer",
     "WebAssembly.Module",
     "WebAssembly.Module.customSections",
     "WebAssembly.Module.exports",
@@ -8662,6 +8680,7 @@
     "XRSession.prototype.onsqueezeend",
     "XRSession.prototype.onsqueezestart",
     "XRSession.prototype.onvisibilitychange",
+    "XRSession.prototype.onvisibilitymaskchange",
     "XRSession.prototype.pauseDepthSensing",
     "XRSession.prototype.preferredReflectionFormat",
     "XRSession.prototype.renderState",
@@ -8692,6 +8711,7 @@
     "XRView.prototype",
     "XRView.prototype.camera",
     "XRView.prototype.eye",
+    "XRView.prototype.index",
     "XRView.prototype.isFirstPersonObserver",
     "XRView.prototype.projectionMatrix",
     "XRView.prototype.recommendedViewportScale",
@@ -8706,6 +8726,13 @@
     "XRViewport.prototype.width",
     "XRViewport.prototype.x",
     "XRViewport.prototype.y",
+    "XRVisibilityMaskChangeEvent",
+    "XRVisibilityMaskChangeEvent.prototype",
+    "XRVisibilityMaskChangeEvent.prototype.eye",
+    "XRVisibilityMaskChangeEvent.prototype.index",
+    "XRVisibilityMaskChangeEvent.prototype.indices",
+    "XRVisibilityMaskChangeEvent.prototype.session",
+    "XRVisibilityMaskChangeEvent.prototype.vertices",
     "XRWebGLBinding",
     "XRWebGLBinding.prototype",
     "XRWebGLBinding.prototype.getCameraImage",
```

  
#### 144.0.7534.0 (`2025-11-21`) ⚡
Added 4 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_144.0.7524.0_to_144.0.7534.0.diff), [json](./browser_apis/chrome-unstable_144.0.7524.0_to_144.0.7534.0.json), [full list](./browser_apis/chrome-unstable_144.0.7534.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_144.0.7524.0.json	2025-11-21 18:00:58.819671689 +0000
+++ ./browser_apis/chrome-unstable_144.0.7534.0.json	2025-11-21 18:05:31.115443867 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9092,
+  "browserApiCount": 9096,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -5365,10 +5365,14 @@
     "SVGAElement.prototype",
     "SVGAElement.prototype.download",
     "SVGAElement.prototype.href",
+    "SVGAElement.prototype.hreflang",
     "SVGAElement.prototype.interestForElement",
+    "SVGAElement.prototype.ping",
+    "SVGAElement.prototype.referrerPolicy",
     "SVGAElement.prototype.rel",
     "SVGAElement.prototype.relList",
     "SVGAElement.prototype.target",
+    "SVGAElement.prototype.type",
     "SVGAngle",
     "SVGAngle.prototype",
     "SVGAngle.prototype.convertToSpecifiedUnits",
```

  
#### 144.0.7524.0 (`2025-11-13`) ⚡
Added 250 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_144.0.7512.1_to_144.0.7524.0.diff), [json](./browser_apis/chrome-unstable_144.0.7512.1_to_144.0.7524.0.json), [full list](./browser_apis/chrome-unstable_144.0.7524.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_144.0.7512.1.json	2025-11-13 19:00:45.486186859 +0000
+++ ./browser_apis/chrome-unstable_144.0.7524.0.json	2025-11-13 19:01:12.718694637 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8842,
+  "browserApiCount": 9092,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -983,10 +983,15 @@
     "CharacterBoundsUpdateEvent.prototype.rangeStart",
     "Clipboard",
     "Clipboard.prototype",
+    "Clipboard.prototype.onclipboardchange",
     "Clipboard.prototype.read",
     "Clipboard.prototype.readText",
     "Clipboard.prototype.write",
     "Clipboard.prototype.writeText",
+    "ClipboardChangeEvent",
+    "ClipboardChangeEvent.prototype",
+    "ClipboardChangeEvent.prototype.changeId",
+    "ClipboardChangeEvent.prototype.types",
     "ClipboardEvent",
     "ClipboardEvent.prototype",
     "ClipboardEvent.prototype.clipboardData",
@@ -1280,6 +1285,7 @@
     "Date.prototype.toLocaleString",
     "Date.prototype.toLocaleTimeString",
     "Date.prototype.toString",
+    "Date.prototype.toTemporalInstant",
     "Date.prototype.toTimeString",
     "Date.prototype.toUTCString",
     "Date.prototype.valueOf",
@@ -1525,6 +1531,7 @@
     "File",
     "File.prototype",
     "File.prototype.arrayBuffer",
+    "File.prototype.bytes",
     "File.prototype.constructor",
     "File.prototype.lastModified",
     "File.prototype.lastModifiedDate",
@@ -2931,6 +2938,7 @@
     "IdentityCredentialError",
     "IdentityCredentialError.prototype",
     "IdentityCredentialError.prototype.code",
+    "IdentityCredentialError.prototype.error",
     "IdentityCredentialError.prototype.url",
     "IdentityProvider",
     "IdentityProvider.close",
@@ -6698,6 +6706,248 @@
     "TaskSignal.prototype.priority",
     "TaskSignal.prototype.reason",
     "TaskSignal.prototype.throwIfAborted",
+    "Temporal",
+    "Temporal.Duration",
+    "Temporal.Duration.compare",
+    "Temporal.Duration.from",
+    "Temporal.Duration.prototype",
+    "Temporal.Duration.prototype.abs",
+    "Temporal.Duration.prototype.add",
+    "Temporal.Duration.prototype.blank",
+    "Temporal.Duration.prototype.days",
+    "Temporal.Duration.prototype.hours",
+    "Temporal.Duration.prototype.microseconds",
+    "Temporal.Duration.prototype.milliseconds",
+    "Temporal.Duration.prototype.minutes",
+    "Temporal.Duration.prototype.months",
+    "Temporal.Duration.prototype.nanoseconds",
+    "Temporal.Duration.prototype.negated",
+    "Temporal.Duration.prototype.round",
+    "Temporal.Duration.prototype.seconds",
+    "Temporal.Duration.prototype.sign",
+    "Temporal.Duration.prototype.subtract",
+    "Temporal.Duration.prototype.toJSON",
+    "Temporal.Duration.prototype.toLocaleString",
+    "Temporal.Duration.prototype.toString",
+    "Temporal.Duration.prototype.total",
+    "Temporal.Duration.prototype.valueOf",
+    "Temporal.Duration.prototype.weeks",
+    "Temporal.Duration.prototype.with",
+    "Temporal.Duration.prototype.years",
+    "Temporal.Instant",
+    "Temporal.Instant.compare",
+    "Temporal.Instant.from",
+    "Temporal.Instant.fromEpochMilliseconds",
+    "Temporal.Instant.fromEpochNanoseconds",
+    "Temporal.Instant.prototype",
+    "Temporal.Instant.prototype.add",
+    "Temporal.Instant.prototype.epochMilliseconds",
+    "Temporal.Instant.prototype.epochNanoseconds",
+    "Temporal.Instant.prototype.equals",
+    "Temporal.Instant.prototype.round",
+    "Temporal.Instant.prototype.since",
+    "Temporal.Instant.prototype.subtract",
+    "Temporal.Instant.prototype.toJSON",
+    "Temporal.Instant.prototype.toLocaleString",
+    "Temporal.Instant.prototype.toString",
+    "Temporal.Instant.prototype.toZonedDateTimeISO",
+    "Temporal.Instant.prototype.until",
+    "Temporal.Instant.prototype.valueOf",
+    "Temporal.Now",
+    "Temporal.Now.instant",
+    "Temporal.Now.plainDateISO",
+    "Temporal.Now.plainDateTimeISO",
+    "Temporal.Now.plainTimeISO",
+    "Temporal.Now.timeZoneId",
+    "Temporal.Now.zonedDateTimeISO",
+    "Temporal.PlainDate",
+    "Temporal.PlainDate.compare",
+    "Temporal.PlainDate.from",
+    "Temporal.PlainDate.prototype",
+    "Temporal.PlainDate.prototype.add",
+    "Temporal.PlainDate.prototype.calendarId",
+    "Temporal.PlainDate.prototype.day",
+    "Temporal.PlainDate.prototype.dayOfWeek",
+    "Temporal.PlainDate.prototype.dayOfYear",
+    "Temporal.PlainDate.prototype.daysInMonth",
+    "Temporal.PlainDate.prototype.daysInWeek",
+    "Temporal.PlainDate.prototype.daysInYear",
+    "Temporal.PlainDate.prototype.equals",
+    "Temporal.PlainDate.prototype.era",
+    "Temporal.PlainDate.prototype.eraYear",
+    "Temporal.PlainDate.prototype.inLeapYear",
+    "Temporal.PlainDate.prototype.month",
+    "Temporal.PlainDate.prototype.monthCode",
+    "Temporal.PlainDate.prototype.monthsInYear",
+    "Temporal.PlainDate.prototype.since",
+    "Temporal.PlainDate.prototype.subtract",
+    "Temporal.PlainDate.prototype.toJSON",
+    "Temporal.PlainDate.prototype.toLocaleString",
+    "Temporal.PlainDate.prototype.toPlainDateTime",
+    "Temporal.PlainDate.prototype.toPlainMonthDay",
+    "Temporal.PlainDate.prototype.toPlainYearMonth",
+    "Temporal.PlainDate.prototype.toString",
+    "Temporal.PlainDate.prototype.toZonedDateTime",
+    "Temporal.PlainDate.prototype.until",
+    "Temporal.PlainDate.prototype.valueOf",
+    "Temporal.PlainDate.prototype.weekOfYear",
+    "Temporal.PlainDate.prototype.with",
+    "Temporal.PlainDate.prototype.withCalendar",
+    "Temporal.PlainDate.prototype.year",
+    "Temporal.PlainDate.prototype.yearOfWeek",
+    "Temporal.PlainDateTime",
+    "Temporal.PlainDateTime.compare",
+    "Temporal.PlainDateTime.from",
+    "Temporal.PlainDateTime.prototype",
+    "Temporal.PlainDateTime.prototype.add",
+    "Temporal.PlainDateTime.prototype.calendarId",
+    "Temporal.PlainDateTime.prototype.day",
+    "Temporal.PlainDateTime.prototype.dayOfWeek",
+    "Temporal.PlainDateTime.prototype.dayOfYear",
+    "Temporal.PlainDateTime.prototype.daysInMonth",
+    "Temporal.PlainDateTime.prototype.daysInWeek",
+    "Temporal.PlainDateTime.prototype.daysInYear",
+    "Temporal.PlainDateTime.prototype.equals",
+    "Temporal.PlainDateTime.prototype.era",
+    "Temporal.PlainDateTime.prototype.eraYear",
+    "Temporal.PlainDateTime.prototype.hour",
+    "Temporal.PlainDateTime.prototype.inLeapYear",
+    "Temporal.PlainDateTime.prototype.microsecond",
+    "Temporal.PlainDateTime.prototype.millisecond",
+    "Temporal.PlainDateTime.prototype.minute",
+    "Temporal.PlainDateTime.prototype.month",
+    "Temporal.PlainDateTime.prototype.monthCode",
+    "Temporal.PlainDateTime.prototype.monthsInYear",
+    "Temporal.PlainDateTime.prototype.nanosecond",
+    "Temporal.PlainDateTime.prototype.round",
+    "Temporal.PlainDateTime.prototype.second",
+    "Temporal.PlainDateTime.prototype.since",
+    "Temporal.PlainDateTime.prototype.subtract",
+    "Temporal.PlainDateTime.prototype.toJSON",
+    "Temporal.PlainDateTime.prototype.toLocaleString",
+    "Temporal.PlainDateTime.prototype.toPlainDate",
+    "Temporal.PlainDateTime.prototype.toPlainTime",
+    "Temporal.PlainDateTime.prototype.toString",
+    "Temporal.PlainDateTime.prototype.toZonedDateTime",
+    "Temporal.PlainDateTime.prototype.until",
+    "Temporal.PlainDateTime.prototype.valueOf",
+    "Temporal.PlainDateTime.prototype.weekOfYear",
+    "Temporal.PlainDateTime.prototype.with",
+    "Temporal.PlainDateTime.prototype.withCalendar",
+    "Temporal.PlainDateTime.prototype.withPlainTime",
+    "Temporal.PlainDateTime.prototype.year",
+    "Temporal.PlainDateTime.prototype.yearOfWeek",
+    "Temporal.PlainMonthDay",
+    "Temporal.PlainMonthDay.from",
+    "Temporal.PlainMonthDay.prototype",
+    "Temporal.PlainMonthDay.prototype.calendarId",
+    "Temporal.PlainMonthDay.prototype.day",
+    "Temporal.PlainMonthDay.prototype.equals",
+    "Temporal.PlainMonthDay.prototype.monthCode",
+    "Temporal.PlainMonthDay.prototype.toJSON",
+    "Temporal.PlainMonthDay.prototype.toLocaleString",
+    "Temporal.PlainMonthDay.prototype.toPlainDate",
+    "Temporal.PlainMonthDay.prototype.toString",
+    "Temporal.PlainMonthDay.prototype.valueOf",
+    "Temporal.PlainMonthDay.prototype.with",
+    "Temporal.PlainTime",
+    "Temporal.PlainTime.compare",
+    "Temporal.PlainTime.from",
+    "Temporal.PlainTime.prototype",
+    "Temporal.PlainTime.prototype.add",
+    "Temporal.PlainTime.prototype.equals",
+    "Temporal.PlainTime.prototype.hour",
+    "Temporal.PlainTime.prototype.microsecond",
+    "Temporal.PlainTime.prototype.millisecond",
+    "Temporal.PlainTime.prototype.minute",
+    "Temporal.PlainTime.prototype.nanosecond",
+    "Temporal.PlainTime.prototype.round",
+    "Temporal.PlainTime.prototype.second",
+    "Temporal.PlainTime.prototype.since",
+    "Temporal.PlainTime.prototype.subtract",
+    "Temporal.PlainTime.prototype.toJSON",
+    "Temporal.PlainTime.prototype.toLocaleString",
+    "Temporal.PlainTime.prototype.toString",
+    "Temporal.PlainTime.prototype.until",
+    "Temporal.PlainTime.prototype.valueOf",
+    "Temporal.PlainTime.prototype.with",
+    "Temporal.PlainYearMonth",
+    "Temporal.PlainYearMonth.compare",
+    "Temporal.PlainYearMonth.from",
+    "Temporal.PlainYearMonth.prototype",
+    "Temporal.PlainYearMonth.prototype.add",
+    "Temporal.PlainYearMonth.prototype.calendarId",
+    "Temporal.PlainYearMonth.prototype.daysInMonth",
+    "Temporal.PlainYearMonth.prototype.daysInYear",
+    "Temporal.PlainYearMonth.prototype.equals",
+    "Temporal.PlainYearMonth.prototype.era",
+    "Temporal.PlainYearMonth.prototype.eraYear",
+    "Temporal.PlainYearMonth.prototype.inLeapYear",
+    "Temporal.PlainYearMonth.prototype.month",
+    "Temporal.PlainYearMonth.prototype.monthCode",
+    "Temporal.PlainYearMonth.prototype.monthsInYear",
+    "Temporal.PlainYearMonth.prototype.since",
+    "Temporal.PlainYearMonth.prototype.subtract",
+    "Temporal.PlainYearMonth.prototype.toJSON",
+    "Temporal.PlainYearMonth.prototype.toLocaleString",
+    "Temporal.PlainYearMonth.prototype.toPlainDate",
+    "Temporal.PlainYearMonth.prototype.toString",
+    "Temporal.PlainYearMonth.prototype.until",
+    "Temporal.PlainYearMonth.prototype.valueOf",
+    "Temporal.PlainYearMonth.prototype.with",
+    "Temporal.PlainYearMonth.prototype.year",
+    "Temporal.ZonedDateTime",
+    "Temporal.ZonedDateTime.compare",
+    "Temporal.ZonedDateTime.from",
+    "Temporal.ZonedDateTime.prototype",
+    "Temporal.ZonedDateTime.prototype.add",
+    "Temporal.ZonedDateTime.prototype.calendarId",
+    "Temporal.ZonedDateTime.prototype.day",
+    "Temporal.ZonedDateTime.prototype.dayOfWeek",
+    "Temporal.ZonedDateTime.prototype.dayOfYear",
+    "Temporal.ZonedDateTime.prototype.daysInMonth",
+    "Temporal.ZonedDateTime.prototype.daysInWeek",
+    "Temporal.ZonedDateTime.prototype.daysInYear",
+    "Temporal.ZonedDateTime.prototype.epochMilliseconds",
+    "Temporal.ZonedDateTime.prototype.epochNanoseconds",
+    "Temporal.ZonedDateTime.prototype.equals",
+    "Temporal.ZonedDateTime.prototype.era",
+    "Temporal.ZonedDateTime.prototype.eraYear",
+    "Temporal.ZonedDateTime.prototype.getTimeZoneTransition",
+    "Temporal.ZonedDateTime.prototype.hour",
+    "Temporal.ZonedDateTime.prototype.hoursInDay",
+    "Temporal.ZonedDateTime.prototype.inLeapYear",
+    "Temporal.ZonedDateTime.prototype.microsecond",
+    "Temporal.ZonedDateTime.prototype.millisecond",
+    "Temporal.ZonedDateTime.prototype.minute",
+    "Temporal.ZonedDateTime.prototype.month",
+    "Temporal.ZonedDateTime.prototype.monthCode",
+    "Temporal.ZonedDateTime.prototype.monthsInYear",
+    "Temporal.ZonedDateTime.prototype.nanosecond",
+    "Temporal.ZonedDateTime.prototype.offset",
+    "Temporal.ZonedDateTime.prototype.offsetNanoseconds",
+    "Temporal.ZonedDateTime.prototype.round",
+    "Temporal.ZonedDateTime.prototype.second",
+    "Temporal.ZonedDateTime.prototype.since",
+    "Temporal.ZonedDateTime.prototype.startOfDay",
+    "Temporal.ZonedDateTime.prototype.subtract",
+    "Temporal.ZonedDateTime.prototype.timeZoneId",
+    "Temporal.ZonedDateTime.prototype.toInstant",
+    "Temporal.ZonedDateTime.prototype.toJSON",
+    "Temporal.ZonedDateTime.prototype.toLocaleString",
+    "Temporal.ZonedDateTime.prototype.toPlainDate",
+    "Temporal.ZonedDateTime.prototype.toPlainDateTime",
+    "Temporal.ZonedDateTime.prototype.toPlainTime",
+    "Temporal.ZonedDateTime.prototype.toString",
+    "Temporal.ZonedDateTime.prototype.until",
+    "Temporal.ZonedDateTime.prototype.valueOf",
+    "Temporal.ZonedDateTime.prototype.weekOfYear",
+    "Temporal.ZonedDateTime.prototype.with",
+    "Temporal.ZonedDateTime.prototype.withCalendar",
+    "Temporal.ZonedDateTime.prototype.withPlainTime",
+    "Temporal.ZonedDateTime.prototype.withTimeZone",
+    "Temporal.ZonedDateTime.prototype.year",
+    "Temporal.ZonedDateTime.prototype.yearOfWeek",
     "Text",
     "Text.prototype",
     "Text.prototype.after",
```

  
#### 144.0.7512.1 (`2025-11-7`) ⚡
Added 1 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_144.0.7500.2_to_144.0.7512.1.diff), [json](./browser_apis/chrome-unstable_144.0.7500.2_to_144.0.7512.1.json), [full list](./browser_apis/chrome-unstable_144.0.7512.1.json))
 ```diff
--- ./browser_apis/chrome-unstable_144.0.7500.2.json	2025-11-07 19:00:55.614984883 +0000
+++ ./browser_apis/chrome-unstable_144.0.7512.1.json	2025-11-07 19:01:28.585191609 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8841,
+  "browserApiCount": 8842,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -7184,6 +7184,7 @@
     "ViewTransition.prototype.skipTransition",
     "ViewTransition.prototype.types",
     "ViewTransition.prototype.updateCallbackDone",
+    "ViewTransition.prototype.waitUntil",
     "ViewTransitionTypeSet",
     "ViewTransitionTypeSet.prototype",
     "ViewTransitionTypeSet.prototype.add",
```

  
#### 144.0.7500.2 (`2025-10-30`) ⚡
Added 8 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_143.0.7489.0_to_144.0.7500.2.diff), [json](./browser_apis/chrome-unstable_143.0.7489.0_to_144.0.7500.2.json), [full list](./browser_apis/chrome-unstable_144.0.7500.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_143.0.7489.0.json	2025-10-30 21:01:00.457924511 +0000
+++ ./browser_apis/chrome-unstable_144.0.7500.2.json	2025-10-30 21:02:02.323699251 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8833,
+  "browserApiCount": 8841,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -2079,6 +2079,8 @@
     "HTMLBodyElement.prototype.onblur",
     "HTMLBodyElement.prototype.onerror",
     "HTMLBodyElement.prototype.onfocus",
+    "HTMLBodyElement.prototype.ongamepadconnected",
+    "HTMLBodyElement.prototype.ongamepaddisconnected",
     "HTMLBodyElement.prototype.onhashchange",
     "HTMLBodyElement.prototype.onlanguagechange",
     "HTMLBodyElement.prototype.onload",
@@ -2239,6 +2241,8 @@
     "HTMLFrameSetElement.prototype.onblur",
     "HTMLFrameSetElement.prototype.onerror",
     "HTMLFrameSetElement.prototype.onfocus",
+    "HTMLFrameSetElement.prototype.ongamepadconnected",
+    "HTMLFrameSetElement.prototype.ongamepaddisconnected",
     "HTMLFrameSetElement.prototype.onhashchange",
     "HTMLFrameSetElement.prototype.onlanguagechange",
     "HTMLFrameSetElement.prototype.onload",
@@ -4695,6 +4699,7 @@
     "PerformanceResourceTiming.prototype",
     "PerformanceResourceTiming.prototype.connectEnd",
     "PerformanceResourceTiming.prototype.connectStart",
+    "PerformanceResourceTiming.prototype.contentEncoding",
     "PerformanceResourceTiming.prototype.decodedBodySize",
     "PerformanceResourceTiming.prototype.deliveryType",
     "PerformanceResourceTiming.prototype.domainLookupEnd",
@@ -7831,6 +7836,7 @@
     "WebTransport.prototype.datagrams",
     "WebTransport.prototype.incomingBidirectionalStreams",
     "WebTransport.prototype.incomingUnidirectionalStreams",
+    "WebTransport.prototype.protocol",
     "WebTransport.prototype.ready",
     "WebTransportBidirectionalStream",
     "WebTransportBidirectionalStream.prototype",
@@ -8615,6 +8621,8 @@
     "onerror",
     "onfocus",
     "onformdata",
+    "ongamepadconnected",
+    "ongamepaddisconnected",
     "ongotpointercapture",
     "onhashchange",
     "oninput",
```

  
#### 143.0.7489.0 (`2025-10-24`) 
No browser API changes.

  
#### 143.0.7475.7 (`2025-10-17`) ⚡
Added 0 APIs, removed 7 (see: [diff](./browser_apis/chrome-unstable_143.0.7461.2_to_143.0.7475.7.diff), [json](./browser_apis/chrome-unstable_143.0.7461.2_to_143.0.7475.7.json), [full list](./browser_apis/chrome-unstable_143.0.7475.7.json))
 ```diff
--- ./browser_apis/chrome-unstable_143.0.7461.2.json	2025-10-17 18:00:53.210926048 +0000
+++ ./browser_apis/chrome-unstable_143.0.7475.7.json	2025-10-17 18:01:27.361196366 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 8840,
+  "browserApiCount": 8833,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -3117,10 +3117,8 @@
     "Intl.Locale.prototype",
     "Intl.Locale.prototype.baseName",
     "Intl.Locale.prototype.calendar",
-    "Intl.Locale.prototype.calendars",
     "Intl.Locale.prototype.caseFirst",
     "Intl.Locale.prototype.collation",
-    "Intl.Locale.prototype.collations",
     "Intl.Locale.prototype.firstDayOfWeek",
     "Intl.Locale.prototype.getCalendars",
     "Intl.Locale.prototype.getCollations",
@@ -3130,19 +3128,14 @@
     "Intl.Locale.prototype.getTimeZones",
     "Intl.Locale.prototype.getWeekInfo",
     "Intl.Locale.prototype.hourCycle",
-    "Intl.Locale.prototype.hourCycles",
     "Intl.Locale.prototype.language",
     "Intl.Locale.prototype.maximize",
     "Intl.Locale.prototype.minimize",
     "Intl.Locale.prototype.numberingSystem",
-    "Intl.Locale.prototype.numberingSystems",
     "Intl.Locale.prototype.numeric",
     "Intl.Locale.prototype.region",
     "Intl.Locale.prototype.script",
-    "Intl.Locale.prototype.textInfo",
-    "Intl.Locale.prototype.timeZones",
     "Intl.Locale.prototype.toString",
-    "Intl.Locale.prototype.weekInfo",
     "Intl.NumberFormat",
     "Intl.NumberFormat.prototype",
     "Intl.NumberFormat.prototype.format",
```

  
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

  <!-- browserapis:end -->
