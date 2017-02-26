# com-chilipeppr-widget-autolevel
Allows you to auto-level your PCB or other conductive surface before milling. Most raw PCB boards or other surfaces have a slight warpage. This widget lets you probe the warpage and then it auto-scales your Gcode to match the warpage so you get very clean/predictable z-positions in your milling job.

![alt text](screenshot.png "Screenshot")

## ChiliPeppr Widget / Auto-Level

All ChiliPeppr widgets/elements are defined using cpdefine() which is a method
that mimics require.js. Each defined object must have a unique ID so it does
not conflict with other ChiliPeppr widgets.

| Item                  | Value           |
| -------------         | ------------- | 
| ID                    | com-chilipeppr-widget-autolevel |
| Name                  | Widget / Auto-Level |
| Description           | Allows you to auto-level your PCB or other conductive surface before milling. Most raw PCB boards or other surfaces have a slight warpage. This widget lets you probe the warpage and then it auto-scales your Gcode to match the warpage so you get very clean/predictable z-positions in your milling job. |
| chilipeppr.load() URL | http://raw.githubusercontent.com/chilipeppr/widget-autolevel/master/auto-generated-widget.html |
| Edit URL              | http://ide.c9.io/chilipeppr/widget-autolevel |
| Github URL            | http://github.com/chilipeppr/widget-autolevel |
| Test URL              | https://preview.c9users.io/chilipeppr/widget-autolevel/widget.html |

## Example Code for chilipeppr.load() Statement

You can use the code below as a starting point for instantiating this widget 
inside a workspace or from another widget. The key is that you need to load 
your widget inlined into a div so the DOM can parse your HTML, CSS, and 
Javascript. Then you use cprequire() to find your widget's Javascript and get 
back the instance of it.

```javascript
// Inject new div to contain widget or use an existing div with an ID
$("body").append('<' + 'div id="myDivWidgetAutolevel"><' + '/div>');

chilipeppr.load(
  "#myDivWidgetAutolevel",
  "http://raw.githubusercontent.com/chilipeppr/widget-autolevel/master/auto-generated-widget.html",
  function() {
    // Callback after widget loaded into #myDivWidgetAutolevel
    // Now use require.js to get reference to instantiated widget
    cprequire(
      ["inline:com-chilipeppr-widget-autolevel"], // the id you gave your widget
      function(myObjWidgetAutolevel) {
        // Callback that is passed reference to the newly loaded widget
        console.log("Widget / Auto-Level just got loaded.", myObjWidgetAutolevel);
        myObjWidgetAutolevel.init();
      }
    );
  }
);

```

## Publish

This widget/element publishes the following signals. These signals are owned by this widget/element and are published to all objects inside the ChiliPeppr environment that listen to them via the 
chilipeppr.subscribe(signal, callback) method. 
To better understand how ChiliPeppr's subscribe() method works see amplify.js's documentation at http://amplifyjs.com/api/pubsub/

  <table id="com-chilipeppr-elem-pubsubviewer-pub" class="table table-bordered table-striped">
      <thead>
          <tr>
              <th style="">Signal</th>
              <th style="">Description</th>
          </tr>
      </thead>
      <tbody>
      <tr><td colspan="2">(No signals defined in this widget/element)</td></tr>    
      </tbody>
  </table>

## Subscribe

This widget/element subscribes to the following signals. These signals are owned by this widget/element. Other objects inside the ChiliPeppr environment can publish to these signals via the chilipeppr.publish(signal, data) method. 
To better understand how ChiliPeppr's publish() method works see amplify.js's documentation at http://amplifyjs.com/api/pubsub/

  <table id="com-chilipeppr-elem-pubsubviewer-sub" class="table table-bordered table-striped">
      <thead>
          <tr>
              <th style="">Signal</th>
              <th style="">Description</th>
          </tr>
      </thead>
      <tbody>
      <tr><td colspan="2">(No signals defined in this widget/element)</td></tr>    
      </tbody>
  </table>

## Foreign Publish

This widget/element publishes to the following signals that are owned by other objects. 
To better understand how ChiliPeppr's subscribe() method works see amplify.js's documentation at http://amplifyjs.com/api/pubsub/

  <table id="com-chilipeppr-elem-pubsubviewer-foreignpub" class="table table-bordered table-striped">
      <thead>
          <tr>
              <th style="">Signal</th>
              <th style="">Description</th>
          </tr>
      </thead>
      <tbody>
      <tr valign="top"><td>/com-chilipeppr-widget-autolevel/com-chilipeppr-widget-3dviewer/sceneadd</td><td>We ask the 3D viewer to add THREE.js objects to the scene.</td></tr><tr valign="top"><td>/com-chilipeppr-widget-autolevel/com-chilipeppr-widget-3dviewer/sceneremove</td><td>We ask the 3D viewer to remove THREE.js objects from the scene.</td></tr><tr valign="top"><td>/com-chilipeppr-widget-autolevel/com-chilipeppr-widget-3dviewer/request3dObject</td><td>We ask the 3D viewer to send us the user object being shown in 3D viewer so we can analyze it. In particular, we want to know its bounding box for calculating the probe area.</td></tr>    
      </tbody>
  </table>

## Foreign Subscribe

This widget/element publishes to the following signals that are owned by other objects.
To better understand how ChiliPeppr's publish() method works see amplify.js's documentation at http://amplifyjs.com/api/pubsub/

  <table id="com-chilipeppr-elem-pubsubviewer-foreignsub" class="table table-bordered table-striped">
      <thead>
          <tr>
              <th style="">Signal</th>
              <th style="">Description</th>
          </tr>
      </thead>
      <tbody>
      <tr valign="top"><td>/com-chilipeppr-widget-autolevel/com-chilipeppr-widget-3dviewer/recv3dObject</td><td>When we request a /com-chilipeppr-widget-3dviewer/request3dObject we get back this signal and the payload is the actual user object so we can analyze it.</td></tr>    
      </tbody>
  </table>

## Methods / Properties

The table below shows, in order, the methods and properties inside the widget/element.

  <table id="com-chilipeppr-elem-methodsprops" class="table table-bordered table-striped">
      <thead>
          <tr>
              <th style="">Method / Property</th>
              <th>Type</th>
              <th style="">Description</th>
          </tr>
      </thead>
      <tbody>
      <tr valign="top"><td>id</td><td>string</td><td>"com-chilipeppr-widget-autolevel"</td></tr><tr valign="top"><td>url</td><td>string</td><td>"http://raw.githubusercontent.com/chilipeppr/widget-autolevel/master/auto-generated-widget.html"</td></tr><tr valign="top"><td>fiddleurl</td><td>string</td><td>"http://ide.c9.io/chilipeppr/widget-autolevel"</td></tr><tr valign="top"><td>githuburl</td><td>string</td><td>"http://github.com/chilipeppr/widget-autolevel"</td></tr><tr valign="top"><td>testurl</td><td>string</td><td>"http://widget-autolevel-chilipeppr.c9users.io/widget.html"</td></tr><tr valign="top"><td>name</td><td>string</td><td>"Widget / Auto-Level"</td></tr><tr valign="top"><td>desc</td><td>string</td><td>"Allows you to auto-level your PCB or other conductive surface before milling. Most raw PCB boards or other surfaces have a slight warpage. This widget lets you probe the warpage and then it auto-scales your Gcode to match the warpage so you get very clean/predictable z-positions in your milling job."</td></tr><tr valign="top"><td>publish</td><td>object</td><td>Please see docs above.</td></tr><tr valign="top"><td>subscribe</td><td>object</td><td>Please see docs above.</td></tr><tr valign="top"><td>foreignPublish</td><td>object</td><td>Please see docs above.</td></tr><tr valign="top"><td>foreignSubscribe</td><td>object</td><td>Please see docs above.</td></tr><tr valign="top"><td>init</td><td>function</td><td>function () </td></tr><tr valign="top"><td>showData</td><td>function</td><td>function () </td></tr><tr valign="top"><td>loadText</td><td>function</td><td>function () </td></tr><tr valign="top"><td>deleteRecentFiles</td><td>function</td><td>function () </td></tr><tr valign="top"><td>createRecentFileEntry</td><td>function</td><td>function (fileStr, info) </td></tr><tr valign="top"><td>buildRecentFileMenu</td><td>function</td><td>function () </td></tr><tr valign="top"><td>loadFileFromLocalStorageKey</td><td>function</td><td>function (key) </td></tr><tr valign="top"><td>loadTestData</td><td>function</td><td>function (data) </td></tr><tr valign="top"><td>matrix</td><td>object</td><td></td></tr><tr valign="top"><td>previousLayerOpacities</td><td>object</td><td></td></tr><tr valign="top"><td>toggleShowMatrix</td><td>function</td><td>function () </td></tr><tr valign="top"><td>isMatrixShowing</td><td>boolean</td><td></td></tr><tr valign="top"><td>showProbeMatrix</td><td>function</td><td>function () </td></tr><tr valign="top"><td>hideProbeMatrix</td><td>function</td><td>function () </td></tr><tr valign="top"><td>refreshProbeMatrix</td><td>function</td><td>function () </td></tr><tr valign="top"><td>isFadeOutUserObject</td><td>boolean</td><td></td></tr><tr valign="top"><td>fadeOutUserObject</td><td>function</td><td>function () </td></tr><tr valign="top"><td>fadeOutUserObjectJustinVersion</td><td>function</td><td>function () </td></tr><tr valign="top"><td>unfadeOutUserObject</td><td>function</td><td>function () </td></tr><tr valign="top"><td>sendGcodeToWorkspace</td><td>function</td><td>function () </td></tr><tr valign="top"><td>envelopeView</td><td>function</td><td>function (evt, opts) </td></tr><tr valign="top"><td>autolevelledGcode</td><td>object</td><td></td></tr><tr valign="top"><td>envelope</td><td>function</td><td>function (options) </td></tr><tr valign="top"><td>getUnitMesh</td><td>function</td><td>function () </td></tr><tr valign="top"><td>rayCast</td><td>function</td><td>function () </td></tr><tr valign="top"><td>exaggerateMult</td><td>number</td><td></td></tr><tr valign="top"><td>setExaggerate</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>probeMesh</td><td>object</td><td></td></tr><tr valign="top"><td>drawMatrix</td><td>function</td><td>function () </td></tr><tr valign="top"><td>removeMatrix</td><td>function</td><td>function () </td></tr><tr valign="top"><td>onDisplay</td><td>function</td><td>function () </td></tr><tr valign="top"><td>onUndisplay</td><td>function</td><td>function () </td></tr><tr valign="top"><td>runTestProbe</td><td>function</td><td>function () </td></tr><tr valign="top"><td>startAutoLevel</td><td>function</td><td>function () </td></tr><tr valign="top"><td>stopAutoLevel</td><td>function</td><td>function () </td></tr><tr valign="top"><td>formUpdate</td><td>function</td><td>function () </td></tr><tr valign="top"><td>probes</td><td>object</td><td></td></tr><tr valign="top"><td>maxx</td><td>object</td><td></td></tr><tr valign="top"><td>maxy</td><td>object</td><td></td></tr><tr valign="top"><td>genProbeGcode</td><td>function</td><td>function () </td></tr><tr valign="top"><td>modalComplete</td><td>function</td><td>function () </td></tr><tr valign="top"><td>genProbeSteps</td><td>function</td><td>function () </td></tr><tr valign="top"><td>currentStep</td><td>object</td><td></td></tr><tr valign="top"><td>isPaused</td><td>boolean</td><td></td></tr><tr valign="top"><td>pause</td><td>function</td><td>function () </td></tr><tr valign="top"><td>doNextStep</td><td>function</td><td>function () </td></tr><tr valign="top"><td>watchZ</td><td>function</td><td>function (probe, donecallback) </td></tr><tr valign="top"><td>isSubToRecvline</td><td>boolean</td><td></td></tr><tr valign="top"><td>autolevelLineCtr</td><td>number</td><td></td></tr><tr valign="top"><td>send</td><td>function</td><td>function (gcode) </td></tr><tr valign="top"><td>statEl</td><td>object</td><td></td></tr><tr valign="top"><td>status</td><td>function</td><td>function (txt) </td></tr><tr valign="top"><td>zsettings</td><td>object</td><td></td></tr><tr valign="top"><td>modalStart</td><td>function</td><td>function () </td></tr><tr valign="top"><td>getZMinSettings</td><td>function</td><td>function (donecallback) </td></tr><tr valign="top"><td>autoFillData</td><td>function</td><td>function () </td></tr><tr valign="top"><td>user3dObject</td><td>object</td><td></td></tr><tr valign="top"><td>recv3dObject</td><td>function</td><td>function (obj) </td></tr><tr valign="top"><td>get3dObjectFrom3dViewer</td><td>function</td><td>function () </td></tr><tr valign="top"><td>bboxHelper</td><td>object</td><td></td></tr><tr valign="top"><td>getBbox</td><td>function</td><td>function () </td></tr><tr valign="top"><td>calcSteps</td><td>function</td><td>function () </td></tr><tr valign="top"><td>toggleProbeArea</td><td>function</td><td>function () </td></tr><tr valign="top"><td>regionObj</td><td>object</td><td></td></tr><tr valign="top"><td>isRegionShowing</td><td>boolean</td><td></td></tr><tr valign="top"><td>addRegionTo3d</td><td>function</td><td>function () </td></tr><tr valign="top"><td>removeRegionFrom3d</td><td>function</td><td>function () </td></tr><tr valign="top"><td>makeSprite</td><td>function</td><td>function (vals) </td></tr><tr valign="top"><td>makeSpriteOld</td><td>function</td><td>function (vals) </td></tr><tr valign="top"><td>makeSprite2</td><td>function</td><td>function (vals) </td></tr><tr valign="top"><td>createText</td><td>function</td><td>function (text) </td></tr><tr valign="top"><td>forkSetup</td><td>function</td><td>function () </td></tr>
      </tbody>
  </table>


## About ChiliPeppr

[ChiliPeppr](http://chilipeppr.com) is a hardware fiddle, meaning it is a 
website that lets you easily
create a workspace to fiddle with your hardware from software. ChiliPeppr provides
a [Serial Port JSON Server](https://github.com/johnlauer/serial-port-json-server) 
that you run locally on your computer, or remotely on another computer, to connect to 
the serial port of your hardware like an Arduino or other microcontroller.

You then create a workspace at ChiliPeppr.com that connects to your hardware 
by starting from scratch or forking somebody else's
workspace that is close to what you are after. Then you write widgets in
Javascript that interact with your hardware by forking the base template 
widget or forking another widget that
is similar to what you are trying to build.

ChiliPeppr is massively capable such that the workspaces for 
[TinyG](http://chilipeppr.com/tinyg) and [Grbl](http://chilipeppr.com/grbl) CNC 
controllers have become full-fledged CNC machine management software used by
tens of thousands.

ChiliPeppr has inspired many people in the hardware/software world to use the
browser and Javascript as the foundation for interacting with hardware. The
Arduino team in Italy caught wind of ChiliPeppr and now
ChiliPeppr's Serial Port JSON Server is the basis for the 
[Arduino's new web IDE](https://create.arduino.cc/). If the Arduino team is excited about building on top
of ChiliPeppr, what
will you build on top of it?

