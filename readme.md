# WIP

## Browser APIs

<!-- browserapis:start -->
### chrome-stable
  
#### 150.0.7871.46 (`2026-6-30`) ⚡
Added 25 APIs, removed 0 (see: [diff](./browser_apis/chrome-stable_149.0.7827.200_to_150.0.7871.46.diff), [json](./browser_apis/chrome-stable_149.0.7827.200_to_150.0.7871.46.json), [full list](./browser_apis/chrome-stable_150.0.7871.46.json))
 ```diff
--- ./browser_apis/chrome-stable_149.0.7827.200.json	2026-06-30 21:28:27.433822522 +0000
+++ ./browser_apis/chrome-stable_150.0.7871.46.json	2026-06-30 21:29:24.230965444 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 9343,
+  "browserApiCount": 9368,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -509,6 +509,7 @@
     "CSSAnimation.prototype.animationName",
     "CSSContainerRule",
     "CSSContainerRule.prototype",
+    "CSSContainerRule.prototype.conditions",
     "CSSContainerRule.prototype.containerName",
     "CSSContainerRule.prototype.containerQuery",
     "CSSCounterStyleRule",
@@ -1766,6 +1767,7 @@
     "GPUComputePassEncoder.prototype.popDebugGroup",
     "GPUComputePassEncoder.prototype.pushDebugGroup",
     "GPUComputePassEncoder.prototype.setBindGroup",
+    "GPUComputePassEncoder.prototype.setImmediates",
     "GPUComputePassEncoder.prototype.setPipeline",
     "GPUComputePassEncoder.prototype.writeTimestamp",
     "GPUComputePipeline",
@@ -1849,6 +1851,7 @@
     "GPURenderBundleEncoder.prototype.popDebugGroup",
     "GPURenderBundleEncoder.prototype.pushDebugGroup",
     "GPURenderBundleEncoder.prototype.setBindGroup",
+    "GPURenderBundleEncoder.prototype.setImmediates",
     "GPURenderBundleEncoder.prototype.setIndexBuffer",
     "GPURenderBundleEncoder.prototype.setPipeline",
     "GPURenderBundleEncoder.prototype.setVertexBuffer",
@@ -1868,6 +1871,7 @@
     "GPURenderPassEncoder.prototype.pushDebugGroup",
     "GPURenderPassEncoder.prototype.setBindGroup",
     "GPURenderPassEncoder.prototype.setBlendConstant",
+    "GPURenderPassEncoder.prototype.setImmediates",
     "GPURenderPassEncoder.prototype.setIndexBuffer",
     "GPURenderPassEncoder.prototype.setPipeline",
     "GPURenderPassEncoder.prototype.setScissorRect",
@@ -1911,6 +1915,7 @@
     "GPUSupportedLimits.prototype.maxComputeWorkgroupsPerDimension",
     "GPUSupportedLimits.prototype.maxDynamicStorageBuffersPerPipelineLayout",
     "GPUSupportedLimits.prototype.maxDynamicUniformBuffersPerPipelineLayout",
+    "GPUSupportedLimits.prototype.maxImmediateSize",
     "GPUSupportedLimits.prototype.maxInterStageShaderVariables",
     "GPUSupportedLimits.prototype.maxSampledTexturesPerShaderStage",
     "GPUSupportedLimits.prototype.maxSamplersPerShaderStage",
@@ -2735,6 +2740,7 @@
     "HTMLTemplateElement",
     "HTMLTemplateElement.prototype",
     "HTMLTemplateElement.prototype.content",
+    "HTMLTemplateElement.prototype.htmlFor",
     "HTMLTemplateElement.prototype.shadowRootClonable",
     "HTMLTemplateElement.prototype.shadowRootCustomElementRegistry",
     "HTMLTemplateElement.prototype.shadowRootDelegatesFocus",
@@ -3472,6 +3478,8 @@
     "MathMLElement.prototype.blur",
     "MathMLElement.prototype.dataset",
     "MathMLElement.prototype.focus",
+    "MathMLElement.prototype.focusGroup",
+    "MathMLElement.prototype.focusGroupStart",
     "MathMLElement.prototype.nonce",
     "MathMLElement.prototype.onabort",
     "MathMLElement.prototype.onanimationcancel",
@@ -3757,7 +3765,9 @@
     "MediaStreamTrackGenerator.prototype.writable",
     "MediaStreamTrackProcessor",
     "MediaStreamTrackProcessor.prototype",
+    "MediaStreamTrackProcessor.prototype.discardedFrames",
     "MediaStreamTrackProcessor.prototype.readable",
+    "MediaStreamTrackProcessor.prototype.totalFrames",
     "MediaStreamTrackVideoStats",
     "MediaStreamTrackVideoStats.prototype",
     "MediaStreamTrackVideoStats.prototype.deliveredFrames",
@@ -4373,6 +4383,8 @@
     "Option.prototype.constructor.prototype.enterKeyHint",
     "Option.prototype.constructor.prototype.firstElementChild",
     "Option.prototype.constructor.prototype.focus",
+    "Option.prototype.constructor.prototype.focusGroup",
+    "Option.prototype.constructor.prototype.focusGroupStart",
     "Option.prototype.constructor.prototype.getAnimations",
     "Option.prototype.constructor.prototype.getAttribute",
     "Option.prototype.constructor.prototype.getAttributeNS",
@@ -4996,8 +5008,15 @@
     "PressureRecord.prototype.toJSON",
     "ProcessingInstruction",
     "ProcessingInstruction.prototype",
+    "ProcessingInstruction.prototype.getAttribute",
+    "ProcessingInstruction.prototype.getAttributeNames",
+    "ProcessingInstruction.prototype.hasAttribute",
+    "ProcessingInstruction.prototype.hasAttributes",
+    "ProcessingInstruction.prototype.removeAttribute",
+    "ProcessingInstruction.prototype.setAttribute",
     "ProcessingInstruction.prototype.sheet",
     "ProcessingInstruction.prototype.target",
+    "ProcessingInstruction.prototype.toggleAttribute",
     "Profiler",
     "Profiler.prototype",
     "Profiler.prototype.sampleInterval",
@@ -5415,6 +5434,7 @@
     "Request.prototype.headers",
     "Request.prototype.integrity",
     "Request.prototype.isHistoryNavigation",
+    "Request.prototype.isReloadNavigation",
     "Request.prototype.json",
     "Request.prototype.keepalive",
     "Request.prototype.method",
@@ -6145,6 +6165,8 @@
     "SVGViewElement.prototype.constructor",
     "SVGViewElement.prototype.dataset",
     "SVGViewElement.prototype.focus",
+    "SVGViewElement.prototype.focusGroup",
+    "SVGViewElement.prototype.focusGroupStart",
     "SVGViewElement.prototype.nonce",
     "SVGViewElement.prototype.onabort",
     "SVGViewElement.prototype.onanimationcancel",
@@ -6259,9 +6281,11 @@
     "Sanitizer.prototype",
     "Sanitizer.prototype.allowAttribute",
     "Sanitizer.prototype.allowElement",
+    "Sanitizer.prototype.allowProcessingInstruction",
     "Sanitizer.prototype.get",
     "Sanitizer.prototype.removeAttribute",
     "Sanitizer.prototype.removeElement",
+    "Sanitizer.prototype.removeProcessingInstruction",
     "Sanitizer.prototype.removeUnsafe",
     "Sanitizer.prototype.replaceElementWithChildren",
     "Sanitizer.prototype.setComments",
@@ -6556,6 +6580,7 @@
     "SpeechRecognition.prototype.onstart",
     "SpeechRecognition.prototype.phrases",
     "SpeechRecognition.prototype.processLocally",
+    "SpeechRecognition.prototype.quality",
     "SpeechRecognition.prototype.start",
     "SpeechRecognition.prototype.stop",
     "SpeechRecognitionErrorEvent",
```

  
#### 149.0.7827.200 (`2026-6-25`) 
No browser API changes.

  
#### 149.0.7827.196 (`2026-6-23`) 
No browser API changes.

  
#### 149.0.7827.155 (`2026-6-16`) 
No browser API changes.

  
#### 149.0.7827.114 (`2026-6-11`) 
No browser API changes.

  
#### 149.0.7827.102 (`2026-6-8`) 
No browser API changes.

  
#### 149.0.7827.53 (`2026-6-2`) ⚡
Added 29 APIs, removed 18 (see: [diff](./browser_apis/chrome-stable_148.0.7778.215_to_149.0.7827.53.diff), [json](./browser_apis/chrome-stable_148.0.7778.215_to_149.0.7827.53.json), [full list](./browser_apis/chrome-stable_149.0.7827.53.json))
 ```diff
--- ./browser_apis/chrome-stable_148.0.7778.215.json	2026-06-02 20:57:53.276504794 +0000
+++ ./browser_apis/chrome-stable_149.0.7827.53.json	2026-06-02 20:58:34.821405987 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 9332,
+  "browserApiCount": 9343,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -39,6 +39,7 @@
     "AnimationEvent.prototype.animationName",
     "AnimationEvent.prototype.elapsedTime",
     "AnimationEvent.prototype.pseudoElement",
+    "AnimationEvent.prototype.pseudoTarget",
     "AnimationPlaybackEvent",
     "AnimationPlaybackEvent.prototype",
     "AnimationPlaybackEvent.prototype.currentTime",
@@ -721,6 +722,12 @@
     "CSSPropertyRule.prototype.initialValue",
     "CSSPropertyRule.prototype.name",
     "CSSPropertyRule.prototype.syntax",
+    "CSSPseudoElement",
+    "CSSPseudoElement.prototype",
+    "CSSPseudoElement.prototype.element",
+    "CSSPseudoElement.prototype.parent",
+    "CSSPseudoElement.prototype.pseudo",
+    "CSSPseudoElement.prototype.type",
     "CSSRotate",
     "CSSRotate.prototype",
     "CSSRotate.prototype.angle",
@@ -3195,6 +3202,7 @@
     "Intl.Locale.prototype.region",
     "Intl.Locale.prototype.script",
     "Intl.Locale.prototype.toString",
+    "Intl.Locale.prototype.variants",
     "Intl.NumberFormat",
     "Intl.NumberFormat.prototype",
     "Intl.NumberFormat.prototype.format",
@@ -4522,6 +4530,7 @@
     "Option.prototype.constructor.prototype.prefix",
     "Option.prototype.constructor.prototype.prepend",
     "Option.prototype.constructor.prototype.previousElementSibling",
+    "Option.prototype.constructor.prototype.pseudo",
     "Option.prototype.constructor.prototype.querySelector",
     "Option.prototype.constructor.prototype.querySelectorAll",
     "Option.prototype.constructor.prototype.releasePointerCapture",
@@ -7227,6 +7236,7 @@
     "TransitionEvent.prototype.elapsedTime",
     "TransitionEvent.prototype.propertyName",
     "TransitionEvent.prototype.pseudoElement",
+    "TransitionEvent.prototype.pseudoTarget",
     "Translator",
     "Translator.availability",
     "Translator.create",
@@ -8249,27 +8259,10 @@
     "WheelEvent.prototype.clientY",
     "WheelEvent.prototype.constructor",
     "WheelEvent.prototype.constructor.prototype",
-    "WheelEvent.prototype.constructor.prototype.bubbles",
-    "WheelEvent.prototype.constructor.prototype.cancelBubble",
-    "WheelEvent.prototype.constructor.prototype.cancelable",
-    "WheelEvent.prototype.constructor.prototype.composed",
-    "WheelEvent.prototype.constructor.prototype.composedPath",
-    "WheelEvent.prototype.constructor.prototype.constructor",
-    "WheelEvent.prototype.constructor.prototype.currentTarget",
-    "WheelEvent.prototype.constructor.prototype.defaultPrevented",
     "WheelEvent.prototype.constructor.prototype.detail",
-    "WheelEvent.prototype.constructor.prototype.eventPhase",
-    "WheelEvent.prototype.constructor.prototype.initEvent",
     "WheelEvent.prototype.constructor.prototype.initUIEvent",
-    "WheelEvent.prototype.constructor.prototype.preventDefault",
-    "WheelEvent.prototype.constructor.prototype.returnValue",
+    "WheelEvent.prototype.constructor.prototype.pseudoTarget",
     "WheelEvent.prototype.constructor.prototype.sourceCapabilities",
-    "WheelEvent.prototype.constructor.prototype.srcElement",
-    "WheelEvent.prototype.constructor.prototype.stopImmediatePropagation",
-    "WheelEvent.prototype.constructor.prototype.stopPropagation",
-    "WheelEvent.prototype.constructor.prototype.target",
-    "WheelEvent.prototype.constructor.prototype.timeStamp",
-    "WheelEvent.prototype.constructor.prototype.type",
     "WheelEvent.prototype.constructor.prototype.view",
     "WheelEvent.prototype.constructor.prototype.which",
     "WheelEvent.prototype.ctrlKey",
@@ -8308,7 +8301,25 @@
     "WindowControlsOverlay.prototype.visible",
     "WindowControlsOverlayGeometryChangeEvent",
     "WindowControlsOverlayGeometryChangeEvent.prototype",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.bubbles",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.cancelBubble",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.cancelable",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.composed",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.composedPath",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.constructor",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.currentTarget",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.defaultPrevented",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.eventPhase",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.initEvent",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.preventDefault",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.returnValue",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.srcElement",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.stopImmediatePropagation",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.stopPropagation",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.target",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.timeStamp",
     "WindowControlsOverlayGeometryChangeEvent.prototype.titlebarAreaRect",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.type",
     "WindowControlsOverlayGeometryChangeEvent.prototype.visible",
     "Worker",
     "Worker.prototype",
```

  
#### 148.0.7778.215 (`2026-5-27`) 
No browser API changes.

  
#### 148.0.7778.178 (`2026-5-19`) 
No browser API changes.

  
#### 148.0.7778.167 (`2026-5-12`) 
No browser API changes.

  
#### 148.0.7778.96 (`2026-5-5`) ⚡
Added 18 APIs, removed 1 (see: [diff](./browser_apis/chrome-stable_147.0.7727.137_to_148.0.7778.96.diff), [json](./browser_apis/chrome-stable_147.0.7727.137_to_148.0.7778.96.json), [full list](./browser_apis/chrome-stable_148.0.7778.96.json))
 ```diff
--- ./browser_apis/chrome-stable_147.0.7727.137.json	2026-05-05 20:19:13.216100976 +0000
+++ ./browser_apis/chrome-stable_148.0.7778.96.json	2026-05-05 20:19:55.938322731 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 9315,
+  "browserApiCount": 9332,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -156,6 +156,7 @@
     "Audio.prototype.constructor.prototype.ended",
     "Audio.prototype.constructor.prototype.error",
     "Audio.prototype.constructor.prototype.load",
+    "Audio.prototype.constructor.prototype.loading",
     "Audio.prototype.constructor.prototype.loop",
     "Audio.prototype.constructor.prototype.mediaKeys",
     "Audio.prototype.constructor.prototype.muted",
@@ -1081,6 +1082,7 @@
     "CreateMonitor.prototype",
     "CreateMonitor.prototype.ondownloadprogress",
     "Credential",
+    "Credential.isConditionalMediationAvailable",
     "Credential.prototype",
     "Credential.prototype.id",
     "Credential.prototype.type",
@@ -3299,6 +3301,19 @@
     "LanguageDetector.prototype.expectedInputLanguages",
     "LanguageDetector.prototype.inputQuota",
     "LanguageDetector.prototype.measureInputUsage",
+    "LanguageModel",
+    "LanguageModel.availability",
+    "LanguageModel.create",
+    "LanguageModel.prototype",
+    "LanguageModel.prototype.append",
+    "LanguageModel.prototype.clone",
+    "LanguageModel.prototype.contextUsage",
+    "LanguageModel.prototype.contextWindow",
+    "LanguageModel.prototype.destroy",
+    "LanguageModel.prototype.measureContextUsage",
+    "LanguageModel.prototype.oncontextoverflow",
+    "LanguageModel.prototype.prompt",
+    "LanguageModel.prototype.promptStreaming",
     "LargestContentfulPaint",
     "LargestContentfulPaint.prototype",
     "LargestContentfulPaint.prototype.element",
@@ -4647,6 +4662,7 @@
     "PaymentMethodChangeEvent.prototype.methodDetails",
     "PaymentMethodChangeEvent.prototype.methodName",
     "PaymentRequest",
+    "PaymentRequest.getSecurePaymentConfirmationCapabilities",
     "PaymentRequest.prototype",
     "PaymentRequest.prototype.abort",
     "PaymentRequest.prototype.canMakePayment",
@@ -4782,6 +4798,7 @@
     "PerformanceResourceTiming.prototype.connectEnd",
     "PerformanceResourceTiming.prototype.connectStart",
     "PerformanceResourceTiming.prototype.contentEncoding",
+    "PerformanceResourceTiming.prototype.contentType",
     "PerformanceResourceTiming.prototype.decodedBodySize",
     "PerformanceResourceTiming.prototype.deliveryType",
     "PerformanceResourceTiming.prototype.domainLookupEnd",
@@ -6449,7 +6466,6 @@
     "SharedStorage.prototype.clear",
     "SharedStorage.prototype.createWorklet",
     "SharedStorage.prototype.delete",
-    "SharedStorage.prototype.get",
     "SharedStorage.prototype.run",
     "SharedStorage.prototype.selectURL",
     "SharedStorage.prototype.set",
@@ -7644,6 +7660,7 @@
     "WebAssembly.Exception.prototype",
     "WebAssembly.Exception.prototype.getArg",
     "WebAssembly.Exception.prototype.is",
+    "WebAssembly.Exception.prototype.stack",
     "WebAssembly.Global",
     "WebAssembly.Global.prototype",
     "WebAssembly.Global.prototype.value",
```

  
#### 147.0.7727.137 (`2026-4-28`) 
No browser API changes.

  
#### 147.0.7727.116 (`2026-4-22`) 
No browser API changes.

  
#### 147.0.7727.101 (`2026-4-15`) 
No browser API changes.

  
#### 147.0.7727.55 (`2026-4-7`) ⚡
Added 96 APIs, removed 0 (see: [diff](./browser_apis/chrome-stable_146.0.7680.177_to_147.0.7727.55.diff), [json](./browser_apis/chrome-stable_146.0.7680.177_to_147.0.7727.55.json), [full list](./browser_apis/chrome-stable_147.0.7727.55.json))
 ```diff
--- ./browser_apis/chrome-stable_146.0.7680.177.json	2026-04-07 19:22:19.173538600 +0000
+++ ./browser_apis/chrome-stable_147.0.7727.55.json	2026-04-07 19:22:44.857011884 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 9219,
+  "browserApiCount": 9315,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -3438,6 +3438,7 @@
     "Math.sin",
     "Math.sinh",
     "Math.sqrt",
+    "Math.sumPrecise",
     "Math.tan",
     "Math.tanh",
     "Math.trunc",
@@ -4226,6 +4227,7 @@
     "Option.prototype.constructor",
     "Option.prototype.constructor.prototype",
     "Option.prototype.constructor.prototype.accessKey",
+    "Option.prototype.constructor.prototype.activeViewTransition",
     "Option.prototype.constructor.prototype.after",
     "Option.prototype.constructor.prototype.animate",
     "Option.prototype.constructor.prototype.append",
@@ -4537,6 +4539,7 @@
     "Option.prototype.constructor.prototype.showPopover",
     "Option.prototype.constructor.prototype.slot",
     "Option.prototype.constructor.prototype.spellcheck",
+    "Option.prototype.constructor.prototype.startViewTransition",
     "Option.prototype.constructor.prototype.style",
     "Option.prototype.constructor.prototype.tabIndex",
     "Option.prototype.constructor.prototype.tagName",
@@ -7541,6 +7544,7 @@
     "ViewTransition.prototype.finished",
     "ViewTransition.prototype.ready",
     "ViewTransition.prototype.skipTransition",
+    "ViewTransition.prototype.transitionRoot",
     "ViewTransition.prototype.types",
     "ViewTransition.prototype.updateCallbackDone",
     "ViewTransition.prototype.waitUntil",
@@ -8658,12 +8662,44 @@
     "XRCamera.prototype",
     "XRCamera.prototype.height",
     "XRCamera.prototype.width",
+    "XRCompositionLayer",
+    "XRCompositionLayer.prototype",
+    "XRCompositionLayer.prototype.blendTextureSourceAlpha",
+    "XRCompositionLayer.prototype.destroy",
+    "XRCompositionLayer.prototype.forceMonoPresentation",
+    "XRCompositionLayer.prototype.layout",
+    "XRCompositionLayer.prototype.mipLevels",
+    "XRCompositionLayer.prototype.needsRedraw",
+    "XRCompositionLayer.prototype.opacity",
+    "XRCubeLayer",
+    "XRCubeLayer.prototype",
+    "XRCubeLayer.prototype.onredraw",
+    "XRCubeLayer.prototype.orientation",
+    "XRCubeLayer.prototype.space",
+    "XRCylinderLayer",
+    "XRCylinderLayer.prototype",
+    "XRCylinderLayer.prototype.aspectRatio",
+    "XRCylinderLayer.prototype.centralAngle",
+    "XRCylinderLayer.prototype.onredraw",
+    "XRCylinderLayer.prototype.radius",
+    "XRCylinderLayer.prototype.space",
+    "XRCylinderLayer.prototype.transform",
     "XRDOMOverlayState",
     "XRDOMOverlayState.prototype",
     "XRDOMOverlayState.prototype.type",
+    "XREquirectLayer",
+    "XREquirectLayer.prototype",
+    "XREquirectLayer.prototype.centralHorizontalAngle",
+    "XREquirectLayer.prototype.lowerVerticalAngle",
+    "XREquirectLayer.prototype.onredraw",
+    "XREquirectLayer.prototype.radius",
+    "XREquirectLayer.prototype.space",
+    "XREquirectLayer.prototype.transform",
+    "XREquirectLayer.prototype.upperVerticalAngle",
     "XRFrame",
     "XRFrame.prototype",
     "XRFrame.prototype.createAnchor",
+    "XRFrame.prototype.detectedPlanes",
     "XRFrame.prototype.fillJointRadii",
     "XRFrame.prototype.fillPoses",
     "XRFrame.prototype.getDepthInformation",
@@ -8722,6 +8758,9 @@
     "XRJointSpace.prototype.jointName",
     "XRLayer",
     "XRLayer.prototype",
+    "XRLayerEvent",
+    "XRLayerEvent.prototype",
+    "XRLayerEvent.prototype.layer",
     "XRLightEstimate",
     "XRLightEstimate.prototype",
     "XRLightEstimate.prototype.primaryLightDirection",
@@ -8731,6 +8770,36 @@
     "XRLightProbe.prototype",
     "XRLightProbe.prototype.onreflectionchange",
     "XRLightProbe.prototype.probeSpace",
+    "XRPlane",
+    "XRPlane.prototype",
+    "XRPlane.prototype.lastChangedTime",
+    "XRPlane.prototype.orientation",
+    "XRPlane.prototype.planeSpace",
+    "XRPlane.prototype.polygon",
+    "XRPlane.prototype.semanticLabel",
+    "XRPlaneSet",
+    "XRPlaneSet.prototype",
+    "XRPlaneSet.prototype.entries",
+    "XRPlaneSet.prototype.forEach",
+    "XRPlaneSet.prototype.has",
+    "XRPlaneSet.prototype.keys",
+    "XRPlaneSet.prototype.size",
+    "XRPlaneSet.prototype.values",
+    "XRProjectionLayer",
+    "XRProjectionLayer.prototype",
+    "XRProjectionLayer.prototype.deltaPose",
+    "XRProjectionLayer.prototype.fixedFoveation",
+    "XRProjectionLayer.prototype.ignoreDepthValues",
+    "XRProjectionLayer.prototype.textureArrayLength",
+    "XRProjectionLayer.prototype.textureHeight",
+    "XRProjectionLayer.prototype.textureWidth",
+    "XRQuadLayer",
+    "XRQuadLayer.prototype",
+    "XRQuadLayer.prototype.height",
+    "XRQuadLayer.prototype.onredraw",
+    "XRQuadLayer.prototype.space",
+    "XRQuadLayer.prototype.transform",
+    "XRQuadLayer.prototype.width",
     "XRRay",
     "XRRay.prototype",
     "XRRay.prototype.direction",
@@ -8746,6 +8815,7 @@
     "XRRenderState.prototype.depthFar",
     "XRRenderState.prototype.depthNear",
     "XRRenderState.prototype.inlineVerticalFieldOfView",
+    "XRRenderState.prototype.layers",
     "XRRigidTransform",
     "XRRigidTransform.prototype",
     "XRRigidTransform.prototype.inverse",
@@ -8763,8 +8833,10 @@
     "XRSession.prototype.enabledFeatures",
     "XRSession.prototype.end",
     "XRSession.prototype.environmentBlendMode",
+    "XRSession.prototype.initiateRoomCapture",
     "XRSession.prototype.inputSources",
     "XRSession.prototype.interactionMode",
+    "XRSession.prototype.maxRenderLayers",
     "XRSession.prototype.onend",
     "XRSession.prototype.oninputsourceschange",
     "XRSession.prototype.onselect",
@@ -8789,6 +8861,9 @@
     "XRSessionEvent",
     "XRSessionEvent.prototype",
     "XRSessionEvent.prototype.session",
+    "XRSubImage",
+    "XRSubImage.prototype",
+    "XRSubImage.prototype.viewport",
     "XRSystem",
     "XRSystem.prototype",
     "XRSystem.prototype.isSessionSupported",
@@ -8829,9 +8904,18 @@
     "XRVisibilityMaskChangeEvent.prototype.vertices",
     "XRWebGLBinding",
     "XRWebGLBinding.prototype",
+    "XRWebGLBinding.prototype.createCubeLayer",
+    "XRWebGLBinding.prototype.createCylinderLayer",
+    "XRWebGLBinding.prototype.createEquirectLayer",
+    "XRWebGLBinding.prototype.createProjectionLayer",
+    "XRWebGLBinding.prototype.createQuadLayer",
     "XRWebGLBinding.prototype.getCameraImage",
     "XRWebGLBinding.prototype.getDepthInformation",
     "XRWebGLBinding.prototype.getReflectionCubeMap",
+    "XRWebGLBinding.prototype.getSubImage",
+    "XRWebGLBinding.prototype.getViewSubImage",
+    "XRWebGLBinding.prototype.nativeProjectionScaleFactor",
+    "XRWebGLBinding.prototype.usesDepthValues",
     "XRWebGLDepthInformation",
     "XRWebGLDepthInformation.prototype",
     "XRWebGLDepthInformation.prototype.texture",
@@ -8844,6 +8928,18 @@
     "XRWebGLLayer.prototype.framebufferWidth",
     "XRWebGLLayer.prototype.getViewport",
     "XRWebGLLayer.prototype.ignoreDepthValues",
+    "XRWebGLSubImage",
+    "XRWebGLSubImage.prototype",
+    "XRWebGLSubImage.prototype.colorTexture",
+    "XRWebGLSubImage.prototype.colorTextureHeight",
+    "XRWebGLSubImage.prototype.colorTextureWidth",
+    "XRWebGLSubImage.prototype.depthStencilTexture",
+    "XRWebGLSubImage.prototype.depthStencilTextureHeight",
+    "XRWebGLSubImage.prototype.depthStencilTextureWidth",
+    "XRWebGLSubImage.prototype.imageIndex",
+    "XRWebGLSubImage.prototype.motionVectorTexture",
+    "XRWebGLSubImage.prototype.motionVectorTextureHeight",
+    "XRWebGLSubImage.prototype.motionVectorTextureWidth",
     "XSLTProcessor",
     "XSLTProcessor.prototype",
     "XSLTProcessor.prototype.clearParameters",
```

  
#### 146.0.7680.177 (`2026-3-31`) 
No browser API changes.

  
#### 146.0.7680.164 (`2026-3-23`) 
No browser API changes.

  
#### 146.0.7680.153 (`2026-3-18`) 
No browser API changes.

  
#### 146.0.7680.80 (`2026-3-14`) 
No browser API changes.

  
#### 146.0.7680.75 (`2026-3-12`) 
No browser API changes.

  
#### 146.0.7680.71 (`2026-3-10`) ⚡
Added 56 APIs, removed 0 (see: [diff](./browser_apis/chrome-stable_145.0.7632.159_to_146.0.7680.71.diff), [json](./browser_apis/chrome-stable_145.0.7632.159_to_146.0.7680.71.json), [full list](./browser_apis/chrome-stable_146.0.7680.71.json))
 ```diff
--- ./browser_apis/chrome-stable_145.0.7632.159.json	2026-03-10 19:13:07.065564293 +0000
+++ ./browser_apis/chrome-stable_146.0.7680.71.json	2026-03-10 19:13:34.058568328 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 9163,
+  "browserApiCount": 9219,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -43,6 +43,11 @@
     "AnimationPlaybackEvent.prototype",
     "AnimationPlaybackEvent.prototype.currentTime",
     "AnimationPlaybackEvent.prototype.timelineTime",
+    "AnimationTrigger",
+    "AnimationTrigger.prototype",
+    "AnimationTrigger.prototype.addAnimation",
+    "AnimationTrigger.prototype.getAnimations",
+    "AnimationTrigger.prototype.removeAnimation",
     "Array",
     "Array.from",
     "Array.fromAsync",
@@ -206,6 +211,7 @@
     "AudioContext.prototype.onerror",
     "AudioContext.prototype.onsinkchange",
     "AudioContext.prototype.outputLatency",
+    "AudioContext.prototype.playbackStats",
     "AudioContext.prototype.resume",
     "AudioContext.prototype.setSinkId",
     "AudioContext.prototype.sinkId",
@@ -283,6 +289,16 @@
     "AudioParamMap.prototype.keys",
     "AudioParamMap.prototype.size",
     "AudioParamMap.prototype.values",
+    "AudioPlaybackStats",
+    "AudioPlaybackStats.prototype",
+    "AudioPlaybackStats.prototype.averageLatency",
+    "AudioPlaybackStats.prototype.maximumLatency",
+    "AudioPlaybackStats.prototype.minimumLatency",
+    "AudioPlaybackStats.prototype.resetLatency",
+    "AudioPlaybackStats.prototype.toJSON",
+    "AudioPlaybackStats.prototype.totalDuration",
+    "AudioPlaybackStats.prototype.underrunDuration",
+    "AudioPlaybackStats.prototype.underrunEvents",
     "AudioProcessingEvent",
     "AudioProcessingEvent.prototype",
     "AudioProcessingEvent.prototype.inputBuffer",
@@ -1093,6 +1109,7 @@
     "CustomElementRegistry.prototype.define",
     "CustomElementRegistry.prototype.get",
     "CustomElementRegistry.prototype.getName",
+    "CustomElementRegistry.prototype.initialize",
     "CustomElementRegistry.prototype.upgrade",
     "CustomElementRegistry.prototype.whenDefined",
     "CustomEvent",
@@ -1889,7 +1906,11 @@
     "GPUSupportedLimits.prototype.maxSampledTexturesPerShaderStage",
     "GPUSupportedLimits.prototype.maxSamplersPerShaderStage",
     "GPUSupportedLimits.prototype.maxStorageBufferBindingSize",
+    "GPUSupportedLimits.prototype.maxStorageBuffersInFragmentStage",
+    "GPUSupportedLimits.prototype.maxStorageBuffersInVertexStage",
     "GPUSupportedLimits.prototype.maxStorageBuffersPerShaderStage",
+    "GPUSupportedLimits.prototype.maxStorageTexturesInFragmentStage",
+    "GPUSupportedLimits.prototype.maxStorageTexturesInVertexStage",
     "GPUSupportedLimits.prototype.maxStorageTexturesPerShaderStage",
     "GPUSupportedLimits.prototype.maxTextureArrayLayers",
     "GPUSupportedLimits.prototype.maxTextureDimension1D",
@@ -1913,6 +1934,7 @@
     "GPUTexture.prototype.label",
     "GPUTexture.prototype.mipLevelCount",
     "GPUTexture.prototype.sampleCount",
+    "GPUTexture.prototype.textureBindingViewDimension",
     "GPUTexture.prototype.usage",
     "GPUTexture.prototype.width",
     "GPUTextureUsage",
@@ -2705,6 +2727,7 @@
     "HTMLTemplateElement.prototype",
     "HTMLTemplateElement.prototype.content",
     "HTMLTemplateElement.prototype.shadowRootClonable",
+    "HTMLTemplateElement.prototype.shadowRootCustomElementRegistry",
     "HTMLTemplateElement.prototype.shadowRootDelegatesFocus",
     "HTMLTemplateElement.prototype.shadowRootMode",
     "HTMLTemplateElement.prototype.shadowRootSerializable",
@@ -3207,6 +3230,7 @@
     "Intl.v8BreakIterator.prototype.resolvedOptions",
     "Intl.v8BreakIterator.supportedLocalesOf",
     "Iterator",
+    "Iterator.concat",
     "Iterator.from",
     "Iterator.prototype",
     "Iterator.prototype.constructor",
@@ -3829,6 +3853,7 @@
     "NavigationHistoryEntry.prototype.url",
     "NavigationPrecommitController",
     "NavigationPrecommitController.prototype",
+    "NavigationPrecommitController.prototype.addHandler",
     "NavigationPrecommitController.prototype.redirect",
     "NavigationPreloadManager",
     "NavigationPreloadManager.prototype",
@@ -4314,6 +4339,7 @@
     "Option.prototype.constructor.prototype.constructor.prototype.when",
     "Option.prototype.constructor.prototype.contentEditable",
     "Option.prototype.constructor.prototype.currentCSSZoom",
+    "Option.prototype.constructor.prototype.customElementRegistry",
     "Option.prototype.constructor.prototype.dataset",
     "Option.prototype.constructor.prototype.dir",
     "Option.prototype.constructor.prototype.draggable",
@@ -4504,6 +4530,7 @@
     "Option.prototype.constructor.prototype.setAttributeNS",
     "Option.prototype.constructor.prototype.setAttributeNode",
     "Option.prototype.constructor.prototype.setAttributeNodeNS",
+    "Option.prototype.constructor.prototype.setHTML",
     "Option.prototype.constructor.prototype.setHTMLUnsafe",
     "Option.prototype.constructor.prototype.setPointerCapture",
     "Option.prototype.constructor.prototype.shadowRoot",
@@ -6199,6 +6226,17 @@
     "SVGViewElement.prototype.viewBox",
     "SVGViewElement.prototype.viewportElement",
     "SVGViewElement.prototype.zoomAndPan",
+    "Sanitizer",
+    "Sanitizer.prototype",
+    "Sanitizer.prototype.allowAttribute",
+    "Sanitizer.prototype.allowElement",
+    "Sanitizer.prototype.get",
+    "Sanitizer.prototype.removeAttribute",
+    "Sanitizer.prototype.removeElement",
+    "Sanitizer.prototype.removeUnsafe",
+    "Sanitizer.prototype.replaceElementWithChildren",
+    "Sanitizer.prototype.setComments",
+    "Sanitizer.prototype.setDataAttributes",
     "Scheduler",
     "Scheduler.prototype",
     "Scheduler.prototype.postTask",
@@ -6374,6 +6412,7 @@
     "ShadowRoot.prototype.children",
     "ShadowRoot.prototype.clonable",
     "ShadowRoot.prototype.constructor",
+    "ShadowRoot.prototype.customElementRegistry",
     "ShadowRoot.prototype.delegatesFocus",
     "ShadowRoot.prototype.elementFromPoint",
     "ShadowRoot.prototype.elementsFromPoint",
@@ -6396,6 +6435,7 @@
     "ShadowRoot.prototype.querySelectorAll",
     "ShadowRoot.prototype.replaceChildren",
     "ShadowRoot.prototype.serializable",
+    "ShadowRoot.prototype.setHTML",
     "ShadowRoot.prototype.setHTMLUnsafe",
     "ShadowRoot.prototype.slotAssignment",
     "ShadowRoot.prototype.styleSheets",
@@ -7104,6 +7144,20 @@
     "TimeRanges.prototype.end",
     "TimeRanges.prototype.length",
     "TimeRanges.prototype.start",
+    "TimelineTrigger",
+    "TimelineTrigger.prototype",
+    "TimelineTrigger.prototype.ranges",
+    "TimelineTriggerRange",
+    "TimelineTriggerRange.prototype",
+    "TimelineTriggerRange.prototype.activationRangeEnd",
+    "TimelineTriggerRange.prototype.activationRangeStart",
+    "TimelineTriggerRange.prototype.activeRangeEnd",
+    "TimelineTriggerRange.prototype.activeRangeStart",
+    "TimelineTriggerRange.prototype.timeline",
+    "TimelineTriggerRangeList",
+    "TimelineTriggerRangeList.prototype",
+    "TimelineTriggerRangeList.prototype.item",
+    "TimelineTriggerRangeList.prototype.length",
     "ToggleEvent",
     "ToggleEvent.prototype",
     "ToggleEvent.prototype.newState",
@@ -8287,6 +8341,7 @@
     "XMLDocument.prototype.close",
     "XMLDocument.prototype.compatMode",
     "XMLDocument.prototype.constructor",
+    "XMLDocument.prototype.constructor.parseHTML",
     "XMLDocument.prototype.constructor.parseHTMLUnsafe",
     "XMLDocument.prototype.contentType",
     "XMLDocument.prototype.cookie",
@@ -8306,6 +8361,7 @@
     "XMLDocument.prototype.createTextNode",
     "XMLDocument.prototype.createTreeWalker",
     "XMLDocument.prototype.currentScript",
+    "XMLDocument.prototype.customElementRegistry",
     "XMLDocument.prototype.defaultView",
     "XMLDocument.prototype.designMode",
     "XMLDocument.prototype.dir",
```

  
#### 145.0.7632.159 (`2026-3-3`) 
No browser API changes.

  
#### 145.0.7632.116 (`2026-2-23`) 
No browser API changes.

  
#### 145.0.7632.109 (`2026-2-18`) 
No browser API changes.

  
#### 145.0.7632.75 (`2026-2-13`) 
No browser API changes.

  
#### 145.0.7632.67 (`2026-2-12`) 
No browser API changes.

  
#### 145.0.7632.45 (`2026-2-10`) ⚡
Added 40 APIs, removed 0 (see: [diff](./browser_apis/chrome-stable_144.0.7559.132_to_145.0.7632.45.diff), [json](./browser_apis/chrome-stable_144.0.7559.132_to_145.0.7632.45.json), [full list](./browser_apis/chrome-stable_145.0.7632.45.json))
 ```diff
--- ./browser_apis/chrome-stable_144.0.7559.132.json	2026-02-10 22:10:19.680763842 +0000
+++ ./browser_apis/chrome-stable_145.0.7632.45.json	2026-02-10 22:10:47.316737352 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-stable",
-  "browserApiCount": 9123,
+  "browserApiCount": 9163,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -1056,6 +1056,11 @@
     "CountQueuingStrategy.prototype",
     "CountQueuingStrategy.prototype.highWaterMark",
     "CountQueuingStrategy.prototype.size",
+    "CrashReportContext",
+    "CrashReportContext.prototype",
+    "CrashReportContext.prototype.delete",
+    "CrashReportContext.prototype.initialize",
+    "CrashReportContext.prototype.set",
     "CreateMonitor",
     "CreateMonitor.prototype",
     "CreateMonitor.prototype.ondownloadprogress",
@@ -2560,11 +2565,13 @@
     "HTMLScriptElement.prototype.event",
     "HTMLScriptElement.prototype.fetchPriority",
     "HTMLScriptElement.prototype.htmlFor",
+    "HTMLScriptElement.prototype.innerText",
     "HTMLScriptElement.prototype.integrity",
     "HTMLScriptElement.prototype.noModule",
     "HTMLScriptElement.prototype.referrerPolicy",
     "HTMLScriptElement.prototype.src",
     "HTMLScriptElement.prototype.text",
+    "HTMLScriptElement.prototype.textContent",
     "HTMLScriptElement.prototype.type",
     "HTMLScriptElement.supports",
     "HTMLSelectElement",
@@ -3273,6 +3280,8 @@
     "LargestContentfulPaint.prototype.element",
     "LargestContentfulPaint.prototype.id",
     "LargestContentfulPaint.prototype.loadTime",
+    "LargestContentfulPaint.prototype.paintTime",
+    "LargestContentfulPaint.prototype.presentationTime",
     "LargestContentfulPaint.prototype.renderTime",
     "LargestContentfulPaint.prototype.size",
     "LargestContentfulPaint.prototype.toJSON",
@@ -3364,6 +3373,8 @@
     "Map.prototype.entries",
     "Map.prototype.forEach",
     "Map.prototype.get",
+    "Map.prototype.getOrInsert",
+    "Map.prototype.getOrInsertComputed",
     "Map.prototype.has",
     "Map.prototype.keys",
     "Map.prototype.set",
@@ -3415,6 +3426,7 @@
     "MathMLElement.prototype.focus",
     "MathMLElement.prototype.nonce",
     "MathMLElement.prototype.onabort",
+    "MathMLElement.prototype.onanimationcancel",
     "MathMLElement.prototype.onanimationend",
     "MathMLElement.prototype.onanimationiteration",
     "MathMLElement.prototype.onanimationstart",
@@ -3830,6 +3842,7 @@
     "NavigationTransition.prototype.finished",
     "NavigationTransition.prototype.from",
     "NavigationTransition.prototype.navigationType",
+    "NavigationTransition.prototype.to",
     "Navigator",
     "Navigator.prototype",
     "Navigator.prototype.adAuctionComponents",
@@ -4350,6 +4363,7 @@
     "Option.prototype.constructor.prototype.offsetTop",
     "Option.prototype.constructor.prototype.offsetWidth",
     "Option.prototype.constructor.prototype.onabort",
+    "Option.prototype.constructor.prototype.onanimationcancel",
     "Option.prototype.constructor.prototype.onanimationend",
     "Option.prototype.constructor.prototype.onanimationiteration",
     "Option.prototype.constructor.prototype.onanimationstart",
@@ -4516,6 +4530,12 @@
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
@@ -4656,6 +4676,8 @@
     "PerformanceElementTiming.prototype.loadTime",
     "PerformanceElementTiming.prototype.naturalHeight",
     "PerformanceElementTiming.prototype.naturalWidth",
+    "PerformanceElementTiming.prototype.paintTime",
+    "PerformanceElementTiming.prototype.presentationTime",
     "PerformanceElementTiming.prototype.renderTime",
     "PerformanceElementTiming.prototype.toJSON",
     "PerformanceElementTiming.prototype.url",
@@ -4671,6 +4693,8 @@
     "PerformanceLongAnimationFrameTiming.prototype",
     "PerformanceLongAnimationFrameTiming.prototype.blockingDuration",
     "PerformanceLongAnimationFrameTiming.prototype.firstUIEventTimestamp",
+    "PerformanceLongAnimationFrameTiming.prototype.paintTime",
+    "PerformanceLongAnimationFrameTiming.prototype.presentationTime",
     "PerformanceLongAnimationFrameTiming.prototype.renderStart",
     "PerformanceLongAnimationFrameTiming.prototype.scripts",
     "PerformanceLongAnimationFrameTiming.prototype.styleAndLayoutStart",
@@ -4693,6 +4717,7 @@
     "PerformanceNavigationTiming",
     "PerformanceNavigationTiming.prototype",
     "PerformanceNavigationTiming.prototype.activationStart",
+    "PerformanceNavigationTiming.prototype.confidence",
     "PerformanceNavigationTiming.prototype.criticalCHRestart",
     "PerformanceNavigationTiming.prototype.domComplete",
     "PerformanceNavigationTiming.prototype.domContentLoadedEventEnd",
@@ -4719,6 +4744,9 @@
     "PerformanceObserverEntryList.prototype.getEntriesByType",
     "PerformancePaintTiming",
     "PerformancePaintTiming.prototype",
+    "PerformancePaintTiming.prototype.paintTime",
+    "PerformancePaintTiming.prototype.presentationTime",
+    "PerformancePaintTiming.prototype.toJSON",
     "PerformanceResourceTiming",
     "PerformanceResourceTiming.prototype",
     "PerformanceResourceTiming.prototype.connectEnd",
@@ -4793,6 +4821,11 @@
     "PerformanceTiming.prototype.toJSON",
     "PerformanceTiming.prototype.unloadEventEnd",
     "PerformanceTiming.prototype.unloadEventStart",
+    "PerformanceTimingConfidence",
+    "PerformanceTimingConfidence.prototype",
+    "PerformanceTimingConfidence.prototype.randomizedTriggerRate",
+    "PerformanceTimingConfidence.prototype.toJSON",
+    "PerformanceTimingConfidence.prototype.value",
     "PeriodicSyncManager",
     "PeriodicSyncManager.prototype",
     "PeriodicSyncManager.prototype.getTags",
@@ -6058,6 +6091,7 @@
     "SVGViewElement.prototype.focus",
     "SVGViewElement.prototype.nonce",
     "SVGViewElement.prototype.onabort",
+    "SVGViewElement.prototype.onanimationcancel",
     "SVGViewElement.prototype.onanimationend",
     "SVGViewElement.prototype.onanimationiteration",
     "SVGViewElement.prototype.onanimationstart",
@@ -7427,6 +7461,7 @@
     "VideoFrame.prototype.duration",
     "VideoFrame.prototype.flip",
     "VideoFrame.prototype.format",
+    "VideoFrame.prototype.metadata",
     "VideoFrame.prototype.rotation",
     "VideoFrame.prototype.timestamp",
     "VideoFrame.prototype.visibleRect",
@@ -7532,6 +7567,8 @@
     "WeakMap.prototype",
     "WeakMap.prototype.delete",
     "WeakMap.prototype.get",
+    "WeakMap.prototype.getOrInsert",
+    "WeakMap.prototype.getOrInsertComputed",
     "WeakMap.prototype.has",
     "WeakMap.prototype.set",
     "WeakRef",
@@ -8317,6 +8354,7 @@
     "XMLDocument.prototype.links",
     "XMLDocument.prototype.moveBefore",
     "XMLDocument.prototype.onabort",
+    "XMLDocument.prototype.onanimationcancel",
     "XMLDocument.prototype.onanimationend",
     "XMLDocument.prototype.onanimationiteration",
     "XMLDocument.prototype.onanimationstart",
@@ -8813,6 +8851,7 @@
     "console.trace",
     "console.warn",
     "cookieStore",
+    "crashReport",
     "createImageBitmap",
     "credentialless",
     "crossOriginIsolated",
@@ -8861,6 +8900,7 @@
     "offscreenBuffering",
     "onabort",
     "onafterprint",
+    "onanimationcancel",
     "onanimationend",
     "onanimationiteration",
     "onanimationstart",
```

  
#### 144.0.7559.132 (`2026-2-3`) 
No browser API changes.

  
#### 144.0.7559.109 (`2026-1-27`) 
No browser API changes.

  
#### 144.0.7559.96 (`2026-1-20`) 
No browser API changes.

  
### chrome-unstable
  
#### 152.0.7928.2 (`2026-7-6`) ⚡
Added 17 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_151.0.7912.0_to_152.0.7928.2.diff), [json](./browser_apis/chrome-unstable_151.0.7912.0_to_152.0.7928.2.json), [full list](./browser_apis/chrome-unstable_152.0.7928.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_151.0.7912.0.json	2026-07-06 14:50:36.607117354 +0000
+++ ./browser_apis/chrome-unstable_152.0.7928.2.json	2026-07-06 14:51:11.252650639 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9403,
+  "browserApiCount": 9420,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -36,6 +36,7 @@
     "AnalyserNode.prototype.smoothingTimeConstant",
     "AnimationEvent",
     "AnimationEvent.prototype",
+    "AnimationEvent.prototype.animation",
     "AnimationEvent.prototype.animationName",
     "AnimationEvent.prototype.elapsedTime",
     "AnimationEvent.prototype.pseudoElement",
@@ -3157,6 +3158,13 @@
     "IntegrityViolationReportBody.prototype.documentURL",
     "IntegrityViolationReportBody.prototype.reportOnly",
     "IntegrityViolationReportBody.prototype.toJSON",
+    "InteractionContentfulPaint",
+    "InteractionContentfulPaint.prototype",
+    "InteractionContentfulPaint.prototype.interactionId",
+    "InteractionContentfulPaint.prototype.largestContentfulPaint",
+    "InteractionContentfulPaint.prototype.paintTime",
+    "InteractionContentfulPaint.prototype.presentationTime",
+    "InteractionContentfulPaint.prototype.toJSON",
     "InterestEvent",
     "InterestEvent.prototype",
     "InterestEvent.prototype.source",
@@ -4894,6 +4902,13 @@
     "PerformanceServerTiming.prototype.duration",
     "PerformanceServerTiming.prototype.name",
     "PerformanceServerTiming.prototype.toJSON",
+    "PerformanceSoftNavigation",
+    "PerformanceSoftNavigation.prototype",
+    "PerformanceSoftNavigation.prototype.getLargestInteractionContentfulPaint",
+    "PerformanceSoftNavigation.prototype.interactionId",
+    "PerformanceSoftNavigation.prototype.navigationType",
+    "PerformanceSoftNavigation.prototype.paintTime",
+    "PerformanceSoftNavigation.prototype.presentationTime",
     "PerformanceTiming",
     "PerformanceTiming.prototype",
     "PerformanceTiming.prototype.connectEnd",
@@ -7290,6 +7305,7 @@
     "TransformStreamDefaultController.prototype.terminate",
     "TransitionEvent",
     "TransitionEvent.prototype",
+    "TransitionEvent.prototype.animation",
     "TransitionEvent.prototype.elapsedTime",
     "TransitionEvent.prototype.propertyName",
     "TransitionEvent.prototype.pseudoElement",
@@ -7660,6 +7676,7 @@
     "VisibilityStateEntry.prototype.duration",
     "VisibilityStateEntry.prototype.entryType",
     "VisibilityStateEntry.prototype.name",
+    "VisibilityStateEntry.prototype.navigationId",
     "VisibilityStateEntry.prototype.startTime",
     "VisibilityStateEntry.prototype.toJSON",
     "VisualViewport",
```

  
#### 151.0.7912.0 (`2026-6-26`) ⚡
Added 29 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_151.0.7896.2_to_151.0.7912.0.diff), [json](./browser_apis/chrome-unstable_151.0.7896.2_to_151.0.7912.0.json), [full list](./browser_apis/chrome-unstable_151.0.7912.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_151.0.7896.2.json	2026-06-26 15:41:46.511602233 +0000
+++ ./browser_apis/chrome-unstable_151.0.7912.0.json	2026-06-26 15:42:24.290554530 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9374,
+  "browserApiCount": 9403,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -1422,6 +1422,7 @@
     "EditContext.prototype.updateText",
     "ElementInternals",
     "ElementInternals.prototype",
+    "ElementInternals.prototype.ariaActionsElements",
     "ElementInternals.prototype.ariaActiveDescendantElement",
     "ElementInternals.prototype.ariaAtomic",
     "ElementInternals.prototype.ariaAutoComplete",
@@ -1664,6 +1665,24 @@
     "FontFace.prototype.variant",
     "FontFace.prototype.variationSettings",
     "FontFace.prototype.weight",
+    "FontFaceSet",
+    "FontFaceSet.prototype",
+    "FontFaceSet.prototype.add",
+    "FontFaceSet.prototype.check",
+    "FontFaceSet.prototype.clear",
+    "FontFaceSet.prototype.delete",
+    "FontFaceSet.prototype.entries",
+    "FontFaceSet.prototype.forEach",
+    "FontFaceSet.prototype.has",
+    "FontFaceSet.prototype.keys",
+    "FontFaceSet.prototype.load",
+    "FontFaceSet.prototype.onloading",
+    "FontFaceSet.prototype.onloadingdone",
+    "FontFaceSet.prototype.onloadingerror",
+    "FontFaceSet.prototype.ready",
+    "FontFaceSet.prototype.size",
+    "FontFaceSet.prototype.status",
+    "FontFaceSet.prototype.values",
     "FontFaceSetLoadEvent",
     "FontFaceSetLoadEvent.prototype",
     "FontFaceSetLoadEvent.prototype.fontfaces",
@@ -2800,6 +2819,14 @@
     "HTMLUListElement.prototype.type",
     "HTMLUnknownElement",
     "HTMLUnknownElement.prototype",
+    "HTMLUserMediaElement",
+    "HTMLUserMediaElement.prototype",
+    "HTMLUserMediaElement.prototype.error",
+    "HTMLUserMediaElement.prototype.oncancel",
+    "HTMLUserMediaElement.prototype.onerror",
+    "HTMLUserMediaElement.prototype.onstream",
+    "HTMLUserMediaElement.prototype.setConstraints",
+    "HTMLUserMediaElement.prototype.stream",
     "HTMLVideoElement",
     "HTMLVideoElement.prototype",
     "HTMLVideoElement.prototype.cancelVideoFrameCallback",
@@ -4265,6 +4292,7 @@
     "Option.prototype.constructor.prototype.after",
     "Option.prototype.constructor.prototype.animate",
     "Option.prototype.constructor.prototype.append",
+    "Option.prototype.constructor.prototype.ariaActionsElements",
     "Option.prototype.constructor.prototype.ariaActiveDescendantElement",
     "Option.prototype.constructor.prototype.ariaAtomic",
     "Option.prototype.constructor.prototype.ariaAutoComplete",
@@ -8307,6 +8335,7 @@
     "WheelEvent.prototype.layerX",
     "WheelEvent.prototype.layerY",
     "WheelEvent.prototype.metaKey",
+    "WheelEvent.prototype.momentum",
     "WheelEvent.prototype.movementX",
     "WheelEvent.prototype.movementY",
     "WheelEvent.prototype.offsetX",
```

  
#### 151.0.7896.2 (`2026-6-18`) ⚡
Added 6 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_151.0.7886.2_to_151.0.7896.2.diff), [json](./browser_apis/chrome-unstable_151.0.7886.2_to_151.0.7896.2.json), [full list](./browser_apis/chrome-unstable_151.0.7896.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_151.0.7886.2.json	2026-06-18 15:14:20.758982399 +0000
+++ ./browser_apis/chrome-unstable_151.0.7896.2.json	2026-06-18 15:14:47.635622655 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9368,
+  "browserApiCount": 9374,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -1572,6 +1572,7 @@
     "File.prototype.slice",
     "File.prototype.stream",
     "File.prototype.text",
+    "File.prototype.textStream",
     "File.prototype.type",
     "File.prototype.webkitRelativePath",
     "FileList",
@@ -3765,7 +3766,9 @@
     "MediaStreamTrackGenerator.prototype.writable",
     "MediaStreamTrackProcessor",
     "MediaStreamTrackProcessor.prototype",
+    "MediaStreamTrackProcessor.prototype.discardedFrames",
     "MediaStreamTrackProcessor.prototype.readable",
+    "MediaStreamTrackProcessor.prototype.totalFrames",
     "MediaStreamTrackVideoStats",
     "MediaStreamTrackVideoStats.prototype",
     "MediaStreamTrackVideoStats.prototype.deliveredFrames",
@@ -5443,6 +5446,7 @@
     "Request.prototype.signal",
     "Request.prototype.targetAddressSpace",
     "Request.prototype.text",
+    "Request.prototype.textStream",
     "Request.prototype.url",
     "ResizeObserver",
     "ResizeObserver.prototype",
@@ -5478,6 +5482,7 @@
     "Response.prototype.status",
     "Response.prototype.statusText",
     "Response.prototype.text",
+    "Response.prototype.textStream",
     "Response.prototype.type",
     "Response.prototype.url",
     "Response.redirect",
@@ -6581,6 +6586,7 @@
     "SpeechRecognition.prototype.quality",
     "SpeechRecognition.prototype.start",
     "SpeechRecognition.prototype.stop",
+    "SpeechRecognition.prototype.unspokenPunctuation",
     "SpeechRecognitionErrorEvent",
     "SpeechRecognitionErrorEvent.prototype",
     "SpeechRecognitionErrorEvent.prototype.error",
```

  
#### 151.0.7886.2 (`2026-6-15`) ⚡
Added 6 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_151.0.7872.0_to_151.0.7886.2.diff), [json](./browser_apis/chrome-unstable_151.0.7872.0_to_151.0.7886.2.json), [full list](./browser_apis/chrome-unstable_151.0.7886.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_151.0.7872.0.json	2026-06-15 16:44:12.215318812 +0000
+++ ./browser_apis/chrome-unstable_151.0.7886.2.json	2026-06-15 16:44:41.481572157 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9362,
+  "browserApiCount": 9368,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -1767,6 +1767,7 @@
     "GPUComputePassEncoder.prototype.popDebugGroup",
     "GPUComputePassEncoder.prototype.pushDebugGroup",
     "GPUComputePassEncoder.prototype.setBindGroup",
+    "GPUComputePassEncoder.prototype.setImmediates",
     "GPUComputePassEncoder.prototype.setPipeline",
     "GPUComputePassEncoder.prototype.writeTimestamp",
     "GPUComputePipeline",
@@ -1850,6 +1851,7 @@
     "GPURenderBundleEncoder.prototype.popDebugGroup",
     "GPURenderBundleEncoder.prototype.pushDebugGroup",
     "GPURenderBundleEncoder.prototype.setBindGroup",
+    "GPURenderBundleEncoder.prototype.setImmediates",
     "GPURenderBundleEncoder.prototype.setIndexBuffer",
     "GPURenderBundleEncoder.prototype.setPipeline",
     "GPURenderBundleEncoder.prototype.setVertexBuffer",
@@ -1869,6 +1871,7 @@
     "GPURenderPassEncoder.prototype.pushDebugGroup",
     "GPURenderPassEncoder.prototype.setBindGroup",
     "GPURenderPassEncoder.prototype.setBlendConstant",
+    "GPURenderPassEncoder.prototype.setImmediates",
     "GPURenderPassEncoder.prototype.setIndexBuffer",
     "GPURenderPassEncoder.prototype.setPipeline",
     "GPURenderPassEncoder.prototype.setScissorRect",
@@ -1912,6 +1915,7 @@
     "GPUSupportedLimits.prototype.maxComputeWorkgroupsPerDimension",
     "GPUSupportedLimits.prototype.maxDynamicStorageBuffersPerPipelineLayout",
     "GPUSupportedLimits.prototype.maxDynamicUniformBuffersPerPipelineLayout",
+    "GPUSupportedLimits.prototype.maxImmediateSize",
     "GPUSupportedLimits.prototype.maxInterStageShaderVariables",
     "GPUSupportedLimits.prototype.maxSampledTexturesPerShaderStage",
     "GPUSupportedLimits.prototype.maxSamplersPerShaderStage",
@@ -8260,9 +8264,11 @@
     "WebTransportDatagramDuplexStream.prototype",
     "WebTransportDatagramDuplexStream.prototype.incomingHighWaterMark",
     "WebTransportDatagramDuplexStream.prototype.incomingMaxAge",
+    "WebTransportDatagramDuplexStream.prototype.incomingMaxBufferedDatagrams",
     "WebTransportDatagramDuplexStream.prototype.maxDatagramSize",
     "WebTransportDatagramDuplexStream.prototype.outgoingHighWaterMark",
     "WebTransportDatagramDuplexStream.prototype.outgoingMaxAge",
+    "WebTransportDatagramDuplexStream.prototype.outgoingMaxBufferedDatagrams",
     "WebTransportDatagramDuplexStream.prototype.readable",
     "WebTransportDatagramDuplexStream.prototype.writable",
     "WebTransportError",
```

  
#### 151.0.7872.0 (`2026-6-4`) 
No browser API changes.

  
#### 150.0.7865.2 (`2026-6-1`) ⚡
Added 12 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_150.0.7846.4_to_150.0.7865.2.diff), [json](./browser_apis/chrome-unstable_150.0.7846.4_to_150.0.7865.2.json), [full list](./browser_apis/chrome-unstable_150.0.7865.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_150.0.7846.4.json	2026-06-01 15:58:07.515640708 +0000
+++ ./browser_apis/chrome-unstable_150.0.7865.2.json	2026-06-01 15:58:48.598353503 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9350,
+  "browserApiCount": 9362,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -2736,6 +2736,7 @@
     "HTMLTemplateElement",
     "HTMLTemplateElement.prototype",
     "HTMLTemplateElement.prototype.content",
+    "HTMLTemplateElement.prototype.htmlFor",
     "HTMLTemplateElement.prototype.shadowRootClonable",
     "HTMLTemplateElement.prototype.shadowRootCustomElementRegistry",
     "HTMLTemplateElement.prototype.shadowRootDelegatesFocus",
@@ -5001,8 +5002,15 @@
     "PressureRecord.prototype.toJSON",
     "ProcessingInstruction",
     "ProcessingInstruction.prototype",
+    "ProcessingInstruction.prototype.getAttribute",
+    "ProcessingInstruction.prototype.getAttributeNames",
+    "ProcessingInstruction.prototype.hasAttribute",
+    "ProcessingInstruction.prototype.hasAttributes",
+    "ProcessingInstruction.prototype.removeAttribute",
+    "ProcessingInstruction.prototype.setAttribute",
     "ProcessingInstruction.prototype.sheet",
     "ProcessingInstruction.prototype.target",
+    "ProcessingInstruction.prototype.toggleAttribute",
     "Profiler",
     "Profiler.prototype",
     "Profiler.prototype.sampleInterval",
@@ -5420,6 +5428,7 @@
     "Request.prototype.headers",
     "Request.prototype.integrity",
     "Request.prototype.isHistoryNavigation",
+    "Request.prototype.isReloadNavigation",
     "Request.prototype.json",
     "Request.prototype.keepalive",
     "Request.prototype.method",
@@ -6266,9 +6275,11 @@
     "Sanitizer.prototype",
     "Sanitizer.prototype.allowAttribute",
     "Sanitizer.prototype.allowElement",
+    "Sanitizer.prototype.allowProcessingInstruction",
     "Sanitizer.prototype.get",
     "Sanitizer.prototype.removeAttribute",
     "Sanitizer.prototype.removeElement",
+    "Sanitizer.prototype.removeProcessingInstruction",
     "Sanitizer.prototype.removeUnsafe",
     "Sanitizer.prototype.replaceElementWithChildren",
     "Sanitizer.prototype.setComments",
@@ -6563,6 +6574,7 @@
     "SpeechRecognition.prototype.onstart",
     "SpeechRecognition.prototype.phrases",
     "SpeechRecognition.prototype.processLocally",
+    "SpeechRecognition.prototype.quality",
     "SpeechRecognition.prototype.start",
     "SpeechRecognition.prototype.stop",
     "SpeechRecognitionErrorEvent",
```

  
#### 150.0.7846.4 (`2026-5-21`) 
No browser API changes.

  
#### 150.0.7838.0 (`2026-5-14`) ⚡
Added 7 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_150.0.7828.2_to_150.0.7838.0.diff), [json](./browser_apis/chrome-unstable_150.0.7828.2_to_150.0.7838.0.json), [full list](./browser_apis/chrome-unstable_150.0.7838.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_150.0.7828.2.json	2026-05-14 16:34:49.519330834 +0000
+++ ./browser_apis/chrome-unstable_150.0.7838.0.json	2026-05-14 16:35:19.617980926 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9343,
+  "browserApiCount": 9350,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -509,6 +509,7 @@
     "CSSAnimation.prototype.animationName",
     "CSSContainerRule",
     "CSSContainerRule.prototype",
+    "CSSContainerRule.prototype.conditions",
     "CSSContainerRule.prototype.containerName",
     "CSSContainerRule.prototype.containerQuery",
     "CSSCounterStyleRule",
@@ -3472,6 +3473,8 @@
     "MathMLElement.prototype.blur",
     "MathMLElement.prototype.dataset",
     "MathMLElement.prototype.focus",
+    "MathMLElement.prototype.focusGroup",
+    "MathMLElement.prototype.focusGroupStart",
     "MathMLElement.prototype.nonce",
     "MathMLElement.prototype.onabort",
     "MathMLElement.prototype.onanimationcancel",
@@ -4373,6 +4376,8 @@
     "Option.prototype.constructor.prototype.enterKeyHint",
     "Option.prototype.constructor.prototype.firstElementChild",
     "Option.prototype.constructor.prototype.focus",
+    "Option.prototype.constructor.prototype.focusGroup",
+    "Option.prototype.constructor.prototype.focusGroupStart",
     "Option.prototype.constructor.prototype.getAnimations",
     "Option.prototype.constructor.prototype.getAttribute",
     "Option.prototype.constructor.prototype.getAttributeNS",
@@ -6145,6 +6150,8 @@
     "SVGViewElement.prototype.constructor",
     "SVGViewElement.prototype.dataset",
     "SVGViewElement.prototype.focus",
+    "SVGViewElement.prototype.focusGroup",
+    "SVGViewElement.prototype.focusGroupStart",
     "SVGViewElement.prototype.nonce",
     "SVGViewElement.prototype.onabort",
     "SVGViewElement.prototype.onanimationcancel",
```

  
#### 150.0.7828.2 (`2026-5-7`) 
No browser API changes.

  
#### 149.0.7815.2 (`2026-4-30`) 
No browser API changes.

  
#### 149.0.7808.0 (`2026-4-24`) ⚡
Added 10 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_149.0.7795.2_to_149.0.7808.0.diff), [json](./browser_apis/chrome-unstable_149.0.7795.2_to_149.0.7808.0.json), [full list](./browser_apis/chrome-unstable_149.0.7808.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_149.0.7795.2.json	2026-04-24 23:10:56.461429440 +0000
+++ ./browser_apis/chrome-unstable_149.0.7808.0.json	2026-04-24 23:11:29.737021568 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9333,
+  "browserApiCount": 9343,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -39,6 +39,7 @@
     "AnimationEvent.prototype.animationName",
     "AnimationEvent.prototype.elapsedTime",
     "AnimationEvent.prototype.pseudoElement",
+    "AnimationEvent.prototype.pseudoTarget",
     "AnimationPlaybackEvent",
     "AnimationPlaybackEvent.prototype",
     "AnimationPlaybackEvent.prototype.currentTime",
@@ -721,6 +722,12 @@
     "CSSPropertyRule.prototype.initialValue",
     "CSSPropertyRule.prototype.name",
     "CSSPropertyRule.prototype.syntax",
+    "CSSPseudoElement",
+    "CSSPseudoElement.prototype",
+    "CSSPseudoElement.prototype.element",
+    "CSSPseudoElement.prototype.parent",
+    "CSSPseudoElement.prototype.pseudo",
+    "CSSPseudoElement.prototype.type",
     "CSSRotate",
     "CSSRotate.prototype",
     "CSSRotate.prototype.angle",
@@ -4523,6 +4530,7 @@
     "Option.prototype.constructor.prototype.prefix",
     "Option.prototype.constructor.prototype.prepend",
     "Option.prototype.constructor.prototype.previousElementSibling",
+    "Option.prototype.constructor.prototype.pseudo",
     "Option.prototype.constructor.prototype.querySelector",
     "Option.prototype.constructor.prototype.querySelectorAll",
     "Option.prototype.constructor.prototype.releasePointerCapture",
@@ -7228,6 +7236,7 @@
     "TransitionEvent.prototype.elapsedTime",
     "TransitionEvent.prototype.propertyName",
     "TransitionEvent.prototype.pseudoElement",
+    "TransitionEvent.prototype.pseudoTarget",
     "Translator",
     "Translator.availability",
     "Translator.create",
@@ -8252,6 +8261,7 @@
     "WheelEvent.prototype.constructor.prototype",
     "WheelEvent.prototype.constructor.prototype.detail",
     "WheelEvent.prototype.constructor.prototype.initUIEvent",
+    "WheelEvent.prototype.constructor.prototype.pseudoTarget",
     "WheelEvent.prototype.constructor.prototype.sourceCapabilities",
     "WheelEvent.prototype.constructor.prototype.view",
     "WheelEvent.prototype.constructor.prototype.which",
```

  
#### 149.0.7795.2 (`2026-4-17`) ⚡
Added 32 APIs, removed 18 (see: [diff](./browser_apis/chrome-unstable_149.0.7779.3_to_149.0.7795.2.diff), [json](./browser_apis/chrome-unstable_149.0.7779.3_to_149.0.7795.2.json), [full list](./browser_apis/chrome-unstable_149.0.7795.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_149.0.7779.3.json	2026-04-17 17:13:17.430789569 +0000
+++ ./browser_apis/chrome-unstable_149.0.7795.2.json	2026-04-17 17:14:05.166195145 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9319,
+  "browserApiCount": 9333,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -3195,6 +3195,7 @@
     "Intl.Locale.prototype.region",
     "Intl.Locale.prototype.script",
     "Intl.Locale.prototype.toString",
+    "Intl.Locale.prototype.variants",
     "Intl.NumberFormat",
     "Intl.NumberFormat.prototype",
     "Intl.NumberFormat.prototype.format",
@@ -3301,6 +3302,19 @@
     "LanguageDetector.prototype.expectedInputLanguages",
     "LanguageDetector.prototype.inputQuota",
     "LanguageDetector.prototype.measureInputUsage",
+    "LanguageModel",
+    "LanguageModel.availability",
+    "LanguageModel.create",
+    "LanguageModel.prototype",
+    "LanguageModel.prototype.append",
+    "LanguageModel.prototype.clone",
+    "LanguageModel.prototype.contextUsage",
+    "LanguageModel.prototype.contextWindow",
+    "LanguageModel.prototype.destroy",
+    "LanguageModel.prototype.measureContextUsage",
+    "LanguageModel.prototype.oncontextoverflow",
+    "LanguageModel.prototype.prompt",
+    "LanguageModel.prototype.promptStreaming",
     "LargestContentfulPaint",
     "LargestContentfulPaint.prototype",
     "LargestContentfulPaint.prototype.element",
@@ -8236,27 +8250,9 @@
     "WheelEvent.prototype.clientY",
     "WheelEvent.prototype.constructor",
     "WheelEvent.prototype.constructor.prototype",
-    "WheelEvent.prototype.constructor.prototype.bubbles",
-    "WheelEvent.prototype.constructor.prototype.cancelBubble",
-    "WheelEvent.prototype.constructor.prototype.cancelable",
-    "WheelEvent.prototype.constructor.prototype.composed",
-    "WheelEvent.prototype.constructor.prototype.composedPath",
-    "WheelEvent.prototype.constructor.prototype.constructor",
-    "WheelEvent.prototype.constructor.prototype.currentTarget",
-    "WheelEvent.prototype.constructor.prototype.defaultPrevented",
     "WheelEvent.prototype.constructor.prototype.detail",
-    "WheelEvent.prototype.constructor.prototype.eventPhase",
-    "WheelEvent.prototype.constructor.prototype.initEvent",
     "WheelEvent.prototype.constructor.prototype.initUIEvent",
-    "WheelEvent.prototype.constructor.prototype.preventDefault",
-    "WheelEvent.prototype.constructor.prototype.returnValue",
     "WheelEvent.prototype.constructor.prototype.sourceCapabilities",
-    "WheelEvent.prototype.constructor.prototype.srcElement",
-    "WheelEvent.prototype.constructor.prototype.stopImmediatePropagation",
-    "WheelEvent.prototype.constructor.prototype.stopPropagation",
-    "WheelEvent.prototype.constructor.prototype.target",
-    "WheelEvent.prototype.constructor.prototype.timeStamp",
-    "WheelEvent.prototype.constructor.prototype.type",
     "WheelEvent.prototype.constructor.prototype.view",
     "WheelEvent.prototype.constructor.prototype.which",
     "WheelEvent.prototype.ctrlKey",
@@ -8295,7 +8291,25 @@
     "WindowControlsOverlay.prototype.visible",
     "WindowControlsOverlayGeometryChangeEvent",
     "WindowControlsOverlayGeometryChangeEvent.prototype",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.bubbles",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.cancelBubble",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.cancelable",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.composed",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.composedPath",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.constructor",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.currentTarget",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.defaultPrevented",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.eventPhase",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.initEvent",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.preventDefault",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.returnValue",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.srcElement",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.stopImmediatePropagation",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.stopPropagation",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.target",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.timeStamp",
     "WindowControlsOverlayGeometryChangeEvent.prototype.titlebarAreaRect",
+    "WindowControlsOverlayGeometryChangeEvent.prototype.type",
     "WindowControlsOverlayGeometryChangeEvent.prototype.visible",
     "Worker",
     "Worker.prototype",
```

  
#### 149.0.7779.3 (`2026-4-9`) ⚡
Added 3 APIs, removed 11 (see: [diff](./browser_apis/chrome-unstable_148.0.7766.3_to_149.0.7779.3.diff), [json](./browser_apis/chrome-unstable_148.0.7766.3_to_149.0.7779.3.json), [full list](./browser_apis/chrome-unstable_149.0.7779.3.json))
 ```diff
--- ./browser_apis/chrome-unstable_148.0.7766.3.json	2026-04-09 16:24:38.648637067 +0000
+++ ./browser_apis/chrome-unstable_149.0.7779.3.json	2026-04-09 16:25:14.369272097 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9327,
+  "browserApiCount": 9319,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -39,7 +39,6 @@
     "AnimationEvent.prototype.animationName",
     "AnimationEvent.prototype.elapsedTime",
     "AnimationEvent.prototype.pseudoElement",
-    "AnimationEvent.prototype.pseudoTarget",
     "AnimationPlaybackEvent",
     "AnimationPlaybackEvent.prototype",
     "AnimationPlaybackEvent.prototype.currentTime",
@@ -157,6 +156,7 @@
     "Audio.prototype.constructor.prototype.ended",
     "Audio.prototype.constructor.prototype.error",
     "Audio.prototype.constructor.prototype.load",
+    "Audio.prototype.constructor.prototype.loading",
     "Audio.prototype.constructor.prototype.loop",
     "Audio.prototype.constructor.prototype.mediaKeys",
     "Audio.prototype.constructor.prototype.muted",
@@ -721,12 +721,6 @@
     "CSSPropertyRule.prototype.initialValue",
     "CSSPropertyRule.prototype.name",
     "CSSPropertyRule.prototype.syntax",
-    "CSSPseudoElement",
-    "CSSPseudoElement.prototype",
-    "CSSPseudoElement.prototype.element",
-    "CSSPseudoElement.prototype.parent",
-    "CSSPseudoElement.prototype.pseudo",
-    "CSSPseudoElement.prototype.type",
     "CSSRotate",
     "CSSRotate.prototype",
     "CSSRotate.prototype.angle",
@@ -4515,7 +4509,6 @@
     "Option.prototype.constructor.prototype.prefix",
     "Option.prototype.constructor.prototype.prepend",
     "Option.prototype.constructor.prototype.previousElementSibling",
-    "Option.prototype.constructor.prototype.pseudo",
     "Option.prototype.constructor.prototype.querySelector",
     "Option.prototype.constructor.prototype.querySelectorAll",
     "Option.prototype.constructor.prototype.releasePointerCapture",
@@ -4792,6 +4785,7 @@
     "PerformanceResourceTiming.prototype.connectEnd",
     "PerformanceResourceTiming.prototype.connectStart",
     "PerformanceResourceTiming.prototype.contentEncoding",
+    "PerformanceResourceTiming.prototype.contentType",
     "PerformanceResourceTiming.prototype.decodedBodySize",
     "PerformanceResourceTiming.prototype.deliveryType",
     "PerformanceResourceTiming.prototype.domainLookupEnd",
@@ -6459,7 +6453,6 @@
     "SharedStorage.prototype.clear",
     "SharedStorage.prototype.createWorklet",
     "SharedStorage.prototype.delete",
-    "SharedStorage.prototype.get",
     "SharedStorage.prototype.run",
     "SharedStorage.prototype.selectURL",
     "SharedStorage.prototype.set",
@@ -7221,7 +7214,6 @@
     "TransitionEvent.prototype.elapsedTime",
     "TransitionEvent.prototype.propertyName",
     "TransitionEvent.prototype.pseudoElement",
-    "TransitionEvent.prototype.pseudoTarget",
     "Translator",
     "Translator.availability",
     "Translator.create",
@@ -7655,6 +7647,7 @@
     "WebAssembly.Exception.prototype",
     "WebAssembly.Exception.prototype.getArg",
     "WebAssembly.Exception.prototype.is",
+    "WebAssembly.Exception.prototype.stack",
     "WebAssembly.Global",
     "WebAssembly.Global.prototype",
     "WebAssembly.Global.prototype.value",
@@ -8256,7 +8249,6 @@
     "WheelEvent.prototype.constructor.prototype.initEvent",
     "WheelEvent.prototype.constructor.prototype.initUIEvent",
     "WheelEvent.prototype.constructor.prototype.preventDefault",
-    "WheelEvent.prototype.constructor.prototype.pseudoTarget",
     "WheelEvent.prototype.constructor.prototype.returnValue",
     "WheelEvent.prototype.constructor.prototype.sourceCapabilities",
     "WheelEvent.prototype.constructor.prototype.srcElement",
```

  
#### 148.0.7766.3 (`2026-4-2`) ⚡
Added 1 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_148.0.7753.0_to_148.0.7766.3.diff), [json](./browser_apis/chrome-unstable_148.0.7753.0_to_148.0.7766.3.json), [full list](./browser_apis/chrome-unstable_148.0.7766.3.json))
 ```diff
--- ./browser_apis/chrome-unstable_148.0.7753.0.json	2026-04-02 18:11:33.790315179 +0000
+++ ./browser_apis/chrome-unstable_148.0.7766.3.json	2026-04-02 18:12:09.000336238 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9326,
+  "browserApiCount": 9327,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -4656,6 +4656,7 @@
     "PaymentMethodChangeEvent.prototype.methodDetails",
     "PaymentMethodChangeEvent.prototype.methodName",
     "PaymentRequest",
+    "PaymentRequest.getSecurePaymentConfirmationCapabilities",
     "PaymentRequest.prototype",
     "PaymentRequest.prototype.abort",
     "PaymentRequest.prototype.canMakePayment",
```

  
#### 148.0.7753.0 (`2026-3-26`) 
No browser API changes.

  
#### 148.0.7743.0 (`2026-3-24`) ⚡
Added 1 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_148.0.7730.2_to_148.0.7743.0.diff), [json](./browser_apis/chrome-unstable_148.0.7730.2_to_148.0.7743.0.json), [full list](./browser_apis/chrome-unstable_148.0.7743.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_148.0.7730.2.json	2026-03-24 17:17:19.955214282 +0000
+++ ./browser_apis/chrome-unstable_148.0.7743.0.json	2026-03-24 17:17:59.659789983 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9325,
+  "browserApiCount": 9326,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -1088,6 +1088,7 @@
     "CreateMonitor.prototype",
     "CreateMonitor.prototype.ondownloadprogress",
     "Credential",
+    "Credential.isConditionalMediationAvailable",
     "Credential.prototype",
     "Credential.prototype.id",
     "Credential.prototype.type",
```

  
#### 148.0.7730.2 (`2026-3-13`) 
No browser API changes.

  
#### 147.0.7719.3 (`2026-3-6`) ⚡
Added 10 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_147.0.7703.0_to_147.0.7719.3.diff), [json](./browser_apis/chrome-unstable_147.0.7703.0_to_147.0.7719.3.json), [full list](./browser_apis/chrome-unstable_147.0.7719.3.json))
 ```diff
--- ./browser_apis/chrome-unstable_147.0.7703.0.json	2026-03-06 20:03:19.287418601 +0000
+++ ./browser_apis/chrome-unstable_147.0.7719.3.json	2026-03-06 20:03:55.366484617 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9315,
+  "browserApiCount": 9325,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -39,6 +39,7 @@
     "AnimationEvent.prototype.animationName",
     "AnimationEvent.prototype.elapsedTime",
     "AnimationEvent.prototype.pseudoElement",
+    "AnimationEvent.prototype.pseudoTarget",
     "AnimationPlaybackEvent",
     "AnimationPlaybackEvent.prototype",
     "AnimationPlaybackEvent.prototype.currentTime",
@@ -720,6 +721,12 @@
     "CSSPropertyRule.prototype.initialValue",
     "CSSPropertyRule.prototype.name",
     "CSSPropertyRule.prototype.syntax",
+    "CSSPseudoElement",
+    "CSSPseudoElement.prototype",
+    "CSSPseudoElement.prototype.element",
+    "CSSPseudoElement.prototype.parent",
+    "CSSPseudoElement.prototype.pseudo",
+    "CSSPseudoElement.prototype.type",
     "CSSRotate",
     "CSSRotate.prototype",
     "CSSRotate.prototype.angle",
@@ -4507,6 +4514,7 @@
     "Option.prototype.constructor.prototype.prefix",
     "Option.prototype.constructor.prototype.prepend",
     "Option.prototype.constructor.prototype.previousElementSibling",
+    "Option.prototype.constructor.prototype.pseudo",
     "Option.prototype.constructor.prototype.querySelector",
     "Option.prototype.constructor.prototype.querySelectorAll",
     "Option.prototype.constructor.prototype.releasePointerCapture",
@@ -7211,6 +7219,7 @@
     "TransitionEvent.prototype.elapsedTime",
     "TransitionEvent.prototype.propertyName",
     "TransitionEvent.prototype.pseudoElement",
+    "TransitionEvent.prototype.pseudoTarget",
     "Translator",
     "Translator.availability",
     "Translator.create",
@@ -8245,6 +8254,7 @@
     "WheelEvent.prototype.constructor.prototype.initEvent",
     "WheelEvent.prototype.constructor.prototype.initUIEvent",
     "WheelEvent.prototype.constructor.prototype.preventDefault",
+    "WheelEvent.prototype.constructor.prototype.pseudoTarget",
     "WheelEvent.prototype.constructor.prototype.returnValue",
     "WheelEvent.prototype.constructor.prototype.sourceCapabilities",
     "WheelEvent.prototype.constructor.prototype.srcElement",
```

  
#### 147.0.7703.0 (`2026-2-26`) ⚡
Added 96 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_147.0.7695.0_to_147.0.7703.0.diff), [json](./browser_apis/chrome-unstable_147.0.7695.0_to_147.0.7703.0.json), [full list](./browser_apis/chrome-unstable_147.0.7703.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_147.0.7695.0.json	2026-02-26 18:10:55.293401149 +0000
+++ ./browser_apis/chrome-unstable_147.0.7703.0.json	2026-02-26 18:11:31.946128419 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9219,
+  "browserApiCount": 9315,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -3438,6 +3438,7 @@
     "Math.sin",
     "Math.sinh",
     "Math.sqrt",
+    "Math.sumPrecise",
     "Math.tan",
     "Math.tanh",
     "Math.trunc",
@@ -4226,6 +4227,7 @@
     "Option.prototype.constructor",
     "Option.prototype.constructor.prototype",
     "Option.prototype.constructor.prototype.accessKey",
+    "Option.prototype.constructor.prototype.activeViewTransition",
     "Option.prototype.constructor.prototype.after",
     "Option.prototype.constructor.prototype.animate",
     "Option.prototype.constructor.prototype.append",
@@ -4537,6 +4539,7 @@
     "Option.prototype.constructor.prototype.showPopover",
     "Option.prototype.constructor.prototype.slot",
     "Option.prototype.constructor.prototype.spellcheck",
+    "Option.prototype.constructor.prototype.startViewTransition",
     "Option.prototype.constructor.prototype.style",
     "Option.prototype.constructor.prototype.tabIndex",
     "Option.prototype.constructor.prototype.tagName",
@@ -7541,6 +7544,7 @@
     "ViewTransition.prototype.finished",
     "ViewTransition.prototype.ready",
     "ViewTransition.prototype.skipTransition",
+    "ViewTransition.prototype.transitionRoot",
     "ViewTransition.prototype.types",
     "ViewTransition.prototype.updateCallbackDone",
     "ViewTransition.prototype.waitUntil",
@@ -8658,12 +8662,44 @@
     "XRCamera.prototype",
     "XRCamera.prototype.height",
     "XRCamera.prototype.width",
+    "XRCompositionLayer",
+    "XRCompositionLayer.prototype",
+    "XRCompositionLayer.prototype.blendTextureSourceAlpha",
+    "XRCompositionLayer.prototype.destroy",
+    "XRCompositionLayer.prototype.forceMonoPresentation",
+    "XRCompositionLayer.prototype.layout",
+    "XRCompositionLayer.prototype.mipLevels",
+    "XRCompositionLayer.prototype.needsRedraw",
+    "XRCompositionLayer.prototype.opacity",
+    "XRCubeLayer",
+    "XRCubeLayer.prototype",
+    "XRCubeLayer.prototype.onredraw",
+    "XRCubeLayer.prototype.orientation",
+    "XRCubeLayer.prototype.space",
+    "XRCylinderLayer",
+    "XRCylinderLayer.prototype",
+    "XRCylinderLayer.prototype.aspectRatio",
+    "XRCylinderLayer.prototype.centralAngle",
+    "XRCylinderLayer.prototype.onredraw",
+    "XRCylinderLayer.prototype.radius",
+    "XRCylinderLayer.prototype.space",
+    "XRCylinderLayer.prototype.transform",
     "XRDOMOverlayState",
     "XRDOMOverlayState.prototype",
     "XRDOMOverlayState.prototype.type",
+    "XREquirectLayer",
+    "XREquirectLayer.prototype",
+    "XREquirectLayer.prototype.centralHorizontalAngle",
+    "XREquirectLayer.prototype.lowerVerticalAngle",
+    "XREquirectLayer.prototype.onredraw",
+    "XREquirectLayer.prototype.radius",
+    "XREquirectLayer.prototype.space",
+    "XREquirectLayer.prototype.transform",
+    "XREquirectLayer.prototype.upperVerticalAngle",
     "XRFrame",
     "XRFrame.prototype",
     "XRFrame.prototype.createAnchor",
+    "XRFrame.prototype.detectedPlanes",
     "XRFrame.prototype.fillJointRadii",
     "XRFrame.prototype.fillPoses",
     "XRFrame.prototype.getDepthInformation",
@@ -8722,6 +8758,9 @@
     "XRJointSpace.prototype.jointName",
     "XRLayer",
     "XRLayer.prototype",
+    "XRLayerEvent",
+    "XRLayerEvent.prototype",
+    "XRLayerEvent.prototype.layer",
     "XRLightEstimate",
     "XRLightEstimate.prototype",
     "XRLightEstimate.prototype.primaryLightDirection",
@@ -8731,6 +8770,36 @@
     "XRLightProbe.prototype",
     "XRLightProbe.prototype.onreflectionchange",
     "XRLightProbe.prototype.probeSpace",
+    "XRPlane",
+    "XRPlane.prototype",
+    "XRPlane.prototype.lastChangedTime",
+    "XRPlane.prototype.orientation",
+    "XRPlane.prototype.planeSpace",
+    "XRPlane.prototype.polygon",
+    "XRPlane.prototype.semanticLabel",
+    "XRPlaneSet",
+    "XRPlaneSet.prototype",
+    "XRPlaneSet.prototype.entries",
+    "XRPlaneSet.prototype.forEach",
+    "XRPlaneSet.prototype.has",
+    "XRPlaneSet.prototype.keys",
+    "XRPlaneSet.prototype.size",
+    "XRPlaneSet.prototype.values",
+    "XRProjectionLayer",
+    "XRProjectionLayer.prototype",
+    "XRProjectionLayer.prototype.deltaPose",
+    "XRProjectionLayer.prototype.fixedFoveation",
+    "XRProjectionLayer.prototype.ignoreDepthValues",
+    "XRProjectionLayer.prototype.textureArrayLength",
+    "XRProjectionLayer.prototype.textureHeight",
+    "XRProjectionLayer.prototype.textureWidth",
+    "XRQuadLayer",
+    "XRQuadLayer.prototype",
+    "XRQuadLayer.prototype.height",
+    "XRQuadLayer.prototype.onredraw",
+    "XRQuadLayer.prototype.space",
+    "XRQuadLayer.prototype.transform",
+    "XRQuadLayer.prototype.width",
     "XRRay",
     "XRRay.prototype",
     "XRRay.prototype.direction",
@@ -8746,6 +8815,7 @@
     "XRRenderState.prototype.depthFar",
     "XRRenderState.prototype.depthNear",
     "XRRenderState.prototype.inlineVerticalFieldOfView",
+    "XRRenderState.prototype.layers",
     "XRRigidTransform",
     "XRRigidTransform.prototype",
     "XRRigidTransform.prototype.inverse",
@@ -8763,8 +8833,10 @@
     "XRSession.prototype.enabledFeatures",
     "XRSession.prototype.end",
     "XRSession.prototype.environmentBlendMode",
+    "XRSession.prototype.initiateRoomCapture",
     "XRSession.prototype.inputSources",
     "XRSession.prototype.interactionMode",
+    "XRSession.prototype.maxRenderLayers",
     "XRSession.prototype.onend",
     "XRSession.prototype.oninputsourceschange",
     "XRSession.prototype.onselect",
@@ -8789,6 +8861,9 @@
     "XRSessionEvent",
     "XRSessionEvent.prototype",
     "XRSessionEvent.prototype.session",
+    "XRSubImage",
+    "XRSubImage.prototype",
+    "XRSubImage.prototype.viewport",
     "XRSystem",
     "XRSystem.prototype",
     "XRSystem.prototype.isSessionSupported",
@@ -8829,9 +8904,18 @@
     "XRVisibilityMaskChangeEvent.prototype.vertices",
     "XRWebGLBinding",
     "XRWebGLBinding.prototype",
+    "XRWebGLBinding.prototype.createCubeLayer",
+    "XRWebGLBinding.prototype.createCylinderLayer",
+    "XRWebGLBinding.prototype.createEquirectLayer",
+    "XRWebGLBinding.prototype.createProjectionLayer",
+    "XRWebGLBinding.prototype.createQuadLayer",
     "XRWebGLBinding.prototype.getCameraImage",
     "XRWebGLBinding.prototype.getDepthInformation",
     "XRWebGLBinding.prototype.getReflectionCubeMap",
+    "XRWebGLBinding.prototype.getSubImage",
+    "XRWebGLBinding.prototype.getViewSubImage",
+    "XRWebGLBinding.prototype.nativeProjectionScaleFactor",
+    "XRWebGLBinding.prototype.usesDepthValues",
     "XRWebGLDepthInformation",
     "XRWebGLDepthInformation.prototype",
     "XRWebGLDepthInformation.prototype.texture",
@@ -8844,6 +8928,18 @@
     "XRWebGLLayer.prototype.framebufferWidth",
     "XRWebGLLayer.prototype.getViewport",
     "XRWebGLLayer.prototype.ignoreDepthValues",
+    "XRWebGLSubImage",
+    "XRWebGLSubImage.prototype",
+    "XRWebGLSubImage.prototype.colorTexture",
+    "XRWebGLSubImage.prototype.colorTextureHeight",
+    "XRWebGLSubImage.prototype.colorTextureWidth",
+    "XRWebGLSubImage.prototype.depthStencilTexture",
+    "XRWebGLSubImage.prototype.depthStencilTextureHeight",
+    "XRWebGLSubImage.prototype.depthStencilTextureWidth",
+    "XRWebGLSubImage.prototype.imageIndex",
+    "XRWebGLSubImage.prototype.motionVectorTexture",
+    "XRWebGLSubImage.prototype.motionVectorTextureHeight",
+    "XRWebGLSubImage.prototype.motionVectorTextureWidth",
     "XSLTProcessor",
     "XSLTProcessor.prototype",
     "XSLTProcessor.prototype.clearParameters",
```

  
#### 147.0.7695.0 (`2026-2-20`) ⚡
Added 28 APIs, removed 2 (see: [diff](./browser_apis/chrome-unstable_146.0.7670.2_to_147.0.7695.0.diff), [json](./browser_apis/chrome-unstable_146.0.7670.2_to_147.0.7695.0.json), [full list](./browser_apis/chrome-unstable_147.0.7695.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_146.0.7670.2.json	2026-02-20 18:07:32.491000272 +0000
+++ ./browser_apis/chrome-unstable_147.0.7695.0.json	2026-02-20 18:08:07.178055496 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9193,
+  "browserApiCount": 9219,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -211,6 +211,7 @@
     "AudioContext.prototype.onerror",
     "AudioContext.prototype.onsinkchange",
     "AudioContext.prototype.outputLatency",
+    "AudioContext.prototype.playbackStats",
     "AudioContext.prototype.resume",
     "AudioContext.prototype.setSinkId",
     "AudioContext.prototype.sinkId",
@@ -288,6 +289,16 @@
     "AudioParamMap.prototype.keys",
     "AudioParamMap.prototype.size",
     "AudioParamMap.prototype.values",
+    "AudioPlaybackStats",
+    "AudioPlaybackStats.prototype",
+    "AudioPlaybackStats.prototype.averageLatency",
+    "AudioPlaybackStats.prototype.maximumLatency",
+    "AudioPlaybackStats.prototype.minimumLatency",
+    "AudioPlaybackStats.prototype.resetLatency",
+    "AudioPlaybackStats.prototype.toJSON",
+    "AudioPlaybackStats.prototype.totalDuration",
+    "AudioPlaybackStats.prototype.underrunDuration",
+    "AudioPlaybackStats.prototype.underrunEvents",
     "AudioProcessingEvent",
     "AudioProcessingEvent.prototype",
     "AudioProcessingEvent.prototype.inputBuffer",
@@ -3842,6 +3853,7 @@
     "NavigationHistoryEntry.prototype.url",
     "NavigationPrecommitController",
     "NavigationPrecommitController.prototype",
+    "NavigationPrecommitController.prototype.addHandler",
     "NavigationPrecommitController.prototype.redirect",
     "NavigationPreloadManager",
     "NavigationPreloadManager.prototype",
@@ -4518,6 +4530,7 @@
     "Option.prototype.constructor.prototype.setAttributeNS",
     "Option.prototype.constructor.prototype.setAttributeNode",
     "Option.prototype.constructor.prototype.setAttributeNodeNS",
+    "Option.prototype.constructor.prototype.setHTML",
     "Option.prototype.constructor.prototype.setHTMLUnsafe",
     "Option.prototype.constructor.prototype.setPointerCapture",
     "Option.prototype.constructor.prototype.shadowRoot",
@@ -6213,6 +6226,17 @@
     "SVGViewElement.prototype.viewBox",
     "SVGViewElement.prototype.viewportElement",
     "SVGViewElement.prototype.zoomAndPan",
+    "Sanitizer",
+    "Sanitizer.prototype",
+    "Sanitizer.prototype.allowAttribute",
+    "Sanitizer.prototype.allowElement",
+    "Sanitizer.prototype.get",
+    "Sanitizer.prototype.removeAttribute",
+    "Sanitizer.prototype.removeElement",
+    "Sanitizer.prototype.removeUnsafe",
+    "Sanitizer.prototype.replaceElementWithChildren",
+    "Sanitizer.prototype.setComments",
+    "Sanitizer.prototype.setDataAttributes",
     "Scheduler",
     "Scheduler.prototype",
     "Scheduler.prototype.postTask",
@@ -6411,6 +6435,7 @@
     "ShadowRoot.prototype.querySelectorAll",
     "ShadowRoot.prototype.replaceChildren",
     "ShadowRoot.prototype.serializable",
+    "ShadowRoot.prototype.setHTML",
     "ShadowRoot.prototype.setHTMLUnsafe",
     "ShadowRoot.prototype.slotAssignment",
     "ShadowRoot.prototype.styleSheets",
@@ -7124,10 +7149,10 @@
     "TimelineTrigger.prototype.ranges",
     "TimelineTriggerRange",
     "TimelineTriggerRange.prototype",
+    "TimelineTriggerRange.prototype.activationRangeEnd",
+    "TimelineTriggerRange.prototype.activationRangeStart",
     "TimelineTriggerRange.prototype.activeRangeEnd",
     "TimelineTriggerRange.prototype.activeRangeStart",
-    "TimelineTriggerRange.prototype.entryRangeEnd",
-    "TimelineTriggerRange.prototype.entryRangeStart",
     "TimelineTriggerRange.prototype.timeline",
     "TimelineTriggerRangeList",
     "TimelineTriggerRangeList.prototype",
@@ -8316,6 +8341,7 @@
     "XMLDocument.prototype.close",
     "XMLDocument.prototype.compatMode",
     "XMLDocument.prototype.constructor",
+    "XMLDocument.prototype.constructor.parseHTML",
     "XMLDocument.prototype.constructor.parseHTMLUnsafe",
     "XMLDocument.prototype.contentType",
     "XMLDocument.prototype.cookie",
```

  
#### 146.0.7670.2 (`2026-2-6`) ⚡
Added 17 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_146.0.7655.0_to_146.0.7670.2.diff), [json](./browser_apis/chrome-unstable_146.0.7655.0_to_146.0.7670.2.json), [full list](./browser_apis/chrome-unstable_146.0.7670.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_146.0.7655.0.json	2026-02-06 18:09:21.112106877 +0000
+++ ./browser_apis/chrome-unstable_146.0.7670.2.json	2026-02-06 18:09:57.614232429 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9176,
+  "browserApiCount": 9193,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -1061,6 +1061,11 @@
     "CountQueuingStrategy.prototype",
     "CountQueuingStrategy.prototype.highWaterMark",
     "CountQueuingStrategy.prototype.size",
+    "CrashReportContext",
+    "CrashReportContext.prototype",
+    "CrashReportContext.prototype.delete",
+    "CrashReportContext.prototype.initialize",
+    "CrashReportContext.prototype.set",
     "CreateMonitor",
     "CreateMonitor.prototype",
     "CreateMonitor.prototype.ondownloadprogress",
@@ -1093,6 +1098,7 @@
     "CustomElementRegistry.prototype.define",
     "CustomElementRegistry.prototype.get",
     "CustomElementRegistry.prototype.getName",
+    "CustomElementRegistry.prototype.initialize",
     "CustomElementRegistry.prototype.upgrade",
     "CustomElementRegistry.prototype.whenDefined",
     "CustomEvent",
@@ -1889,7 +1895,11 @@
     "GPUSupportedLimits.prototype.maxSampledTexturesPerShaderStage",
     "GPUSupportedLimits.prototype.maxSamplersPerShaderStage",
     "GPUSupportedLimits.prototype.maxStorageBufferBindingSize",
+    "GPUSupportedLimits.prototype.maxStorageBuffersInFragmentStage",
+    "GPUSupportedLimits.prototype.maxStorageBuffersInVertexStage",
     "GPUSupportedLimits.prototype.maxStorageBuffersPerShaderStage",
+    "GPUSupportedLimits.prototype.maxStorageTexturesInFragmentStage",
+    "GPUSupportedLimits.prototype.maxStorageTexturesInVertexStage",
     "GPUSupportedLimits.prototype.maxStorageTexturesPerShaderStage",
     "GPUSupportedLimits.prototype.maxTextureArrayLayers",
     "GPUSupportedLimits.prototype.maxTextureDimension1D",
@@ -1913,6 +1923,7 @@
     "GPUTexture.prototype.label",
     "GPUTexture.prototype.mipLevelCount",
     "GPUTexture.prototype.sampleCount",
+    "GPUTexture.prototype.textureBindingViewDimension",
     "GPUTexture.prototype.usage",
     "GPUTexture.prototype.width",
     "GPUTextureUsage",
@@ -2705,6 +2716,7 @@
     "HTMLTemplateElement.prototype",
     "HTMLTemplateElement.prototype.content",
     "HTMLTemplateElement.prototype.shadowRootClonable",
+    "HTMLTemplateElement.prototype.shadowRootCustomElementRegistry",
     "HTMLTemplateElement.prototype.shadowRootDelegatesFocus",
     "HTMLTemplateElement.prototype.shadowRootMode",
     "HTMLTemplateElement.prototype.shadowRootSerializable",
@@ -3207,6 +3219,7 @@
     "Intl.v8BreakIterator.prototype.resolvedOptions",
     "Intl.v8BreakIterator.supportedLocalesOf",
     "Iterator",
+    "Iterator.concat",
     "Iterator.from",
     "Iterator.prototype",
     "Iterator.prototype.constructor",
@@ -4314,6 +4327,7 @@
     "Option.prototype.constructor.prototype.constructor.prototype.when",
     "Option.prototype.constructor.prototype.contentEditable",
     "Option.prototype.constructor.prototype.currentCSSZoom",
+    "Option.prototype.constructor.prototype.customElementRegistry",
     "Option.prototype.constructor.prototype.dataset",
     "Option.prototype.constructor.prototype.dir",
     "Option.prototype.constructor.prototype.draggable",
@@ -6374,6 +6388,7 @@
     "ShadowRoot.prototype.children",
     "ShadowRoot.prototype.clonable",
     "ShadowRoot.prototype.constructor",
+    "ShadowRoot.prototype.customElementRegistry",
     "ShadowRoot.prototype.delegatesFocus",
     "ShadowRoot.prototype.elementFromPoint",
     "ShadowRoot.prototype.elementsFromPoint",
@@ -8320,6 +8335,7 @@
     "XMLDocument.prototype.createTextNode",
     "XMLDocument.prototype.createTreeWalker",
     "XMLDocument.prototype.currentScript",
+    "XMLDocument.prototype.customElementRegistry",
     "XMLDocument.prototype.defaultView",
     "XMLDocument.prototype.designMode",
     "XMLDocument.prototype.dir",
@@ -8865,6 +8881,7 @@
     "console.trace",
     "console.warn",
     "cookieStore",
+    "crashReport",
     "createImageBitmap",
     "credentialless",
     "crossOriginIsolated",
```

  
#### 146.0.7655.0 (`2026-1-29`) ⚡
Added 0 APIs, removed 14 (see: [diff](./browser_apis/chrome-unstable_146.0.7647.3_to_146.0.7655.0.diff), [json](./browser_apis/chrome-unstable_146.0.7647.3_to_146.0.7655.0.json), [full list](./browser_apis/chrome-unstable_146.0.7655.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_146.0.7647.3.json	2026-01-29 19:11:10.345583247 +0000
+++ ./browser_apis/chrome-unstable_146.0.7655.0.json	2026-01-29 19:11:52.419416394 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9190,
+  "browserApiCount": 9176,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -4504,7 +4504,6 @@
     "Option.prototype.constructor.prototype.setAttributeNS",
     "Option.prototype.constructor.prototype.setAttributeNode",
     "Option.prototype.constructor.prototype.setAttributeNodeNS",
-    "Option.prototype.constructor.prototype.setHTML",
     "Option.prototype.constructor.prototype.setHTMLUnsafe",
     "Option.prototype.constructor.prototype.setPointerCapture",
     "Option.prototype.constructor.prototype.shadowRoot",
@@ -6200,17 +6199,6 @@
     "SVGViewElement.prototype.viewBox",
     "SVGViewElement.prototype.viewportElement",
     "SVGViewElement.prototype.zoomAndPan",
-    "Sanitizer",
-    "Sanitizer.prototype",
-    "Sanitizer.prototype.allowAttribute",
-    "Sanitizer.prototype.allowElement",
-    "Sanitizer.prototype.get",
-    "Sanitizer.prototype.removeAttribute",
-    "Sanitizer.prototype.removeElement",
-    "Sanitizer.prototype.removeUnsafe",
-    "Sanitizer.prototype.replaceElementWithChildren",
-    "Sanitizer.prototype.setComments",
-    "Sanitizer.prototype.setDataAttributes",
     "Scheduler",
     "Scheduler.prototype",
     "Scheduler.prototype.postTask",
@@ -6408,7 +6396,6 @@
     "ShadowRoot.prototype.querySelectorAll",
     "ShadowRoot.prototype.replaceChildren",
     "ShadowRoot.prototype.serializable",
-    "ShadowRoot.prototype.setHTML",
     "ShadowRoot.prototype.setHTMLUnsafe",
     "ShadowRoot.prototype.slotAssignment",
     "ShadowRoot.prototype.styleSheets",
@@ -8314,7 +8301,6 @@
     "XMLDocument.prototype.close",
     "XMLDocument.prototype.compatMode",
     "XMLDocument.prototype.constructor",
-    "XMLDocument.prototype.constructor.parseHTML",
     "XMLDocument.prototype.constructor.parseHTMLUnsafe",
     "XMLDocument.prototype.contentType",
     "XMLDocument.prototype.cookie",
```

  
#### 146.0.7647.3 (`2026-1-22`) ⚡
Added 19 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_146.0.7635.0_to_146.0.7647.3.diff), [json](./browser_apis/chrome-unstable_146.0.7635.0_to_146.0.7647.3.json), [full list](./browser_apis/chrome-unstable_146.0.7647.3.json))
 ```diff
--- ./browser_apis/chrome-unstable_146.0.7635.0.json	2026-01-22 20:00:55.971656179 +0000
+++ ./browser_apis/chrome-unstable_146.0.7647.3.json	2026-01-22 20:01:35.274371154 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9171,
+  "browserApiCount": 9190,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -43,6 +43,11 @@
     "AnimationPlaybackEvent.prototype",
     "AnimationPlaybackEvent.prototype.currentTime",
     "AnimationPlaybackEvent.prototype.timelineTime",
+    "AnimationTrigger",
+    "AnimationTrigger.prototype",
+    "AnimationTrigger.prototype.addAnimation",
+    "AnimationTrigger.prototype.getAnimations",
+    "AnimationTrigger.prototype.removeAnimation",
     "Array",
     "Array.from",
     "Array.fromAsync",
@@ -7112,6 +7117,20 @@
     "TimeRanges.prototype.end",
     "TimeRanges.prototype.length",
     "TimeRanges.prototype.start",
+    "TimelineTrigger",
+    "TimelineTrigger.prototype",
+    "TimelineTrigger.prototype.ranges",
+    "TimelineTriggerRange",
+    "TimelineTriggerRange.prototype",
+    "TimelineTriggerRange.prototype.activeRangeEnd",
+    "TimelineTriggerRange.prototype.activeRangeStart",
+    "TimelineTriggerRange.prototype.entryRangeEnd",
+    "TimelineTriggerRange.prototype.entryRangeStart",
+    "TimelineTriggerRange.prototype.timeline",
+    "TimelineTriggerRangeList",
+    "TimelineTriggerRangeList.prototype",
+    "TimelineTriggerRangeList.prototype.item",
+    "TimelineTriggerRangeList.prototype.length",
     "ToggleEvent",
     "ToggleEvent.prototype",
     "ToggleEvent.prototype.newState",
```

  
#### 146.0.7635.0 (`2026-1-16`) ⚡
Added 16 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_145.0.7620.2_to_146.0.7635.0.diff), [json](./browser_apis/chrome-unstable_145.0.7620.2_to_146.0.7635.0.json), [full list](./browser_apis/chrome-unstable_146.0.7635.0.json))
 ```diff
--- ./browser_apis/chrome-unstable_145.0.7620.2.json	2026-01-16 18:00:58.980011057 +0000
+++ ./browser_apis/chrome-unstable_146.0.7635.0.json	2026-01-16 18:01:38.885178202 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9155,
+  "browserApiCount": 9171,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -2560,11 +2560,13 @@
     "HTMLScriptElement.prototype.event",
     "HTMLScriptElement.prototype.fetchPriority",
     "HTMLScriptElement.prototype.htmlFor",
+    "HTMLScriptElement.prototype.innerText",
     "HTMLScriptElement.prototype.integrity",
     "HTMLScriptElement.prototype.noModule",
     "HTMLScriptElement.prototype.referrerPolicy",
     "HTMLScriptElement.prototype.src",
     "HTMLScriptElement.prototype.text",
+    "HTMLScriptElement.prototype.textContent",
     "HTMLScriptElement.prototype.type",
     "HTMLScriptElement.supports",
     "HTMLSelectElement",
@@ -4497,6 +4499,7 @@
     "Option.prototype.constructor.prototype.setAttributeNS",
     "Option.prototype.constructor.prototype.setAttributeNode",
     "Option.prototype.constructor.prototype.setAttributeNodeNS",
+    "Option.prototype.constructor.prototype.setHTML",
     "Option.prototype.constructor.prototype.setHTMLUnsafe",
     "Option.prototype.constructor.prototype.setPointerCapture",
     "Option.prototype.constructor.prototype.shadowRoot",
@@ -6192,6 +6195,17 @@
     "SVGViewElement.prototype.viewBox",
     "SVGViewElement.prototype.viewportElement",
     "SVGViewElement.prototype.zoomAndPan",
+    "Sanitizer",
+    "Sanitizer.prototype",
+    "Sanitizer.prototype.allowAttribute",
+    "Sanitizer.prototype.allowElement",
+    "Sanitizer.prototype.get",
+    "Sanitizer.prototype.removeAttribute",
+    "Sanitizer.prototype.removeElement",
+    "Sanitizer.prototype.removeUnsafe",
+    "Sanitizer.prototype.replaceElementWithChildren",
+    "Sanitizer.prototype.setComments",
+    "Sanitizer.prototype.setDataAttributes",
     "Scheduler",
     "Scheduler.prototype",
     "Scheduler.prototype.postTask",
@@ -6389,6 +6403,7 @@
     "ShadowRoot.prototype.querySelectorAll",
     "ShadowRoot.prototype.replaceChildren",
     "ShadowRoot.prototype.serializable",
+    "ShadowRoot.prototype.setHTML",
     "ShadowRoot.prototype.setHTMLUnsafe",
     "ShadowRoot.prototype.slotAssignment",
     "ShadowRoot.prototype.styleSheets",
@@ -8280,6 +8295,7 @@
     "XMLDocument.prototype.close",
     "XMLDocument.prototype.compatMode",
     "XMLDocument.prototype.constructor",
+    "XMLDocument.prototype.constructor.parseHTML",
     "XMLDocument.prototype.constructor.parseHTMLUnsafe",
     "XMLDocument.prototype.contentType",
     "XMLDocument.prototype.cookie",
```

  
#### 145.0.7620.2 (`2026-1-9`) ⚡
Added 7 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_145.0.7587.4_to_145.0.7620.2.diff), [json](./browser_apis/chrome-unstable_145.0.7587.4_to_145.0.7620.2.json), [full list](./browser_apis/chrome-unstable_145.0.7620.2.json))
 ```diff
--- ./browser_apis/chrome-unstable_145.0.7587.4.json	2026-01-09 18:01:05.116647824 +0000
+++ ./browser_apis/chrome-unstable_145.0.7620.2.json	2026-01-09 18:01:45.392450372 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9148,
+  "browserApiCount": 9155,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -3835,6 +3835,7 @@
     "NavigationTransition.prototype.finished",
     "NavigationTransition.prototype.from",
     "NavigationTransition.prototype.navigationType",
+    "NavigationTransition.prototype.to",
     "Navigator",
     "Navigator.prototype",
     "Navigator.prototype.adAuctionComponents",
@@ -4709,6 +4710,7 @@
     "PerformanceNavigationTiming",
     "PerformanceNavigationTiming.prototype",
     "PerformanceNavigationTiming.prototype.activationStart",
+    "PerformanceNavigationTiming.prototype.confidence",
     "PerformanceNavigationTiming.prototype.criticalCHRestart",
     "PerformanceNavigationTiming.prototype.domComplete",
     "PerformanceNavigationTiming.prototype.domContentLoadedEventEnd",
@@ -4812,6 +4814,11 @@
     "PerformanceTiming.prototype.toJSON",
     "PerformanceTiming.prototype.unloadEventEnd",
     "PerformanceTiming.prototype.unloadEventStart",
+    "PerformanceTimingConfidence",
+    "PerformanceTimingConfidence.prototype",
+    "PerformanceTimingConfidence.prototype.randomizedTriggerRate",
+    "PerformanceTimingConfidence.prototype.toJSON",
+    "PerformanceTimingConfidence.prototype.value",
     "PeriodicSyncManager",
     "PeriodicSyncManager.prototype",
     "PeriodicSyncManager.prototype.getTags",
```

  
#### 145.0.7587.4 (`2025-12-22`) ⚡
Added 1 APIs, removed 0 (see: [diff](./browser_apis/chrome-unstable_145.0.7572.2_to_145.0.7587.4.diff), [json](./browser_apis/chrome-unstable_145.0.7572.2_to_145.0.7587.4.json), [full list](./browser_apis/chrome-unstable_145.0.7587.4.json))
 ```diff
--- ./browser_apis/chrome-unstable_145.0.7572.2.json	2025-12-22 20:00:51.264849748 +0000
+++ ./browser_apis/chrome-unstable_145.0.7587.4.json	2025-12-22 20:01:32.157114250 +0000
@@ -1,6 +1,6 @@
 {
   "browser": "chrome-unstable",
-  "browserApiCount": 9147,
+  "browserApiCount": 9148,
   "browserApis": [
     "AbsoluteOrientationSensor",
     "AbsoluteOrientationSensor.prototype",
@@ -7447,6 +7447,7 @@
     "VideoFrame.prototype.duration",
     "VideoFrame.prototype.flip",
     "VideoFrame.prototype.format",
+    "VideoFrame.prototype.metadata",
     "VideoFrame.prototype.rotation",
     "VideoFrame.prototype.timestamp",
     "VideoFrame.prototype.visibleRect",
```

  
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

  <!-- browserapis:end -->
