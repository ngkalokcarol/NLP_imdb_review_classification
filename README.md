# NLP_imdb_review_classification

<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />

<title>temp-166082918636927600</title>

<script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>



<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.7.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.7.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.7.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff2?v=4.7.0') format('woff2'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.7.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.7.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.7.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.fa-pull-left {
  float: left;
}
.fa-pull-right {
  float: right;
}
.fa.fa-pull-left {
  margin-right: .3em;
}
.fa.fa-pull-right {
  margin-left: .3em;
}
/* Deprecated as of 4.4.0 */
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
.fa-pulse {
  -webkit-animation: fa-spin 1s infinite steps(8);
  animation: fa-spin 1s infinite steps(8);
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=1)";
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2)";
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=3)";
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1)";
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1)";
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook-f:before,
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-feed:before,
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before,
.fa-gratipay:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper-pp:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-resistance:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-y-combinator-square:before,
.fa-yc-square:before,
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
.fa-buysellads:before {
  content: "\f20d";
}
.fa-connectdevelop:before {
  content: "\f20e";
}
.fa-dashcube:before {
  content: "\f210";
}
.fa-forumbee:before {
  content: "\f211";
}
.fa-leanpub:before {
  content: "\f212";
}
.fa-sellsy:before {
  content: "\f213";
}
.fa-shirtsinbulk:before {
  content: "\f214";
}
.fa-simplybuilt:before {
  content: "\f215";
}
.fa-skyatlas:before {
  content: "\f216";
}
.fa-cart-plus:before {
  content: "\f217";
}
.fa-cart-arrow-down:before {
  content: "\f218";
}
.fa-diamond:before {
  content: "\f219";
}
.fa-ship:before {
  content: "\f21a";
}
.fa-user-secret:before {
  content: "\f21b";
}
.fa-motorcycle:before {
  content: "\f21c";
}
.fa-street-view:before {
  content: "\f21d";
}
.fa-heartbeat:before {
  content: "\f21e";
}
.fa-venus:before {
  content: "\f221";
}
.fa-mars:before {
  content: "\f222";
}
.fa-mercury:before {
  content: "\f223";
}
.fa-intersex:before,
.fa-transgender:before {
  content: "\f224";
}
.fa-transgender-alt:before {
  content: "\f225";
}
.fa-venus-double:before {
  content: "\f226";
}
.fa-mars-double:before {
  content: "\f227";
}
.fa-venus-mars:before {
  content: "\f228";
}
.fa-mars-stroke:before {
  content: "\f229";
}
.fa-mars-stroke-v:before {
  content: "\f22a";
}
.fa-mars-stroke-h:before {
  content: "\f22b";
}
.fa-neuter:before {
  content: "\f22c";
}
.fa-genderless:before {
  content: "\f22d";
}
.fa-facebook-official:before {
  content: "\f230";
}
.fa-pinterest-p:before {
  content: "\f231";
}
.fa-whatsapp:before {
  content: "\f232";
}
.fa-server:before {
  content: "\f233";
}
.fa-user-plus:before {
  content: "\f234";
}
.fa-user-times:before {
  content: "\f235";
}
.fa-hotel:before,
.fa-bed:before {
  content: "\f236";
}
.fa-viacoin:before {
  content: "\f237";
}
.fa-train:before {
  content: "\f238";
}
.fa-subway:before {
  content: "\f239";
}
.fa-medium:before {
  content: "\f23a";
}
.fa-yc:before,
.fa-y-combinator:before {
  content: "\f23b";
}
.fa-optin-monster:before {
  content: "\f23c";
}
.fa-opencart:before {
  content: "\f23d";
}
.fa-expeditedssl:before {
  content: "\f23e";
}
.fa-battery-4:before,
.fa-battery:before,
.fa-battery-full:before {
  content: "\f240";
}
.fa-battery-3:before,
.fa-battery-three-quarters:before {
  content: "\f241";
}
.fa-battery-2:before,
.fa-battery-half:before {
  content: "\f242";
}
.fa-battery-1:before,
.fa-battery-quarter:before {
  content: "\f243";
}
.fa-battery-0:before,
.fa-battery-empty:before {
  content: "\f244";
}
.fa-mouse-pointer:before {
  content: "\f245";
}
.fa-i-cursor:before {
  content: "\f246";
}
.fa-object-group:before {
  content: "\f247";
}
.fa-object-ungroup:before {
  content: "\f248";
}
.fa-sticky-note:before {
  content: "\f249";
}
.fa-sticky-note-o:before {
  content: "\f24a";
}
.fa-cc-jcb:before {
  content: "\f24b";
}
.fa-cc-diners-club:before {
  content: "\f24c";
}
.fa-clone:before {
  content: "\f24d";
}
.fa-balance-scale:before {
  content: "\f24e";
}
.fa-hourglass-o:before {
  content: "\f250";
}
.fa-hourglass-1:before,
.fa-hourglass-start:before {
  content: "\f251";
}
.fa-hourglass-2:before,
.fa-hourglass-half:before {
  content: "\f252";
}
.fa-hourglass-3:before,
.fa-hourglass-end:before {
  content: "\f253";
}
.fa-hourglass:before {
  content: "\f254";
}
.fa-hand-grab-o:before,
.fa-hand-rock-o:before {
  content: "\f255";
}
.fa-hand-stop-o:before,
.fa-hand-paper-o:before {
  content: "\f256";
}
.fa-hand-scissors-o:before {
  content: "\f257";
}
.fa-hand-lizard-o:before {
  content: "\f258";
}
.fa-hand-spock-o:before {
  content: "\f259";
}
.fa-hand-pointer-o:before {
  content: "\f25a";
}
.fa-hand-peace-o:before {
  content: "\f25b";
}
.fa-trademark:before {
  content: "\f25c";
}
.fa-registered:before {
  content: "\f25d";
}
.fa-creative-commons:before {
  content: "\f25e";
}
.fa-gg:before {
  content: "\f260";
}
.fa-gg-circle:before {
  content: "\f261";
}
.fa-tripadvisor:before {
  content: "\f262";
}
.fa-odnoklassniki:before {
  content: "\f263";
}
.fa-odnoklassniki-square:before {
  content: "\f264";
}
.fa-get-pocket:before {
  content: "\f265";
}
.fa-wikipedia-w:before {
  content: "\f266";
}
.fa-safari:before {
  content: "\f267";
}
.fa-chrome:before {
  content: "\f268";
}
.fa-firefox:before {
  content: "\f269";
}
.fa-opera:before {
  content: "\f26a";
}
.fa-internet-explorer:before {
  content: "\f26b";
}
.fa-tv:before,
.fa-television:before {
  content: "\f26c";
}
.fa-contao:before {
  content: "\f26d";
}
.fa-500px:before {
  content: "\f26e";
}
.fa-amazon:before {
  content: "\f270";
}
.fa-calendar-plus-o:before {
  content: "\f271";
}
.fa-calendar-minus-o:before {
  content: "\f272";
}
.fa-calendar-times-o:before {
  content: "\f273";
}
.fa-calendar-check-o:before {
  content: "\f274";
}
.fa-industry:before {
  content: "\f275";
}
.fa-map-pin:before {
  content: "\f276";
}
.fa-map-signs:before {
  content: "\f277";
}
.fa-map-o:before {
  content: "\f278";
}
.fa-map:before {
  content: "\f279";
}
.fa-commenting:before {
  content: "\f27a";
}
.fa-commenting-o:before {
  content: "\f27b";
}
.fa-houzz:before {
  content: "\f27c";
}
.fa-vimeo:before {
  content: "\f27d";
}
.fa-black-tie:before {
  content: "\f27e";
}
.fa-fonticons:before {
  content: "\f280";
}
.fa-reddit-alien:before {
  content: "\f281";
}
.fa-edge:before {
  content: "\f282";
}
.fa-credit-card-alt:before {
  content: "\f283";
}
.fa-codiepie:before {
  content: "\f284";
}
.fa-modx:before {
  content: "\f285";
}
.fa-fort-awesome:before {
  content: "\f286";
}
.fa-usb:before {
  content: "\f287";
}
.fa-product-hunt:before {
  content: "\f288";
}
.fa-mixcloud:before {
  content: "\f289";
}
.fa-scribd:before {
  content: "\f28a";
}
.fa-pause-circle:before {
  content: "\f28b";
}
.fa-pause-circle-o:before {
  content: "\f28c";
}
.fa-stop-circle:before {
  content: "\f28d";
}
.fa-stop-circle-o:before {
  content: "\f28e";
}
.fa-shopping-bag:before {
  content: "\f290";
}
.fa-shopping-basket:before {
  content: "\f291";
}
.fa-hashtag:before {
  content: "\f292";
}
.fa-bluetooth:before {
  content: "\f293";
}
.fa-bluetooth-b:before {
  content: "\f294";
}
.fa-percent:before {
  content: "\f295";
}
.fa-gitlab:before {
  content: "\f296";
}
.fa-wpbeginner:before {
  content: "\f297";
}
.fa-wpforms:before {
  content: "\f298";
}
.fa-envira:before {
  content: "\f299";
}
.fa-universal-access:before {
  content: "\f29a";
}
.fa-wheelchair-alt:before {
  content: "\f29b";
}
.fa-question-circle-o:before {
  content: "\f29c";
}
.fa-blind:before {
  content: "\f29d";
}
.fa-audio-description:before {
  content: "\f29e";
}
.fa-volume-control-phone:before {
  content: "\f2a0";
}
.fa-braille:before {
  content: "\f2a1";
}
.fa-assistive-listening-systems:before {
  content: "\f2a2";
}
.fa-asl-interpreting:before,
.fa-american-sign-language-interpreting:before {
  content: "\f2a3";
}
.fa-deafness:before,
.fa-hard-of-hearing:before,
.fa-deaf:before {
  content: "\f2a4";
}
.fa-glide:before {
  content: "\f2a5";
}
.fa-glide-g:before {
  content: "\f2a6";
}
.fa-signing:before,
.fa-sign-language:before {
  content: "\f2a7";
}
.fa-low-vision:before {
  content: "\f2a8";
}
.fa-viadeo:before {
  content: "\f2a9";
}
.fa-viadeo-square:before {
  content: "\f2aa";
}
.fa-snapchat:before {
  content: "\f2ab";
}
.fa-snapchat-ghost:before {
  content: "\f2ac";
}
.fa-snapchat-square:before {
  content: "\f2ad";
}
.fa-pied-piper:before {
  content: "\f2ae";
}
.fa-first-order:before {
  content: "\f2b0";
}
.fa-yoast:before {
  content: "\f2b1";
}
.fa-themeisle:before {
  content: "\f2b2";
}
.fa-google-plus-circle:before,
.fa-google-plus-official:before {
  content: "\f2b3";
}
.fa-fa:before,
.fa-font-awesome:before {
  content: "\f2b4";
}
.fa-handshake-o:before {
  content: "\f2b5";
}
.fa-envelope-open:before {
  content: "\f2b6";
}
.fa-envelope-open-o:before {
  content: "\f2b7";
}
.fa-linode:before {
  content: "\f2b8";
}
.fa-address-book:before {
  content: "\f2b9";
}
.fa-address-book-o:before {
  content: "\f2ba";
}
.fa-vcard:before,
.fa-address-card:before {
  content: "\f2bb";
}
.fa-vcard-o:before,
.fa-address-card-o:before {
  content: "\f2bc";
}
.fa-user-circle:before {
  content: "\f2bd";
}
.fa-user-circle-o:before {
  content: "\f2be";
}
.fa-user-o:before {
  content: "\f2c0";
}
.fa-id-badge:before {
  content: "\f2c1";
}
.fa-drivers-license:before,
.fa-id-card:before {
  content: "\f2c2";
}
.fa-drivers-license-o:before,
.fa-id-card-o:before {
  content: "\f2c3";
}
.fa-quora:before {
  content: "\f2c4";
}
.fa-free-code-camp:before {
  content: "\f2c5";
}
.fa-telegram:before {
  content: "\f2c6";
}
.fa-thermometer-4:before,
.fa-thermometer:before,
.fa-thermometer-full:before {
  content: "\f2c7";
}
.fa-thermometer-3:before,
.fa-thermometer-three-quarters:before {
  content: "\f2c8";
}
.fa-thermometer-2:before,
.fa-thermometer-half:before {
  content: "\f2c9";
}
.fa-thermometer-1:before,
.fa-thermometer-quarter:before {
  content: "\f2ca";
}
.fa-thermometer-0:before,
.fa-thermometer-empty:before {
  content: "\f2cb";
}
.fa-shower:before {
  content: "\f2cc";
}
.fa-bathtub:before,
.fa-s15:before,
.fa-bath:before {
  content: "\f2cd";
}
.fa-podcast:before {
  content: "\f2ce";
}
.fa-window-maximize:before {
  content: "\f2d0";
}
.fa-window-minimize:before {
  content: "\f2d1";
}
.fa-window-restore:before {
  content: "\f2d2";
}
.fa-times-rectangle:before,
.fa-window-close:before {
  content: "\f2d3";
}
.fa-times-rectangle-o:before,
.fa-window-close-o:before {
  content: "\f2d4";
}
.fa-bandcamp:before {
  content: "\f2d5";
}
.fa-grav:before {
  content: "\f2d6";
}
.fa-etsy:before {
  content: "\f2d7";
}
.fa-imdb:before {
  content: "\f2d8";
}
.fa-ravelry:before {
  content: "\f2d9";
}
.fa-eercast:before {
  content: "\f2da";
}
.fa-microchip:before {
  content: "\f2db";
}
.fa-snowflake-o:before {
  content: "\f2dc";
}
.fa-superpowers:before {
  content: "\f2dd";
}
.fa-wpexplorer:before {
  content: "\f2de";
}
.fa-meetup:before {
  content: "\f2e0";
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
div.traceback-wrapper pre.traceback {
  max-height: 600px;
  overflow: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 5px;
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
[dir="rtl"] #ipython_notebook {
  margin-right: 10px;
  margin-left: 0;
}
[dir="rtl"] #ipython_notebook.pull-left {
  float: right !important;
  float: right;
}
.flex-spacer {
  flex: 1;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#kernel_logo_widget {
  margin: 0 10px;
}
span#login_widget {
  float: right;
}
[dir="rtl"] span#login_widget {
  float: left;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
.modal-header {
  cursor: move;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
[dir="rtl"] .center-nav form.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] .center-nav .navbar-text {
  float: right;
}
[dir="rtl"] .navbar-inner {
  text-align: right;
}
[dir="rtl"] div.text-left {
  text-align: right;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  position: absolute;
  display: block;
  width: 100%;
  height: 100%;
  overflow: hidden;
  cursor: pointer;
  opacity: 0;
  z-index: 2;
}
.alternate_upload .btn-xs > input.fileinput {
  margin: -1px -5px;
}
.alternate_upload .btn-upload {
  position: relative;
  height: 22px;
}
::-webkit-file-upload-button {
  cursor: pointer;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
ul#tabs {
  margin-bottom: 4px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
[dir="rtl"] ul#tabs.nav-tabs > li {
  float: right;
}
[dir="rtl"] ul#tabs.nav.nav-tabs {
  padding-right: 0;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons .pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .list_toolbar .col-sm-4,
[dir="rtl"] .list_toolbar .col-sm-8 {
  float: right;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: text-bottom;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
[dir="rtl"] .list_item > div input {
  margin-right: 0;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_modified {
  margin-right: 7px;
  margin-left: 7px;
}
[dir="rtl"] .item_modified.pull-right {
  float: left !important;
  float: left;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
[dir="rtl"] .item_buttons.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .item_buttons .kernel-name {
  margin-left: 7px;
  float: right;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
.sort_button {
  display: inline-block;
  padding-left: 7px;
}
[dir="rtl"] .sort_button.pull-right {
  float: left !important;
  float: left;
}
#tree-selector {
  padding-right: 0px;
}
#button-select-all {
  min-width: 50px;
}
[dir="rtl"] #button-select-all.btn {
  float: right ;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
  margin-top: 2px;
  height: 16px;
}
[dir="rtl"] #select-all.pull-left {
  float: right !important;
  float: right;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.fa-pull-left {
  margin-right: .3em;
}
.folder_icon:before.fa-pull-right {
  margin-left: .3em;
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.fa-pull-left {
  margin-right: .3em;
}
.file_icon:before.fa-pull-right {
  margin-left: .3em;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
#new-menu .dropdown-header {
  font-size: 10px;
  border-bottom: 1px solid #e5e5e5;
  padding: 0 0 3px;
  margin: -3px 20px 0;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.move-button {
  display: none;
}
.download-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
.CodeMirror-dialog {
  background-color: #fff;
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI escape sequences */
/* The color values are a mix of
   http://www.xcolors.net/dl/baskerville-ivorylight and
   http://www.xcolors.net/dl/euphrasia */
.ansi-black-fg {
  color: #3E424D;
}
.ansi-black-bg {
  background-color: #3E424D;
}
.ansi-black-intense-fg {
  color: #282C36;
}
.ansi-black-intense-bg {
  background-color: #282C36;
}
.ansi-red-fg {
  color: #E75C58;
}
.ansi-red-bg {
  background-color: #E75C58;
}
.ansi-red-intense-fg {
  color: #B22B31;
}
.ansi-red-intense-bg {
  background-color: #B22B31;
}
.ansi-green-fg {
  color: #00A250;
}
.ansi-green-bg {
  background-color: #00A250;
}
.ansi-green-intense-fg {
  color: #007427;
}
.ansi-green-intense-bg {
  background-color: #007427;
}
.ansi-yellow-fg {
  color: #DDB62B;
}
.ansi-yellow-bg {
  background-color: #DDB62B;
}
.ansi-yellow-intense-fg {
  color: #B27D12;
}
.ansi-yellow-intense-bg {
  background-color: #B27D12;
}
.ansi-blue-fg {
  color: #208FFB;
}
.ansi-blue-bg {
  background-color: #208FFB;
}
.ansi-blue-intense-fg {
  color: #0065CA;
}
.ansi-blue-intense-bg {
  background-color: #0065CA;
}
.ansi-magenta-fg {
  color: #D160C4;
}
.ansi-magenta-bg {
  background-color: #D160C4;
}
.ansi-magenta-intense-fg {
  color: #A03196;
}
.ansi-magenta-intense-bg {
  background-color: #A03196;
}
.ansi-cyan-fg {
  color: #60C6C8;
}
.ansi-cyan-bg {
  background-color: #60C6C8;
}
.ansi-cyan-intense-fg {
  color: #258F8F;
}
.ansi-cyan-intense-bg {
  background-color: #258F8F;
}
.ansi-white-fg {
  color: #C5C1B4;
}
.ansi-white-bg {
  background-color: #C5C1B4;
}
.ansi-white-intense-fg {
  color: #A1A6B2;
}
.ansi-white-intense-bg {
  background-color: #A1A6B2;
}
.ansi-default-inverse-fg {
  color: #FFFFFF;
}
.ansi-default-inverse-bg {
  background-color: #000000;
}
.ansi-bold {
  font-weight: bold;
}
.ansi-underline {
  text-decoration: underline;
}
/* The following styles are deprecated an will be removed in a future version */
.ansibold {
  font-weight: bold;
}
.ansi-inverse {
  outline: 0.5px dotted;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  position: relative;
  overflow: visible;
}
div.cell:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: transparent;
}
div.cell.jupyter-soft-selected {
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected,
div.cell.selected.jupyter-soft-selected {
  border-color: #ababab;
}
div.cell.selected:before,
div.cell.selected.jupyter-soft-selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #42A5F5;
}
@media print {
  div.cell.selected,
  div.cell.selected.jupyter-soft-selected {
    border-color: transparent;
  }
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
}
.edit_mode div.cell.selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #66BB6A;
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  /* Note that this should set vertical padding only, since CodeMirror assumes
       that horizontal padding will be set on CodeMirror pre */
  padding: 0.4em 0;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. This sets horizontal padding only,
    use .CodeMirror-lines for vertical */
  padding: 0 0.4em;
  border: 0;
  border-radius: 0;
}
.CodeMirror-cursor {
  border-left: 1.4px solid black;
}
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .CodeMirror-cursor {
    border-left: 2px solid black;
  }
}
@media screen and (min-width: 4320px) {
  .CodeMirror-cursor {
    border-left: 4px solid black;
  }
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
div.output_area .mglyph > img {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 1px 0 1px 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul:not(.list-inline),
.rendered_html ol:not(.list-inline) {
  padding-left: 2em;
}
.rendered_html ul {
  list-style: disc;
}
.rendered_html ul ul {
  list-style: square;
  margin-top: 0;
}
.rendered_html ul ul ul {
  list-style: circle;
}
.rendered_html ol {
  list-style: decimal;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin-top: 0;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
  padding: 0px;
  background-color: #fff;
}
.rendered_html code {
  background-color: #eff0f1;
}
.rendered_html p code {
  padding: 1px 5px;
}
.rendered_html pre code {
  background-color: #fff;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  color: #000;
  font-size: 100%;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: none;
  border-collapse: collapse;
  border-spacing: 0;
  color: black;
  font-size: 12px;
  table-layout: fixed;
}
.rendered_html thead {
  border-bottom: 1px solid black;
  vertical-align: bottom;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  text-align: right;
  vertical-align: middle;
  padding: 0.5em 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html tbody tr:nth-child(odd) {
  background: #f5f5f5;
}
.rendered_html tbody tr:hover {
  background: rgba(66, 165, 245, 0.2);
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
.rendered_html .alert {
  margin-bottom: initial;
}
.rendered_html * + .alert {
  margin-top: 1em;
}
[dir="rtl"] .rendered_html p {
  text-align: right;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.rendered .rendered_html tr,
.text_cell.rendered .rendered_html th,
.text_cell.rendered .rendered_html td {
  max-width: none;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.text_cell .dropzone .input_area {
  border: 2px dashed #bababa;
  margin: -1px;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
.jupyter-keybindings {
  padding: 1px;
  line-height: 24px;
  border-bottom: 1px solid gray;
}
.jupyter-keybindings input {
  margin: 0;
  padding: 0;
  border: none;
}
.jupyter-keybindings i {
  padding: 6px;
}
.well code {
  background-color: #ffffff;
  border-color: #ababab;
  border-width: 1px;
  border-style: solid;
  padding: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.tags_button_container {
  width: 100%;
  display: flex;
}
.tag-container {
  display: flex;
  flex-direction: row;
  flex-grow: 1;
  overflow: hidden;
  position: relative;
}
.tag-container > * {
  margin: 0 4px;
}
.remove-tag-btn {
  margin-left: 4px;
}
.tags-input {
  display: flex;
}
.cell-tag:last-child:after {
  content: "";
  position: absolute;
  right: 0;
  width: 40px;
  height: 100%;
  /* Fade to background color of cell toolbar */
  background: linear-gradient(to right, rgba(0, 0, 0, 0), #EEE);
}
.tags-input > * {
  margin-left: 4px;
}
.cell-tag,
.tags-input input,
.tags-input button {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  box-shadow: none;
  width: inherit;
  font-size: inherit;
  height: 22px;
  line-height: 22px;
  padding: 0px 4px;
  display: inline-block;
}
.cell-tag:focus,
.tags-input input:focus,
.tags-input button:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.cell-tag::-moz-placeholder,
.tags-input input::-moz-placeholder,
.tags-input button::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.cell-tag:-ms-input-placeholder,
.tags-input input:-ms-input-placeholder,
.tags-input button:-ms-input-placeholder {
  color: #999;
}
.cell-tag::-webkit-input-placeholder,
.tags-input input::-webkit-input-placeholder,
.tags-input button::-webkit-input-placeholder {
  color: #999;
}
.cell-tag::-ms-expand,
.tags-input input::-ms-expand,
.tags-input button::-ms-expand {
  border: 0;
  background-color: transparent;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
.cell-tag[readonly],
.tags-input input[readonly],
.tags-input button[readonly],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  background-color: #eeeeee;
  opacity: 1;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  cursor: not-allowed;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button {
  height: auto;
}
select.cell-tag,
select.tags-input input,
select.tags-input button {
  height: 30px;
  line-height: 30px;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button,
select[multiple].cell-tag,
select[multiple].tags-input input,
select[multiple].tags-input button {
  height: auto;
}
.cell-tag,
.tags-input button {
  padding: 0px 4px;
}
.cell-tag {
  background-color: #fff;
  white-space: nowrap;
}
.tags-input input[type=text]:focus {
  outline: none;
  box-shadow: none;
  border-color: #ccc;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
[dir="rtl"] #kernel_logo_widget {
  float: left !important;
  float: left;
}
.modal .modal-body .move-path {
  display: flex;
  flex-direction: row;
  justify-content: space;
  align-items: center;
}
.modal .modal-body .move-path .server-root {
  padding-right: 20px;
}
.modal .modal-body .move-path .path-input {
  flex: 1;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
[dir="rtl"] #menubar .navbar-toggle {
  float: right;
}
[dir="rtl"] #menubar .navbar-collapse {
  clear: right;
}
[dir="rtl"] #menubar .navbar-nav {
  float: right;
}
[dir="rtl"] #menubar .nav {
  padding-right: 0px;
}
[dir="rtl"] #menubar .navbar-nav > li {
  float: right;
}
[dir="rtl"] #menubar .navbar-right {
  float: left !important;
}
[dir="rtl"] ul.dropdown-menu {
  text-align: right;
  left: auto;
}
[dir="rtl"] ul#new-menu.dropdown-menu {
  right: auto;
  left: 0;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
[dir="rtl"] i.menu-icon.pull-right {
  float: left !important;
  float: left;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
[dir="rtl"] ul#help_menu li a {
  padding-left: 2.2em;
}
[dir="rtl"] ul#help_menu li a i {
  margin-right: 0;
  margin-left: -1.2em;
}
[dir="rtl"] ul#help_menu li a i.pull-right {
  float: left !important;
  float: left;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
[dir="rtl"] .dropdown-submenu > .dropdown-menu {
  right: 100%;
  margin-right: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.fa-pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.fa-pull-right {
  margin-left: .3em;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
[dir="rtl"] .dropdown-submenu > a:after {
  float: left;
  content: "\f0d9";
  margin-right: 0;
  margin-left: -10px;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
[dir="rtl"] #notification_area {
  float: left !important;
  float: left;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] .indicator_area {
  float: left !important;
  float: left;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
[dir="rtl"] #kernel_indicator {
  float: left !important;
  float: left;
  border-left: 0;
  border-right: 1px solid;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] #modal_indicator {
  float: left !important;
  float: left;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  height: 30px;
  margin-top: 4px;
  display: flex;
  justify-content: flex-start;
  align-items: baseline;
  width: 50%;
  flex: 1;
}
span.save_widget span.filename {
  height: 100%;
  line-height: 1em;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  text-overflow: ellipsis;
  overflow: hidden;
  white-space: nowrap;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
[dir="rtl"] span.save_widget.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] span.save_widget span.filename {
  margin-left: 0;
  margin-right: 16px;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
  white-space: nowrap;
  padding: 0 5px;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
    padding: 0 0 0 5px;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
.toolbar-btn-label {
  margin-left: 6px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
[dir="rtl"] .btn-group > .btn,
.btn-group-vertical > .btn {
  float: right;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
[dir="rtl"] ul.typeahead-list i {
  margin-left: 0;
  margin-right: -10px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
ul.typeahead-list  > li > a.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .typeahead-list {
  text-align: right;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  min-width: 20px;
  color: transparent;
}
[dir="rtl"] .no-shortcut.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .command-shortcut.pull-right {
  float: left !important;
  float: left;
}
.command-shortcut:before {
  content: "(command mode)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
[dir="rtl"] .edit-shortcut.pull-right {
  float: left !important;
  float: left;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
[dir="ltr"] #find-and-replace .input-group-btn + .form-control {
  border-left: none;
}
[dir="rtl"] #find-and-replace .input-group-btn + .form-control {
  border-right: none;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>
<style type="text/css">
    
/* Temporary definitions which will become obsolete with Notebook release 5.0 */
.ansi-black-fg { color: #3E424D; }
.ansi-black-bg { background-color: #3E424D; }
.ansi-black-intense-fg { color: #282C36; }
.ansi-black-intense-bg { background-color: #282C36; }
.ansi-red-fg { color: #E75C58; }
.ansi-red-bg { background-color: #E75C58; }
.ansi-red-intense-fg { color: #B22B31; }
.ansi-red-intense-bg { background-color: #B22B31; }
.ansi-green-fg { color: #00A250; }
.ansi-green-bg { background-color: #00A250; }
.ansi-green-intense-fg { color: #007427; }
.ansi-green-intense-bg { background-color: #007427; }
.ansi-yellow-fg { color: #DDB62B; }
.ansi-yellow-bg { background-color: #DDB62B; }
.ansi-yellow-intense-fg { color: #B27D12; }
.ansi-yellow-intense-bg { background-color: #B27D12; }
.ansi-blue-fg { color: #208FFB; }
.ansi-blue-bg { background-color: #208FFB; }
.ansi-blue-intense-fg { color: #0065CA; }
.ansi-blue-intense-bg { background-color: #0065CA; }
.ansi-magenta-fg { color: #D160C4; }
.ansi-magenta-bg { background-color: #D160C4; }
.ansi-magenta-intense-fg { color: #A03196; }
.ansi-magenta-intense-bg { background-color: #A03196; }
.ansi-cyan-fg { color: #60C6C8; }
.ansi-cyan-bg { background-color: #60C6C8; }
.ansi-cyan-intense-fg { color: #258F8F; }
.ansi-cyan-intense-bg { background-color: #258F8F; }
.ansi-white-fg { color: #C5C1B4; }
.ansi-white-bg { background-color: #C5C1B4; }
.ansi-white-intense-fg { color: #A1A6B2; }
.ansi-white-intense-bg { background-color: #A1A6B2; }

.ansi-bold { font-weight: bold; }

    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h4 id="Carol-Ng---MSBA-6460-Final-Report">Carol Ng - MSBA 6460 Final Report<a class="anchor-link" href="#Carol-Ng---MSBA-6460-Final-Report">&#182;</a></h4>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Sentiment-Analysis-with-BERT">Sentiment Analysis with BERT<a class="anchor-link" href="#Sentiment-Analysis-with-BERT">&#182;</a></h2><p>For the project I will use the IMDB review data and will perform the following to train a sentiment analysis model.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="IMDB-Dataset">IMDB Dataset<a class="anchor-link" href="#IMDB-Dataset">&#182;</a></h2><p>IMDB Reviews Dataset is a large movie review dataset. The IMDB Reviews dataset is used for binary sentiment classification, whether a review is positive or negative. It contains 25,000 movie reviews for training and 25,000 for testing. All these 50,000 reviews are labeled data that may be used for supervised deep learning. Besides, there is an additional 50,000 unlabeled reviews.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Process:">Process:<a class="anchor-link" href="#Process:">&#182;</a></h2><ol>
<li>Transformers - Text Preprocessing</li>
<li>Load BERT Classifier and Tokenizer along with Input modules</li>
<li>Download the IMDB Reviews Data</li>
<li>Create a processed dataset</li>
<li>Configure the Loaded BERT model and Train for Fine-tuning</li>
<li>Make Predictions with the Fine-tuned Model</li>
</ol>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="What-is-BERT?">What is BERT?<a class="anchor-link" href="#What-is-BERT?">&#182;</a></h2><p>BERT stands for Bidirectional Encoder Representations from Transformers and it is a state-of-the-art machine learning model used for NLP tasks. Jacob Devlin and his colleagues developed BERT at Google in 2018. Devlin and his colleagues trained the BERT on English Wikipedia (2,500M words) and BooksCorpus (800M words) and achieved the best accuracies for some of the NLP tasks in 2018. There are two pre-trained general BERT variations: The base model is a 12-layer, 768-hidden, 12-heads, 110M parameter neural network architecture, whereas the large model is a 24-layer, 1024-hidden, 16-heads, 340M parameter neural network architecture. Figure 2 shows the visualization of the BERT network created by Devlin et al.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><img src="data:image/png;base64, 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lMhNOjIL5/910WkHbDe2161Xnl5Wmvij79sG4M/fZ/776F3h8IHbLqmuSsWPlvz8/Zd0AnfZaNDUB29KcburbbijC/HpB68fvtva+2670puvPGEbVHewZ9SEOPv4PXbdadu7777r9efvP/HgLX756dvo6kPMQlGZ3vrvkxP3GFdR9PeLL76YHag+cu8NkmtcxSxvHSJUVVlx9w3nnj5xh39tsv5jjz320dvPHLvfJj980+JTlB0i3slIy5f+c8U5E684+/Ajjzj0qisvf+yuyWcdvevcOb92kmxMosMGzMASjE2aeBhMwioMx4R4ShGhczNpwgYzvp323HPPjVll2AkHbvnoXVfW1dakFJOWGYtAF0Xg5x++OumQrZ599MZrr7nqhOOOvmnySeefNGHeX7OTkp35c38//+R9brj0xOOOPfK6a695/rGb6XrSAU0KMymVaE111YO3XXrcAZuNGNLn5ZdfLlv618Q913vl6ftTZ9CdLtZtV5952hE7bLjeGs8///zvMz6buMfY9954NnU60OjHay44+oJT9h2/y/aPPPLQp++/cPSEDdAvKVXQsWXm7z9nnXv8nrdedfrJJ51w5RWXT33g2lMO2ybx/d7YZqqT1Lq2PaMmxKQ9xYR4/vnnJk6cuP766z/91NTxu+xw7gl73jz5lISNczB0ceaROz1x31VXXHHZTTfdOHr06Csuv/zmm29MlnHVyWrR+egfvf0Scwvzfv/+qaemnnD88WuvvfaTTz5x8IH7XnrmwcidJM5coSSen3LXpAkbFmQ3vPTiixMmTNhiiy1eeOH5DdZb45TDt7v/lovQLp3PfscokDQMwAbMwBKMwR5MwioMw3bqaLiOZdCNtWTRvItPP5DOzcknHvfgg/evttpqZ/373w8//ND3X7595N4bfvXJu25I67AIWATai4B07y485oKT99llp23RjJttttnuu+/+yssvj1lphRMP2eremy5gsKm9NDscnrTuu/nCEw7ecvSoIf995eU99thj0003fe65Z+l60gFFHXTLwZpo4KID8/7/PcfU2ayfPn38scfOPfeclVdemf4D9t5/n7nnhAP/9eO3n0ZDJ35h4PDVZx+Cw9LFfzzzzNMnnXTSqquueu8995x33jkP33HpGZN2/P3XH+OXejSUmYdhNmbS3hsygvzSSy8ecfjhdDamPP7YMUdP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" alt="image.png"><img src="data:image/png;base64, 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lMhNOjIL5/910WkHbDe2161Xnl5Wmvij79sG4M/fZ/776F3h8IHbLqmuSsWPlvz8/Zd0AnfZaNDUB29KcburbbijC/HpB68fvtva+2670puvPGEbVHewZ9SEOPv4PXbdadu7777r9efvP/HgLX756dvo6kPMQlGZ3vrvkxP3GFdR9PeLL76YHag+cu8NkmtcxSxvHSJUVVlx9w3nnj5xh39tsv5jjz320dvPHLvfJj980+JTlB0i3slIy5f+c8U5E684+/Ajjzj0qisvf+yuyWcdvevcOb92kmxMosMGzMASjE2aeBhMwioMx4R4ShGhczNpwgYzvp323HPPjVll2AkHbvnoXVfW1dakFJOWGYtAF0Xg5x++OumQrZ599MZrr7nqhOOOvmnySeefNGHeX7OTkp35c38//+R9brj0xOOOPfK6a695/rGb6XrSAU0KMymVaE111YO3XXrcAZuNGNLn5ZdfLlv618Q913vl6ftTZ9CdLtZtV5952hE7bLjeGs8///zvMz6buMfY9954NnU60OjHay44+oJT9h2/y/aPPPLQp++/cPSEDdAvKVXQsWXm7z9nnXv8nrdedfrJJ51w5RWXT33g2lMO2ybx/d7YZqqT1Lq2PaMmxKQ9xYR4/vnnJk6cuP766z/91NTxu+xw7gl73jz5lISNczB0ceaROz1x31VXXHHZTTfdOHr06Csuv/zmm29MlnHVyWrR+egfvf0Scwvzfv/+qaemnnD88WuvvfaTTz5x8IH7XnrmwcidJM5coSSen3LXpAkbFmQ3vPTiixMmTNhiiy1eeOH5DdZb45TDt7v/lovQLp3PfscokDQMwAbMwBKMwR5MwioMw3bqaLiOZdCNtWTRvItPP5DOzcknHvfgg/evttpqZ/373w8//ND3X7595N4bfvXJu25I67AIWATai4B07y485oKT99llp23RjJttttnuu+/+yssvj1lphRMP2eremy5gsKm9NDscnrTuu/nCEw7ecvSoIf995eU99thj0003fe65Z+l60gFFHXTLwZpo4KID8/7/PcfU2ayfPn38scfOPfeclVdemf4D9t5/n7nnhAP/9eO3n0ZDJ35h4PDVZx+Cw9LFfzzzzNMnnXTSqquueu8995x33jkP33HpGZN2/P3XH+OXejSUmYdhNmbS3hsygvzSSy8ecfjhdDamPP7YMUdP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" alt="image.png"></p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Installing-Transformers">Installing Transformers<a class="anchor-link" href="#Installing-Transformers">&#182;</a></h2><p>Installing the Transformers library is fairly easy. Just run the following pip line on a Google Colab cell:</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">pip</span> <span class="n">install</span> <span class="n">transformers</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>After the installation is completed, we will load the pre-trained BERT Tokenizer and Sequence Classifier as well as InputExample and InputFeatures. Then, we will build our model with the Sequence Classifier and our tokenizer with BERT’s Tokenizer.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="First-step---Text-Pre-processing">First step - Text Pre-processing<a class="anchor-link" href="#First-step---Text-Pre-processing">&#182;</a></h1><h2 id="Tokenization:-break-down-each-document-into-single-word-tokens.">Tokenization: break down each document into single word tokens.<a class="anchor-link" href="#Tokenization:-break-down-each-document-into-single-word-tokens.">&#182;</a></h2><p>When to use: when the unit of analysis for task is words.</p>
<p>When not to use: when the unit of analysis is not words, but perhaps characters or sentences.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><img src="data:image/png;base64, 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CIRACIRACKwbgTgs1g19Cg6BEAiBEAiBEAiBEAiBEAiBEAiBEJhFIA6LWWQSHgIhEAIhEAIhEAIhEAIhEAIhEAIhsG4E4rBYN/QpOARCIARCIARCIARCIARCIARCIARCYBaBOCxmkUl4CIRACIRACIRACIRACIRACIRACITAuhGIw2Ld0KfgEAiBEAiBEAiBEAiBEAiBEAiBEAiBWQR2mnUj4SEQAiEQAkcfffQvjvvssssuu+2220lOcpIwCYEQCIEQCIEQCIEQCIEQWBsCcVisDeeUEgIhsPEI/PCHP9x///0PO+ywP//5zzvttNNZznKWu971rnvssccOO+yw8SoTiUMgBEIgBEIgBEIgBEJgoxGIw2KjtVjkDYEQWBMCP/3pTx/5yEe+973v3XHHHU984hP/7W9/+9nPfvbd73730Y9+9D777LMmIqSQEAiBEAiBEAiBEAiBENiuCeQdFtt186fyIRACkwSOOeaYQw455NBDDz3+8Y+/++67P/OZz9x3331PcYpTHH744a95zWt+85vfTKZKYAiEQAiEQAiEQAiEQAiEwAoSiMNiBWEmqxAIgU1CgEvC2Yq//vWvpz/96e93v/vttdde++2335577smR8eUvf/lzn/vcJqlnqhECIRACIRACIRACIRACC0wgDosFbpyIFgIhsE4Efv/733/nO9/xrorznve85zrXuUhxwhOe8NKXvrSXbvJifP/7318nuVJsCIRACIRACIRACIRACGxHBOKw2I4aO1UNgRBYIoE//OEPfBYin/rUp26/DHLa057WtZdZ/PznP19iPokWAiEQAiEQAiEQAiEQAiGwbAJxWCwbXRKGQAhsWgJHHXXUscceq3reuHm84/1znvQ+C9d///vf//SnP23amqdiIRACIRACIRACIRACIbAwBOKwWJimiCAhEAILQ2DXXXflniDOH//4R8+AlFzOXHBkCD/d6U63MJJGkBAIgRAIgRAIgRAIgRDYtATisNi0TZuKhUAILJuARz/OcIYzSP69733vl7/8ZeXzjW9848gjjzzBCU7gTZzLzjkJQyAEQiAEQiAEQiAEQiAElkggDoslgkq0EAiB7YjAKU95ykte8pIq/K1vfesd73iHsxWf/exnDz74YM+D+HHTC13oQtsRi1Q1BEIgBEIgBEIgBEIgBNaJwE7rVG6KDYEQCIHFJXCiE53IT5m+853v/MlPfrL//vt/8pOfdPH1r3995513vvrVr36Oc5xjcUWPZCEQAiEQAiEQAiEQAiGwWQjscMQRR8yqi6e4Z91KeAiEQAhsbgJHH330QQcd9PSnP52rwsEKP3G6yy677L333g94wAN22223JdbdIyRLjJloIRACIRACIRACIRACIRACAwJxWAyA5GsIhEAI/JPAMccc87GPfezQQw89/PDDvdXifOc7H4fFyU9+8qUDisNi6awSMwRCIARCIARCIARCIAQGBOKwGADJ1xAIgRAYEnDaYqedlvMAXRwWQ5T5HgIhEAIhEAIhEAIhEAJLJpCXbi4ZVSKGQAhsrwSW563YXmml3iEQAiEQAiEQAiEQAiGwMgTisFgZjsklBEIgBEIgBEIgBEIgBEIgBEIgBEJgBQnEYbGCMJNVCIRACIRACIRACIRACIRACIRACITAyhCIw2JlOCaXEAiBEAiBEAiBEAiBEAiBEAiBEAiBFSQQh8UKwkxWIRACIRACIRACIRACIRACIRACIRACK0MgDouV4ZhcQiAEQiAEQiAEQiAEQiAEQiAEQiAEVpBAHBYrCDNZhUAIhEAIhEAIhEAIhEAIhEAIhEAIrAyBOCxWhmNyCYEQCIEQCIEQCIEQCIEQCIEQCIEQWEECcVisIMxkFQIhEAIhEAIhEAIhEAIhEAIhEAIhsDIE4rBYGY7JJQRCIARCIARCIARCIARCIARCIARCYAUJxGGxgjCTVQiEQAiEQAiEQAiEQAiEQAiEQAiEwMoQiMNiZTgmlxAIgRAIgRAIgRAIgRAIgRAIgRAIgRUkEIfFCsJMViEQAiEQAiEQAiEQAiEQAiEQAiEQAitDYKc52fz2t7+dcze3QiAEQiAEJgkce+yxO+ywg1s77rjjZIQEhkAIhEAIhEAIhEAIhEAIbJHAPIfF7373uy2mT4QQCIEQCIEBAd4KPguBpzrVqQa38jUEQiAEQiAEQiAEQiAEQmCJBHY44ogjZkWtHcJZdxMeAiEQAiEwn0C5LebHyd0QCIEQCIEQCIEQCIEQCIFJAvNOWOy8886TaRIYAiEQAiEwh0A7YXHUUUfNiZZbIRACIRACIRACIRACIRACcwjMc1hkb3AOuNwKgRAIgTkEMn/OgZNbIRACIRACIRACIRACIbAUAvmVkKVQSpwQCIEQCIEQCIEQCIEQCIEQCIEQCIE1JRCHxZriTmEhEAIhEAIhEAIhEAIhEAIhEAIhEAJLIRCHxVIoJU4IhEAIhEAIhEAIhEAIhEAIhEAIhMCaEojDYk1xp7AQCIEQCIEQCIEQCIEQCIEQCIEQCIGlEJj30s2lpE+cEAiBEAiBEAiBtSGw6667rk1BKSUEQiAEQiAEQiAEVpbAkUceuYwMc8JiGdCSJARCIARCIARCIARCIARCIARCIARCYHUJxGGxunyTewiEQAiEQAiEQAiEQAiEQAiEQAiEwDIIxGGxDGhJEgIhEAIhEAIhEAIhEAIhEAIhEAIhsLoE4rBYXb7JPQRCIARCIARCIARCIARCIARCIARCYBkE8tLNedCOd7x/OHSOPe4zL153b4fjPgKOOeaYLnhNL5sMWyX5moq4CoVVY83B3rdmIVopPg14lb5FSVah9hsvy1DaeG0WiUMgBEIgBEIgBEIgBEJgbQnEYfFv3szOHXfc0fe///3vTFl/f/jDH/7pT38605nOtMsuuwj5d9QZV3L4/e9//6Mf/egkJznJGc94xjLJZsRdxeCjjjrqO9/5zg9+8IPTne50F77whVVqKcKvokCrnDXsRx999De+8Y0///nP5z3veU94whOO68uVAMi3v/1tNC5xiUv88Y9//PWvf73bbrud/OQnH0feKnmr0XWVk570pLqKgr73ve9pgrOc5SwnPvGJtzZz4slQJj5bJcaCR1ap6oeGlWsthdIJTnAClIQvuPARLwRCIARCIARCIARCIARCYF0I5JGQf2IvI+ozn/nMpz/9aU4KRtQf/vCHZzzjGXe84x0/97nP7bTTkjw7PBRf/vKX73znOz/hCU9gEq+9w0ItmO6vfe1rb3/729/3vvd94xvf+Le//W1dOtZaFqrWmuzxj3/8Pe95z5/97Gdj7FrzIx/5yB3ucIf99tvvuc997uGHHw7RLW95y/e9733bbi3L4atf/eptb3vbpz71qbwMJHnMYx6jLM6R4x//+FvFQXKpPvzhD//iF78Y12KrslqoyBroN7/5jXp97WtfIxhinHqIPfCBD+Tg20w1XSjsESYEQiAEQiAEQiAEQiAENjqBTeKwYBHVZ4nt8a/oO7T4Qn71q1898YlPfOxjH8ugZVMJ8Yv3pz71qXfeeefxPrm7LW1dVIjIkti3H0cQbTKwJZ9zd1DWrK9sP36WN7/5zUccccS1r33ta17zmkt0tbQMyTBfjC1GaFlt8aKyml+cTOaX2JJzzfz1r3+dbCnnHT7wgQ/wBVzykpe89a1vfcpTntIRmNOe9rTOYoyF3GJxrcSWlqPhL3/5i9IrxIWvW3tEQraSvO51r+N2+cQnPqEjtfzrYixYhYzl6ROOU7W725hcPnMy70sxmr7yla+o1wEHHFANpFue5jSnOcUpTqHHTjZZSz6+mF/fcXwh4yRLkXwyqwSGQAiEQAiEQAiEQAiEQAisGYElHRxYM2mWURDDg83D0vOpa5m4npVVGSoiMJMk9HHhI9xf+73sXheSewzkXve6F+OTfVvn2CtO/e2Lq+RCRDv/+c+///77O+vOJK44fSoxlTiQUASBVUTdbUXMqsWscAnloxY8Jne/+93Pec5zkl+gD2FaqgohjI/AgiDQdQUOhKyv7lY+4vQR6roStiImA9td+YhAJJ+6dst1RRDiI0N/K9yF+H0R/4jxL4HZw+62kFZKy82pE88gaNAb3vCGN7rRjXgTbnKTm1zrWtdCCS7RKvPKsMQYFFdx/K27VdakPOI0SVzIp6Vy4TNOW+H1l5ycTeX7ELPiF4rGR2DLtm4NpK27brmQqi6kajkMZOiT160SRkIfIX2EulVFtMzFaZk38SqtcHc1wW9/+1vHTyqmB6Ze/OIXc1t4jka0yq3i+1sXgzx99am7FV9BQqoFS6r297i4/3QpVpJ2q0kujp7jbi95i5aLEAiBEAiBEAiBEAiBEAiBdSewsR0WTA4HCjyFYf/2d7/7HePn7Gc/u7c22DyfNELYKuJ//vOfF59ZePrTn94rDy50oQvxL/zkJz9xZN1zHCwru/HsxnOd61yOWsjWXVvxIkhVLyYQU8vtueeeXosgwwtc4AIeCiDGpS996XOc4xz1OoMyhr/whS/I8yIXuYgz8CI4GH/Ws56VhF520Exl/oUvfelL3/rWt1RHVmc+85lFZl2ri5Ct6iKE/NjHPsYgl7lnW5ws8JoGMgi5+MUvfrKTnaysx5///OcgMBoVRzzPvNjP/8///E9nENSRVanuZLYHLj4UxJPh+c53Pu8dUAtVJpsIAB555JGf/exnK/9TnepUzD8C+yv/n/70p+c+97nFHFRBpQjm6YAvfvGLCPPsVKvJTUJ3vYADDcWRSubf//73wVQcCcvCFIdfSRzvrSCMUqSdZCVQC3rShzBaX5JPfepT/DiM5x//+MculP7LX/6StP9x3AcrcRjS1THK61Tya2vC+EtIxek2KM156EPR3/3ud2Uo4wte8ILyrNqRR3HuXvSiF60Wkb+vusEnP/lJnce1VLoB55cXbQClgtIedthh+uH1r399heKm1bQX8hxq2lHkE53oRLLCVn1dCIFOe2kj3VKvI3Z1APRkKwf5YCt/wrhwFxmdWZ6OP+hL6itcZX2UK4KckfTQilKw4lvRfBe72MV0bLd8FKeC0BksaOOst+tC6iXVwQcfTDD5k011ZK5N3SUJSkalXqF/6rdKPNvZzqbi8pTWwNTcxJa/cJEdiVJZLaWfVLTjyv9H5Gp0pZDq0EMPlfk+++xzhjOcQQQ9QXFKh0tadSdDDcZKnr8hEAIhEAIhEAIhEAIhEAILQmADOyyYJYxtxxle9apXMcAYhKwOBtWVrnSlBz3oQWzRgREiPlPnhS984Stf+UpmXsXnF7jd7W7njQNs0ac97WkyFO3JT37yDW5wg/vd734ydzj/KU95ytWvfnXm2SMe8YhLXepS0jIdL3vZyzKonve857Hu9thjj7e97W3CRWC/OZfBmnrmM5+pjeUggkcz3v3udzMFmVUkvMxlLvPIRz6yrFDm0/Of//wDDzyQtOxAtpO0yrrKVa7ipQwDS2xOpyG2zD/0oQ89+tGPLquSMGpx+9vfnvwMxRe96EUcCnXgQmXvc5/7XO9613OLue6NG6xBBq13OqhFJb/GNa7xsIc9zGs7if2sZz2LnKr83ve+F6KKQEJlkVAdGZmub3azm8mHJMxFDKF70pOepJqq1uxJd8nwmte8BjrNUTawDFm8D33oQ9VdBKy8D8IjLYpm8TJoy/MCGtQiEPL1r3+9ckXQjj6EL5fEAFE5KbxUou6+5CUvkaH6emrmpS99qQxvdatbaaAHP/jBbFd8mNPyVwv2tpcs3PWud+WuEqJFPCvEm1MtIoIHf9y96U1vqvRBofVV0QzjBzzgAXJ+znOewz0klUACeL2IwP/93//V3C0yCTUHH4f6vuENb/j617/uK5fB//zP/6g1G54HSve77nWvy5/1uMc9jh0uNx/Zsr1vc5vbeN+Kh5jAR4+n4/KXv/z73/9+LgB4fbTXox71KGLgL3+9jhmvOtXxrnOd69zjHvdwl0eAeFwbslJrdTe4WP7GiKdp0CAwf4ru/dGPfpSohUsre+Ljqle9Khq8ZmTmPZSbHiWtrLi63AJEt0Sb+2nfffflyHjFK17h1aReKfKOd7xDl+Pp4EqoQvk1NJxRpvNwonlYxuDl8pOPbsMBV3ka/jwR/WAnFb+PSYDXQyYGFxl23313niM8n/70pytFJrJFz9g0YIkK0WQ7JjAEQiAEQiAEQiAEQiAEQmC9CEzbWuslzdaWy3Hwspe9jNnD1rLNy+TjjGAj2YrnbmD2NDu5cmbPM5AYJ0xN279sQmazj61yhyPYlqw4ls+d7nQnPgXGjFQyaVK5lgMjk3V3hStcgU0rhMHP+uUfKReGDX+BPpWK7cR0fNOb3sReYoEzJtlXDmgcdNBBzDZ2OBP61a9+tR1yhqg9bbY6I7NsyCp9UIUmzOCioimF44Axyci8//3vz4xn2lU+g/gDIb/5zW+qyF577cU2ZjGixHSvNz5IqBaMZLbi1a52NVYli1QE51BE4O5hCbNstYUqMIBxs/Huw4jlhlBQXwV3uUtYnmKyn0koW7l98IMfZFie5zznKQeBJJwjvj784Q93XoY/6F3vepdUDF1f3eJdYqV7vykfBxubNcv8ZpEOqskK1TRcIfqJswZetKmCfA3CWxtVBfkReGfucpe7sJC5WrhUfNj8OgYyPA68FTe/+c01Ihpa0BMN2u5yl7sc18Og0PaVUe1oAxR6ml6nRMdVPv7xj3O4+KUS0jYzmzysa13i5S9/OaOa68eJgDooxB9xyCGHuPYYC+BicrXo5A74qI7eqF58N2x+tLkMlA6yNnr729/O0ebD2YEwB8db3/pWI4UwvFeKfshDHuJgBWcWODqhAzX6THUMeZKH58JZBu3FPWSY8GJwcsmZH8phEBJqcTR0Ff2ZGwhYEpYA3EBOyuiQamp88XHIQXGaTG93nKQKKlYEFkI8kY1NrQ++cg1nfiJdQovr1VwbnDKAawslGln6WKM9uCCYExmk1T+RIbx+YnToyTe+8Y31ZINRlzM2NQrh+S77jjrILV9DIARCIARCIARCIARCIATWnsCTUZtlAABAAElEQVRGdViwdhhyTGuH6h0icJSAscEcYgqyc3guGCEM2maBiM/SY7HwEfAseH+B4+jii/N///d/9m9t0rJOmUlMfWc0GEIMuUF7yIHJZIt47733Zg6xA4UQQ0JmFXNXcez2PlUJwDqyV2yf2VdJ7D/bAXZUgZvgne98p8P/7Cib527xg7j7lre8pc9k6deyYt294AUv4Kdgp7E5HenfYnJS4WMLna0IC0ROLjDIWdplUVctGKssf24aiJiXfm6DQShzPNm6rsXngLCBrwkYk0xlXiF8egFkpdXU9Ba3uIUde5aqu2DyF7Bvpa09fBE4GpwxkaEILF55+gUQTwFIoskIxvTlWvKVn4Xxj7BUfVmuFccNhCoLn6HOHiYtp1LVqEWW0IkA/gJGOBSsbpGVaA+f60qhqsM34bUg5RPhEXO+wHkBvoxZDgt5MpIVp5X5uTQHUWUlIZF8VVATgDwEICfHDYcFp4ly0RCuplxyeoVuKb6mwZkfhDeB5S/EszNC2N4evqg8q3ZOf4jDDtdexoUXyur/4rPYmfHK0qD8IEIcQNCsyBs1cihhnDvgInFXuXrFs5/9bH2V2HwHvBVXvvKV6wCOyMaR/sZ9w3PHNaCaAuVjYN7tbnczZLSvEw3CjTJ+FtccInLuP/oJVlq8DjtIxYFYA9YhEUdCRHaIw4kYORuAJHcCpWra59Ou3SKVYzKOcvCOIcDl4SEa3YY308AXE2eI+KecXiEY4C15LkJgeyBgRuJMNEcZxZyzNYFMVpxn2cA3UoxNqxXfsbllMqZAQ8lY45w12E2q7SjZrPirEW5ZN4EQ2PzG0WwSm1WKycGMpHZmV2ey1G7s+6608uSdl6eZ34IOgonU5DnIWYY8to4QDsJ9NfOYvfl2x7dWKcSCbjlzrMw0SPOx0MwqyArLr63hJCGk/jBrdRNBhojRglTftsEVr3hFythkzrQFqx7CupAlQE9D2OQ8iIwtLcJs34dbNWhWhNGR+vDVviaqCpKHtPQBS9hkiVYZOyWWbM1tXOgM1pRx1VpaK6yYRhxoDvfNaQvQ9DQffYkMXP+z8LbMV+mCJPqPKcJfWo1lmuTaZVCcEUGLc9hW9W3ViFa6XB9Nt6H60s/7hducY36gctei3OLTwCk2AwXSXfEpnPWAcIu82heUK4/Q+mtQUHJmFUfX8oN0Ws3Yt4eKA/VszKqSi0Pfo0aqo2lHN6Mwz8qZzmYv0wlcCqHhQD9EYFbk1QhXruYwpbMpDAf10sSG85yyJKFtGkR6DvlNqra4PKU7SKKhjSA9R1en/smW2j8JzbJi+DCyTDvmc9MOtdz8MMhwDb6aKumNJCcAMWaViIDdNZOqmIa8VtZwpXUPkhgRwBpBcOkPzB8560KDaNv51zVdA1aQtdbVoRm9Hum3klliDX66l71oc6KC+gmxyjXNVUexIWzqN++wA//rv/6LDSYHXUTfksrHxdj0rUxMVWU3ilOlMD4pQ0xT5Y5XNbkpi8OCcmOwiWC4mp2tzaY2Jrrlme3H8nRXZBMxeZyzcF0lbtVfYpdgUs2pxSBPZSFDDAsGMYAyWuBl2FdMETwuQTAaqmpWBMsSn4tS1Mi8/J73vIeFb2XVEGWTW2JpSKrZF0dCOhOGbvFcqD7NQH1NVYMqm76dsCAPSRAzM5qkRKMfWO+5Zvgp5Cx/zUdbEkHRfVlNeEJW5nUxKEg0ITQzXcKFnmChLRcJ9UISq4gjCWrtmtZl/aYHW3e15qx+UnlCxJnl9AeB6wCI2dZMZ9qyPA/SKlr+FVh/S07X8IJZd2lFHmoQqHTLgCqTBHniVaoqWlOywOlD1S0dlBABTLjA1Ccl8au9TmRoPvJ4PkVCjSIT5aqy/uBaoWgo3SELeoZp11gTAfDq81KVq4VPwZpEHgWJ4K5xocMoVBz5lGDwjpci8QVaqAxJTVzDRBVI68NbBDg51UhMOQDrpIyTJq3KMh983FJrMqiU0vU0K4GuomV1pOrGwq39FFP5y3yQQ76GwIYjYHTQe3haa2gwjM2iJo1BRUzdfLg84+wQE5q7jo/NMczM1VyWls7yaZrTHDPkCrT89TkbnhY1UwEF1FzhEJPhxk1szumjreq1GcMszYHLnCaAgU/9NdHNcliovsmNl9/cZUIQjTnNp2lWHMgpW8fErG6SwGvKKhv13ve+t2q2yG7RZe1hmGdMZS28LkyJjrmVL3hwa2W/agu6sp82J7BFFgdCmsknjWQVt4KrHYsIQJKYKi2pvN7O8Q0sSWabtYOtVcRwEEHnaT70viLWPgcA61xhzfN0IZMtXzbjpMUkADvE2T2iWkFauAtLM+f1HCuxj7yN1+ruLKfDiRYLncdo4nannmm1yZxZWZZjDizLFrFtpSDGSz4gpuIWawcGyylm9JW9N9kWClI097qDpVpNWqXTIeG1BTUpxioFahRVszWlI1nHa9GkFlr9NWJfqC5hx0hPMz8QmIvQfGIPbBBNPrYZaEF9ExsveppBQTNseaq4U58OnPYx3fXVR2ewcUhLafFX6YIH0w6NhqD2tI2uWV2Ry4bAdj2NC/LQUky/JodSQgYSmniBNaPWcCud03OstKBBTORFM0HxF9SsblahsRtB9pzGXqFB8hX5SvdzNtx6YXgaFPJUrhnSwDS9TxahBR3ddYJVZ1YFH0o7J4tW04KVxKiB19Fpq4ZrgaYdBXk7vtoNBpE+BoJtszbtmKv5B+2cjefqSZG2PVB/IICPFdYqQAACz3JYMEgNeYsLAtVw4hP1gQ98IEOpF0a2QOk5Fk2jzAjSeaimDrBr4rHC3Kfdrq43qsNCI2lFH4uc3mM46T28AGbY4ya0/2fBE1kPEG6Z5M40+Ot4OXuG3cjuZT+3ITS/+Tnz2D+VW2VLZRGo3MmEYhrYpu8WQXJdXLj4bFcyW4TEqVlAINeAZawiTOa5jYHjnIUoUUUI6RoK48rfPqYlk5Vbo84tU0lFEIfOapI171jbHLZnP5d5ycxutW4yS2UoUmLMfZRgUw8C6i5nt1o0F3RcMc3mJRIBXMjQqiDQXYtByeMv56WvtU70mSzxWs5qp9atgmgI9CmBTT2eQeBiN/VYt2r+VegW8zdBm1Kt0NKy4ekrktMaQRvDmcxNb1E1KBQqgrXKBZOg1FC5megBHKxbGhSxVh29rjJXKPXdOQXagIWB4WEVocgaAgaCASWaKuuTmlj1fZUJAQDnOOB2sWLpzzwLdbcioOdj2iWP5G5JQoAl1lEm4PfGj+pUf1C6ElXZuCBD1Uj+Koh/LfaSjz/i0JakAke9ZEI28lC1lVXCK4LM/po9ZFWSj7NKSAhsFAK8Fd4fZDY2gswVvBXUIxb4QH5LD22SFl4TnXExZygZ9UxZGhUt2eYqc8uRMbOHceQclgmqZc5c8bick1YyVLq/Nbe3CGtwYSxTCTjBawIhgKrVeB+XTjv09hwvaRKNw9oeIFeLnUwzhuOE/QaXaZYThJfHRFe7ahRoW2cKMhc5nWd2qvzNUVy3PiZt80+J4ZZJjD7qrs9YkhUPURxVh62lOG0xnwP7nOGtP/A7sK/USL0oVw5amsYt63IoCcG0LcSqt0CwVZwxUSkxPSIq5L//+7/N/K0uFmuucDy5m2VrobH5LK31C2HQ+jXU/Gyd1Wd0swZNVjIkT8tzVS8IQDbe/CpR98BtVucxiLwuylhQOxundAMQnDRUKadHezlBK/9gKU6+zsm2eppnPEV2TFVu3D3a0SLONtMcfc6rd01IHZ6b0vC33Kugbq9pqM2D5gCNzcnhZfjQImoSML0Q2KHd1nOIStnTJUSgMxsdBdbfWtz7uugM9EMqh+Laei2C0U0e+QwUnj7tCl4bEQxOzgVtYRxVw03mr9W0kZ0tgtlNofjxb5oMzcbi21jtuzRintLlTOSzo3qpvia2ccLp4/VkvTULjl13YxMNarbpFzcD0MdzyuYce659zpOybWOgVjAP2B/SEGTgr9E6mptb1sxpyPfzZJXFCrBk0Jn1AQqwOmpHrgojpZfWaqWfmHz0HDNPacjqCw6PXl81s5nJ1ti0YNW0Q9s3k1CD9T1PN0u7jdVcSnJ+CgOcMglFrW4G8mRC/cHKwler5/C/qJ1+y+oBzZTI3daggaleSOpd3Bl2CmVozmSrcmnhpj/00CaL204C/61qbKwKaz9rCX+bzmpCNyQMJHOEoaU/TSoERj4zzNF658mtMQYJr54+YaPAo/u2EZZCYLLfTAb2ufUqXR+ux/sqeZ+D2VzV+pA+yTZeV7bGEhp9ViQsY7UCB3cFutsvPIMIZhAzjt0GWhq3hanE2Uh6xiCa0lXZAmD+dcvglNBpDuFcSIPIipsUqVZ6kfv4g6991ZZ4Pas4sll4eL4tXUSln5lozLxcpxze8zMnlSMzeiYl2Gpkp8jfmpoVV60/Pwd3CYBDVdYFwiY7CiIdQocnjBkNc+tHn9WgQdst+dB4PNtiWqRd2fGwpSatUeDCQCjmRlCV2BKWJLVmi0P+PoLlxMdS3TwjlU+ffP61DJsGI2afOVAg+PQ56MOGyRZLaalkoudYZvQ6npE2RQAlTj151Oef6xDYiAQoPRwKJLcLameYO9KsNa6IWcjmGBNLBHo278M4ToUYKdZK5hat2i6ohdLQo7zSukwgjvjaCGppKWeUdQ5Nkz+jgv69xFmu5bDtF9yUfrvarpdtWwqxp8zmyOAQBLUSNDolz460dANmoRmVsdF0SlKZKMzkIqigVUCIClI2WHS0CGuEw3QlvPlE0c50eBaGwdlqxE2PuRx4kVrg6l2Yip2C4SOwBpXjoE16g0JVn97v8Lbl2JOD1aBsDNY4TRoQVbPcVCoTtSnUuQOBjFiB5mHub2+VslFhgXMWoGKaw60vyLBOsfX2K+GMECJpFGYJvwA9oSLXX/OzEC+u0pFqCTDDC+zjrOo1VrZ2qZGWeDaDTt5WkEG5xON80fTIeBuX86fV4RHjJ1JNtW5JLG3UTmPNuMOZUdpujS8YRZZjFffE63777ScC5xGAtAjEjOtxktUI0ZT6Nm+UbuxhzH4sDIqj+Okk6lsP1dIEHDRwWAYHtWajtvhg+hhH3nfOVq+BqaY0B+EtmguNbjfRs95UL9DqlvgUfsYznafH2ydc2WsqFp8sk1LHMEnSlAZytuJMNeprKBka9CtWidkVQAY5B649qt6iNi4Y2+ZJp2bMPAjQvgw9Njmb1vyg/1fOimbiUj55i/g+mDDCzS1mYy4tr/2iyK32ADHAdQNt5Ei7t/WrGhlY4KZ3/Z/MOrbpsaGg/zssAJeRrg+roP7f7vYXCOghZgZ/zZlu4SBbK0tNO809Z9qBxZkdbmVTk5hmM3afyOZqfHq8fREre21upH7r4aS19WWMzMofMcOW2Ly9+nARsImr50vFP2WGcVdyeilfhuqA4GRfzbSaWEyTJxQ6YTGfVdb2E/7vTrax6myE6xA0LdsdOpAeXy3KGJ609s0yphK73NwBejw1ws6qKcYRPhOKjuXgTZuJ2sVqMzHGzDUqQmYD3hKo15LKgJ8jg17urrm7VvSlCKnucpbKx/CwZC497Rbzl7MJq54KMWVbvbQFVcYEZ2D3yZWusmZqwpv4TH9c9QLtB8qkjznrWrtbObCCiJuz1jyB5XeflWrZ4WQjqocSHZGwdeBVI0rEX+ehoi1FZqLqbxZX+pl117lQChllWovMkUq5k3fV1BkNiguNmWNbPuZBXRrzpTSobMnMz+JEEu+JadRyaJ+QesQTrF287FPtZMUtwiypjRSFmk9VWd1VwRpjJZaD8BJStjKxaWAjVxLK8aTwLfKcu4NbJFGKEhWhuVlirlXBV7tbvhr+gySTX+VjL4JsNFHvVSWnEJn4a6kjPG2svrZh6JaslO6jRB9fxfHV360afZMiJTAEVomArstYdb7anvasIuxT0YDdNRGZtKu3T0Y28HkrTLAmQO4JcaxZzirSUxlsLCiKl1FTaQ0N+lapXCalyQxXO5AwTB0fBRF+TtUMavKb29lUqsaVIIntLHa+rS06JYYmnBJYtgj4NPkxNJOYgcExkbZwUyiV2grYrA63TKfKsk1q1TP3tsird6EtqNc+iuB8wWEWilIJLNY8XEzBEolXVy0oSCZ202a1qVsmQH4Nnya5hR4HNEzI1uUWDi9/kMVCfdmoFa5nMnWo+/KkDLTILohHZtBYKc3x3UdYg2utzLZUEOE5ceaUaD2iGGh3vaWSIGABtTpz3HB2uG7J1csS4yMEolkN4a62kC1twRJvW75ykD/CdinsqyM5y/xrxW37hUVc02sgHZ7/jtI1K08n/4HiZOEl5LURTdsxvSS3I2hu8dKoPi0UOgwV0d8+fHDNIJdQK/TWOOZ0FQkVJJ9BktX4ak4oDxEgpRrNKoWOpN2B4qsqY4TKYQY2eZphtCnnS6U15VI59H9tqmUNKOHGHWhIMtS1O1O8Iutg1HUQzEtl0gs3KUnLW6GBDLoeUaVa2b/aghdGXfS9qpr8nbOg2TK46JM6bVsC9G0zp7M5JhDumP4xn7FUcMm5D2dKqLtuY+qWbbsFPhPDp4XgZr7iPOXj0Alb+KpeUDirk8NOgDkD2TA3KLSUgdwGrFXJzOnADgVbN1Ap0pru+HS0r4mxueH4eky/fDEiK6thX9XaLX7m/zQ5Fl/QsYQ0AC5tHUgzW+Q0v07AHSVQT/Lpk5jd2Bi8s9znZgT9zEykJ1G8jHa3jI2aAV34OkjeZ7WC1/QkRpQVzhaWvqtQUx4n7qzSSUi82scwdy9lyja5Wz8oDc5oqbWcWWiWPSvBSlVEthgaXS7MX7xCJhHe0H66qbIIzLqm3pnKGduaQBwrgSobk+4Sb36lFOFQoj1DMz43h68mSk1vVWDBzuK2LTUlodkQQ25OqjluOh7VwWRUTTYnc+L5mKSktWiBIwlQZh/hsxIqQo1m3dWUBNBzZKu+YvLWWyFwq8+shC0cN6OAC1zVNJyWslJaOSiser5o8oG38iSwprF+GFzmUMuJlVVCeoPFEnwRaKX0M9dO8c2vmvx95N+E2eIFUCZ9Lc6Rp5XFV2ud30aEJW2JWclElwNNU6q+GqmCD/+RnSteba1DfsoBKwvPcnpKVe8HUffCYm7h8xZHN15i0VusYCKEwGoQMJyXMskbj3PmIoIZLIYJlcsYbPtdpgsTuLSmQdPRpPxLKX0y4UoFEmB+1cwAVkMVtHNgcqtyzWCmRBO+CccMM0cYhMVRCkOibQJXfHNU760QyD5htFDiWe+rbWCMZZ7fFqTVoKpMSFNfJbeycFUAaPo1eY7zbCEw4oCGpbn5Ndw1QzJ19BmzZU/SJEwHkK1CWyb9RRVtfdHB+vC1vFap+Z0HK6sk/ZOlYe0o2RCw1petMkva+dlixUD11/hq7nhaHFNNKUrsSc4qYhvDSci5RpdWHabUrGaqUigkBNZ5qNNcNhVIcv3czMBnMSmMDqkP0BxmzR5SybMfKaRiG1uRycNSncx29QK32BU1Gf3B7KGxmhjU+3LkQdQCdW91pzih1ExZtfNVcvnYDWqRJWfEwqVTtbHpq+5HJCgG80xLuIIX1f24rlqHlLnxTh61aJ2/SjRp6Dn+coi3Q2dLF0b3pm4p0XLTt/5kDnR+Mw8CdfBkMs4qBW6xP2g464LW7Aesdjde1MuK07i5MFh4dpq3gsw6iaFhCtVDomq2RtyoJywMbwuebsrU9zQBvwMbxhaxeVZvsI/hqFLvjRPfGOAUNJZsJusKjE9zn6fIXHPpMZ5dmC/MiTbPec2ZN1L5FKy6bl/7wEZzHFipJiO4VS8DI4PDP/VsMJOMAG0WGySkWJi2bK0z8r3Lh5C69SCOr61QF2ZMfn3b8h6fkUp8xictTVbuVtoWv8+qD+yvW5w+0IiyhJhinHrFn9tY61jyW+RWEI0NWB4Kh4o1GQuQrcuvTB4KCmcHz7HIfeYtrUAztVHNl++wg9+glZyRzIb0zJsJdM7Argz97XMbfK1bgwhWTV1FTNys3yYafcxLuai5JmseUAqKckXw6dO2axqb813qyNNkv4tbusUclKjdLQmWAT2Zqle7Usdl/O+ctabj1nbMeN/UXf/3wLaFHxl9vtbFPkkrQqA4qmNyJDnvCTVUD6yBw/AgJLY2CqqbOeJr4eSh4LmwW0ITtXVgbXDil2ufz8vTVZzusnWmGhwKljm3ih4I4KvxpUZayqM0zjdV9xPeKLXrXmCBFgbzvt0Jx2g9SaSCxAbTHhTsPi3+4EJan5Y/yXUbdSlPjS5q5QDB0CA2tzc4tCunTkwCphS91GDRSx2/8v4wR3PJbGJx6lVPc9Rz0iU3kCFfQ2CjE9DbjRTqV68UmtNMhmZ42pgIG7SO5hazn4FvSmm6uCnF4mWycou6OVk1VXbXKkBVEME8bO2bjNkCTbDmZ0vJAj59ZlEwe6u1ydDxdbO6BcIE68w5OFac3g3RauTCDKkDmCFxoD6ZEq2GLYIJE5ZS0izQjrbhzMAQGT12fp3+6ONb+yxn1ADZah0iOTxr+p1vM7cc1vKC7eFjWeGrUtMqmvKjidGjmegkwG6tSLoc1UI+mDc9kEmjFLm5SwM09LY2262Kr9HtWltqr3zlK6uLRdDCZxW218Kv1wytylNNa0eHhCJXoDjkJ7C7PmaPJoBF2fLt58nRg4haTvHwoNkWR5DI1C2prNfUyJbhglyYEknFj6BvN5HMnJpMr6bctkBVNhBAprbxcbTW1OdF1uis/RaZ4mR6AZaeTGnRBG4Zm3QweA0iubXIa3ZBeMfrPKtihPYnCAig+hzcWtzoFoeoBrJJrz8+MJZTr9BP9DpzjvmEikslm1U1PQFYG716JmhOxzv8O85zfUOQUWW7XyY0dUHDyPVMABOPmm1PdzCOBtIyA20Kml6g0wcGd7fbrxvbYeGJpic84QkMfv2AnmFl9ZAt28k4YVF4Jw1zvYwWf0Vg4dtKFYFZYgowkPxlhlkRRTDdsJZF8PCVIWHfVZcSoYwia1J97fuKEJ+KUOGuJfGpr+66noygROIxhMxQDHgvT3ZhPaAukFASJZbwfYlmCjOC6c/U1of310qshP7K02LANWPi8Iyc5HbIec3pJW5JVQIrqxdyUNl/1Oe4WjR5RK6qVbnC6SUOwXJYmH/rtEUvUl0rnSLoBek8JsatQ8Xysc55MxNViS+JRerdMwRTHBlaDqIdJ8I/SAqnxNB7TG0iE0MIfYtpbQEQoaXqLyTvBXbdvkrSrluSiu+Wj2WbO0kbeV5OTNMok5sKRQnjBlLfWsUlkVz8JqqvyEjCd6aaNAA+CHMrDq2g/kJCPVBu/BG0FmcoCkXlLKaEsnJiUN318BJbEku4BzsdOtC4zjYLl5AkLXPXFVkO4usSHAceJBZNiIHAl+dsXq2jZAbTLAmva1opN42O6mEW44JC5lUXTHoTsY6qCHEsWh7PlkpWAwIVQSrlcm1wFyrFQttTck2SvsWlahFceIwWEP6F+rkWzIVwmojWV9PX+rT6/ivgH0JaNpynMC1Y54xxFZczX6cnTo19X9W09hjVohJSj7j5LKX1lYUmAghjZ1wrKBchsJkIULN0eBYUjbzVy1AtY8xi5G4L31gXhrzRTWbKZS+5GV5luWsnF1mzgUf0zY1MdHo5pcKvpfQmWZ9VXUNEvTaZUFEGVvo48tqHmC3p1haFAw44wBrHoUAzoWoT2+G7/o2bvWzuel8DpYLRhZiJ1NP+A93atM9P4U0QiFnxfbX0m0Jp4YobmBmmaHnKTSn462MiS0sSL0DlQe5LX/dr6xFD3arajwsLCnR4uqsig361FJn1LiNO3fnN24LYvtbdpeSzLXGUwiBUKC3Lo7vGuGuLo6enqQH0txr7VURxEKHn4CsO/hpBun0/OqytjEyIdBX56AyytQnkwRN7OXPEtp1e+2Gi9QLMSbKWtyiEFDa+GHoRRYi+p2psb1qfjq0z+KvWRNJJ3NU3nPZ33tPPymhrmyW2qSRhzULaJJeE3kVFoeBRsTgEJZfQSLEBQwvytUVeswvmtPe1qxrNkxull4HwWsrUSh3VsvoSqfQE0Ty8T7mdFNJky+Cyn+QuON58odaFaxBf/7HnZFrg1jH6PKBh2uHgGERb969USjOn0yKU5Nve9rZmftOFhmMBedaJw2KOhADCy+9jc5ExNctxMyeHzXprAzssjAGGq6nBLMaFSQ8wmC2BBoYVjolFxzJHtJZzLbC2he1LG0gMJ6lYgHZXytAyTiSnxHD3mk+NBLOtVdbs4ICT5dwsY3BWtlJxfNBaWIll4firI9r5N0HzjSlaBFO2CAawr/4S0vOxZDOhE5vpJQ6PieEnlbK4LQ11yU3KlapVQf4E8EZcL+AlfF+7iiOCcC+DcUtMyV0QSQgmhoGZ0VeF8koaOeKbH+s9xgJ9lY8kbEsaRllx5gIvwbJc0RhaBAYqGhA1GgaViYbZyfQ1OAeStyrI3DkxxnY5y/E3hWlELgCtSWaFctkwaHlAFFryENt6ViTZisp1wMRUZceeSNYJA7tWWfsAg6KViLaHIECGV56mOYuEd6fZBNCylCeLQS2fIvuolFVZ/mqkOHk6AkM8+wxoEFgjKldCuoX+g6SpuXQsDWdeJowuVPKrgnqpjr5kFhZBoQ1IfyFPTh9weJqtfz42H+SjjcpCJhsUuiWGpjNZkcRHz3HCxaSvXQB87GMfq2hjoVLJ1hkiPg59Q3Ei8+t5MtOOH9WB2PiXS0VMEQDEk21PDOuoCGoqxC0CWEV4cECwDwaIXqoR3VXBKk5u3BkgK67awl/cZGh5kwPvklveVyet6hjI9lt4YSQsYuIbqsaRhhBToJjeu66T6MPEUJY4nu3SagqSp8D2UQs9UJtqd5+666+YvDlQeKbD2Vo9FjpVUwTJ1csOIanIo3SZKJ1+5lFk/GWuRDUllax0pGLVCs1FCGxKAha4GgvGYF/BGlwU8Y07EIxoSqS/6tJXzcA3ORjmFug+vK6FmxKt6ZRRU7rNAMsQT/Qgkz6haZYubsXnMzUL9bcW5NqiwA5ka3khnIkdAVOi6c4iOOt4BQ4WIFoBu8U6iIYFxUonq1Ypcyl9w9pEU7eUMIBla761vpt4WzQXYiqI9mX9sjRbUMBnmTjcx33PVe29j4rrk6zvNfEMDSL140Ityrqou8uQkG4g28rH35aDbH2tuy1wlS4Mak4K48IqSQnhkvNX49pVst9A27F/04omEsWMbD0Hi2kJjIO7LbJ8dDNHBphhOoAkdq0sqUYQDYpSof+0yIMLGixVXyeh702asoP4a/yVSkBx5XlhatJS1M6JWnsqtBdKDmi9zEaEXUNqPE3J0KCq8XSYIkwOuA0gUHIo5PbbKTxmEqgNIsoSNYyissbVVJza2TdSNVrWbW5zm9KOSgxzghnVrKjdbR8a5jRSMpPcfiQIjBeGxlhmcOSDISXWZIKJuWLSR6kIlledx7FxSxjzlSlloSaHqqA2qoZTF/WqZdTMZrGoWWLMQQhcttNsw9OZmSFV08mY22HgIq6dS2wGHdeyakj4uDaM/dUnzIbWyLoeZGUK1teZPXYDRDBIfAT6VExTgyXTdQXqKzU7+GqwGVEuTBYiSM44Z/DIQYivlYP82X4tmghyMGdVBH/pOgQWmaj8lKZpSWzRGNgCDXVHISQ3handpC7o0L4SydYKraLrrzWgVIEmldxIzupu8YUYSCUkNYsBKW2L79qMaVqpCDKEtI8gHxOEPZmK4JY6csnzQYhsGlXHWTa5tIixDH1ct1aj/5n+hMiTm8CypO4+MhcIRU9SCPhse7Wo0qWSbY9aePsIl7m/6lgx5W82rK/qQo+sushZKlnhX0YpGQRaaO01uXDLpwTTkUSWUHjLQSmmJHGq0V2IY/51ckcTE1h4E2x8oV4WMy0iT6VQ/jScC5+KLNz6B3IdDlScWwK5QkQoYfR/161B3VVHikLV0V+Tu35u3nTrH/U57pEW+eDcSrEW0gxk4q7AKsWFJK65DDCUlRAyVM6VlsyDHljhkJrBJRfZX8T8LRpan3JczVFF6JY8X1WWGdxhFt3eppyKi0AAEzqlSqXGC5VUEBmGLf8SwFcfA6eNnaIntypUv61UhU7FSUWLEsFHWtkavMLbiK6c8zcENisBfd60MDA8VJZZJdDEYsraoHVXL0qh4WzZ7atg+LOyhE/6IADx4kzLASvLLMSito5TxLlc+0zatemOocX5a0ExX7XwxbkgIR+uvRw+BUaXh9VVnPnkh2z5vtkP9TLmgcB0blW+6lWvyjBzQN1pC4/L2QQ2S7eYzAnn+GwjW5LsN9JDLIWIOcRhRqX24F+R0aZR8Cb387m9HB2MkcxU5qAvxallvr4X5Cw9pzfIVcoOs5XCXf1kGRIibwHVIrL1t1ZkGdZXd5eX7VZJYmgzOxWqvWwU6RKSsz+1L/+Cw7l277RL5ammPHHW4p4Dye3Z+FuUWukWU7+oohYthBpGaXS+mEPEXp1toXarv5C/u3b1nAOdtHj7yOtyrRZA+eu3dQwHnZw1ocfihifNp5eKgu14uKb0YK+dP7eoWxRaR4rAofL1kTnsTC8sXr9GT+ujtBibfIsGrLHpkIWQPv6qXpvHVNBRWRq1fa/BhKb/E0m787wQ1WO85VIxk2hir36jv6E0FpjO72dlsDLS7ZVi4trx+bFHRs52W2VOEpBt7tpPdebXeZOFWol4/UyJzvOaJWyEs3eQwc0IsqNpWNGuxy3FjPIsNp8Xq9A2HofFmNU41fYTsoEdFhrJlEq3qNYyVAYXk61oLPlM3hI4uNsyr1sDI7wvvWUohz5an0PFkaqMNEuRJZ+RT0uQig/FjM+NamzrygZkq1HLXN9lvJm/bBSbAccRxGz5t1QuxBxEbkJOxu9rMT8Ckbg5zUQOrXjKjkHOch7XuhdGhi1Ck6pdTEorsCWprHqp+rR9Qf31ILkkLVVf2ZakjyCwRW4RXEjYvjaeQqp9aWAieDqJOuuRJYH2JWwfDSRpOdRFD0eIr33OFUe2PnXdBOuzLQEqQkvS59Pn0Eera4X6yFk+raBBtJ5Pk6ElHwvgVp/E116eXviWSUWA0RJF8eV1tobRV6zo1GuPtJDN+mc9mJO8cuv/9pHHkvdSSdVH9hWWyar1+ec6BDYTAVo1RZBJTwNr9TJwrFaGw4Z2WFi87EOoFHOoVc0FRwyzkxnG3OrD27WETA6H1FSfBe7jYAIXxuS+GXPFKi9Dfv+x/t3yXMcLsxxrkN+B+UGT5okmjGszra1Uu6O0kQocCGlytqIxXzn0qTEWO64ZXow6ZKF78DIIZI1wPZRLnZ7Dc81qpcZwdvSv5UN1ANxXGoWzcg69mvwHpa/vV+NCD6H8DMZFOSzcLQhbKyTmDF3jSz4WuOawUIqv8lTo1ua5tfFZ3eTXuKysZpFyEzhu4wSBxxYYz73DogncCtL0Jf/AYSFPFWzR6sImgWFoiXegY3CrfXXLRjqpbOeMc2jR1veCKkIzt1/FllZ9mzpajdWNxtjJIsSjAfaNHNHSsvR5e1qeiVY7o6lVxMTLhneIiRuRWV6+DKPGVOPJVo+clHuxxV/VC72dOc3qNo/RxMa+Et21+qclw8ht050pwgaVhyPK2DHSx3KqOO+Vj+lXfU0d5tWWwyC+6dfHXb2R78b7jPlBFsphYYPNMz7qwrvNs1MDWd+gYZoSrQg8PjTbvl68FXbmHIWGwhlwCZc3h/R5brLr/4fXJqvbglfHJGVG83CaU2GmHj21zCf7MA6ic0WLMKiCic+caO03UI15XwcR1v4rMaxedlE41CkitmLsmQzMvLWXakFK1ILmaKa1mZRy5qTruE0XRNQmhgalryzO1K+TWwLN3dYwxyZ9KD1GikAeaJr04iNtbHMRAhuOAM3YlO7hL1p4E94GrGmfvkVr3Pa5glZH77SCGNqMn15fbyWuxoW5ruRXHZu3tdtvwqGXUzcdCtiivsgUt4lKsbZ7xjEx6bBwHthZDPOVE20DDXVQKT4gYqBBu7XDRrZBhFX6yqziVVcoG4NOUqWUJ8IJUAaV1p90WDR5WF/MTl4b9pV2LG5maWRo4eyrOnMnPuaIUdw5ndkkvcOi5dZfFDFZ+fThdW3yV6LOo9X0Qz1n4PIYJ1mpEJqYNjUo8GHVq5ecmak2yUnl7vLGBXSGALe4nPWEysRXvchXFru74yqofnFQNGI4bLHrjjNpIYTX+r6qYOuxxqYBQjfQz5XVIpfAZMOBnE1gHErgLfoXdDyZk3yW3ijcfpje4owqg7YVPb6QibGsy+ktJKcnb7H0cSbbEqIu/JI+MiEDXxu9hZOF62ecLdmMGh+37ETakK/B0p+w0LdVXLs7cNrCeYtMJs4XeA7LxznQceY4yBM6HMwkk91mnGpOiIo46+RNw6hytVDJdIZB/JrA1Usn6UeiHkUAtroKaqNBqsFXE68zsDq8yVDHlucgQvvqBJCZxHkW3q7JziM5ZzQULkjLL7Yt46KVu5QLi4hp03RqUtUrKoluYCZ0QMZ5Ik9atcHlLjmdK3HiRlt7et2rf7bYZNYLblw8tYh6zQGlK1qhiGRcb3HJNooJo/PI1gzQhF9KrVc7ThwWq014Zv6GkEXOU/3O//O3mXd0OH5WE5O/7voMEguxHhgD+uj47iDy2nw1EkjrFQ+EN3fws0xOHGsjzEKVooEMdX5fTIx8h13NFFucrNe3CsQjrWPA5jXK94JISwxjxFvu7LFQg0zT9GMh1ALDYUGEXN+GS+khsDwC5qiytfydVE2oTTbH7KyyoGg8dEQF0ZPspVOSjEHK6GTRLbd2MRnNPGmLzD4k9ZQCV78HVCJNxl96oEwqH2vTpAxmD8oxnczi6wl53k+Z025VjVSU5nJhVInmmTLFK88KpJfXaztBGKvv4lgf5UY9ZWiZsubolNREFot3Xipabo5/3/e+9+3LqhKX91f1q+hJDnWLqGTo8xfiqwW9X9NxMAOzSfqsmCJcPCTXJXoTUc4+wvtZWm5MWYE+fXHjazG5PPxlgVfHG8TRDx01dyxcVp4rtHHiXP0gzvK+ql3B97evacuNPPZIHT+hvFnlyxByEIDAbulXLebgorKFZTJb+ViCuat4fxirNbh0PAMQQ72o75MtZzG9htDeLFb2jfyGmg0SRbQIW3VBBhqLwQgvF0xznPmqw7vbQmSraQhsMxkHNljdMigc2GFXN0fVHAHsuvOAqDLJJ6OZGWxUaGKzzWQ3aKkYrg7vOKeMFSXBSyJW6jEijVU8lz4kyVxvo6Pk24ZsQo4vjDtz4CGHHEKX9m4LM1KLo1Af1Rmf/TQ8hdcgbfHrgguSTi5Pd+lyXh/m4YJBnK36qmPrYAcddBDniHfke7xLci2iS1AUFUHIylA7GhdmPK3WimAts4HNDHpLD1Cl9NgaOy0yp4aP6VRWLVsV0feU1Rv5uOn54hBgcjS5a0tYQ5jqSWWv14/ctYK25WKL/aFaTe18WkHVXv6SvJ/9wLFpzVthvHNVeEln+b7JLzI/Sw+tctPVOTjshrrlhyO84scE2ArqL6DzHIrm4zfn8ypn0zjDSgKy5xw9yWIIW7Bk61xVn9v6XsdhsZ78dVndWj8zlpocAifnoBZBD27X635BWksULZMkrsnm77pLtSACaFx7AjxQ5EHGZ0EEmyWGtjM5mtNdzO+Es3JYpXDoKGrmZZ8qojrb4iNdJSDJNgS2kQCzk77IFqLdGk3+0lEodnZ4/G2Zc1gwAj1Vy4JyApkhLaaDY7QfVhkndYtZF+YNeVLIbNG4NgfSuiigNDzamK+D+MRg49m+o6JRZ52RnqVLDRLO+UpHLBlqb81X2rNsKbtq1xIShvwcEx6IcM5Zdaxl7C6WA1FN3c1yMM8It5XHYrQj6rgBY4yJ7vlNuqA8ZdLvKLYiVBw3Ykildi18fCGmYw5ahFTEWEEOqk8ALSJnmnFtmpG2qfjkVyMRPNrpGKCKE0+L+GEsgTZI2FElsH7iZIQnHC0Tdg6ZYTjIU4guwcZgz5SNLb784VIc29VPhHhURBNoF6UIYRL3VpzqOxKPM3UIKFlB4SFTTwKSH15ZlQz9X03Aiy2VnO1espz7u8u7prLXRz+XA4td51FN/dOn5aleDlZQ7vks1MjJfFWw6W0Q2f0Gp8WsC2NBhkTVFv6qnXFhcOmT2qKNCxVh5DMV9DeZe82HCF5YqBcxNsqnNsjZV1mJX00MQr1bbRxtiSGGP/mZ+rx4+jzzSQ/hVjD8NZ9TRb3XgPD6Ng2WWai9tLI4TGUmrgEFRStUuMMCpgWR5cBMxUGjO8XD7lXi5DEEyfkTvdkNcPXqm6Dl3C5YcTLkDlMFGFu/bRG29kKH1xmqsVxIrj8wv10wvyd9lBXHLjqrz+F/2pS+0c+oAxn0LgONb8WFhyy8yaV1BjEZ7UaECJ568NK0mm+xhVpHoltqjkGGvoKMg6lVubw8S3EbjTNpIXqXoyIHHngg+BxhDoyYqZAxRbCZtRqHSGsX04U5RHflNvLELgk1hxlV/1QXLdimHeOFQ0e/4hCXCXeVW3qItcZfi45RXzLoJ47Y8OdyTBh0JhnjkZOLmwwH16BNTr9AcbIT1ceD9oZVq9SyL3RjAw18/YFgxHAtN2Okd6bQV01xQJn6iFezoqd7dAw9WX2bY1eP8lJhhE0R5l4VJLZrMwkPkQnBG0wGbkrV0bWMTU0sAggaxVtRJitlfjY5K9eIcwwKNOfadKrJyJrDUiiaBtWIDtQYwk3UySRrGRiHxVrSnihLz9M1J25snCBVoFJsHHnXVFIzms+aFrlthS1sa244ktvWDkkdAqtIgCni14jYe4YVa4FO6c2IzEi6Mp3SrhS9s4oXQhmypeYnnO3SsM8pSU4NMFm952ywKUqVp9fKiorPPKOCS+7UAFXJx0lXOvdAd1c6JYmqR/un2M0yyZbOQqGUPxaOqYziTh2kfjmtoAj2IQuQRthyYwSyx0Sg/PGb8BTQlWmK3uvGzGjRZEVO6qMMy4CnfItGjXaLTeIFFi1yfyE3hhwNlQMCgf7W4FpbaBSBVFuKfnkNBnG26it92u8veFUEBYNWTX5tQfeliVLuGZY+QuSpRbzsUKsx/v0ElcOAQpxls01K57Y/3DsL1Jr6q14sJQYhYv8/e/cdLt9V1Q3cF33tjxUQFRQBBQHpSlUCSJMmJTRpQQIECCQQQgoJBH+U0KSFHqRJBwHpIEVKIFRpgghBuigqFvR59Hne90OWrt9ynzPnzsy9M7+59+7549495+yy9neVvdba+5wRz8CBEy+b7Bn+JFLnQhFv+hCWOLXHDwaaaerWLZJQo1kd2hsnCeJt0SwQ0Cw5onNS4ccIhukeI55zzjliVCzQM2lETI6+XAEB4kyHiVCIVJ2IvcUGABFmy9YBJ3pWQUxlypIU3qJHNgg8qaMXnj9vqKUXfvFEqCAkE6ep6bg4XmCEOMemukg1CRanYY0jFTQuhoYYFwu28fhA1owC/jo/L6qny3DQ22gQ27Sa/irXYE/+tNNOo/JESEyIYDEwSWAK6FFtLii1ZeXRZi9ZxGXGBONIOxxqykDo6OfqBFcsDLlCqprEDNq6PeKII0bzTcSABlFqsjQ6/aQEDqSIdcIa/RMwvMi7yxVEmPa9aT2D5iE4XMBu+U0iJ6HDmKTIsTPUR4wn2sQOlAgU6Y43lQ4fp3LLpESzapo+9SEYfgfNw+CZ7wuCoeS1LyrjAt0U6KoJNLxgiFhU8tNMjRgQYyInlIUAHADe1Jn/Ky0zutyZJhCmDtTfEL4K3Qkzuw2WTFjgO6WgCOyJXyqVJsAR8mDKLC2VwZ0YHaSue/+ux+GtI1AyNRpN0qgPNHINUl9zb3ul7EJ3CQuZCxOEm7/0gvltlpWgFsIkBw66QlVNtAUNC/01a/NiHyJngU5Mp/hySeRBVgiDaEr0aTrMhbXPgogdJkjrZfm18jI7S0ZmN2i6s1HuQtLCqhM464QBJ3gWXwAO6dTcx7huISyaDKu5AlU189b8lXFK/zFENj+0hYPTOLR09NE7Ah2BjkBHoCPQEVgDAtxQLrUQnTPHm+HTCER55LwTQVTj/YhPuI88KtvdHFZ+DP/PS9eEVdUTQrbmPEsOPWdUz+FE8q15tDzv0Z8AEEhzK7XlpMoRiO23OX3E65NnqWBeaODwiSV8NYRZ1P7dFVHzEb3uTnDCmRMwIEPkUGNO/UgiHHvssTxLLrXQS004iAzFdcKGWjn7N6KARDbEJqcoND31rFAL+oSDOnIo/O/RDcNaf8syXgi5bWziBTYFpzjEKOdVewVm0qMgVjzppJPEZjbzhQE6V1+cAwdcM/0YTk3vz/PyP9kuUVM8p+Ci6QtZOeg1xtBEOAdb8mPXVLiOJJVNUHTqGfjKa2NB0kPyfHphTMArLBF+2zkc3RoVLRBgNZEqeuTZ63xLWKYrYJm0nXkJHsxaz/giF4By0bVPbQ5Gx+OpkmyXrUijS2o4RC3CrNWU3cILeqFPH1KnK2kIw3lyQShV6xsU5uJeCQtb04YGIMToYIaFtb7wCQ7I0LN8isCJ6tUKS5RR6DkXyQI7//GEhSt6Jg813xc946PcBILFZrjsoknhuydE6tCSCLjJzkjMAdm83DUjwZtQVkavVs6yiJTQMiCSGuDN68MCOWdqKHjIA0Ed1ln0CtPBTsopwFa3/hIGSg1hBi2mEH26eMYZZzA7EV4KUKV9WYZGI6IycyQ9J9rHO5Lm3AR1AFeTCVKZ5MgHeRWu5CPdBIUrKCHtxxxzjOP6vjaTghXdtO3vlsQT+zas0zSZ+GrKZkrUqZv5hi5kfRqKErKRVxTs3nv4giGVqcQRo5sX+3DUUUfVCUo9eDwBks6PCOOBrH9o0GUJSlG9aUa36rgoLehX5wmPLF7YB+kYCMN5mBLSkEbIFIj59QkHBjx6W/qviVBbBopNQJJZ+wsQxCuYTpUHgs2MowHNsvxxS3bJ4sJ+1sNl1IeddFwFYfKzFCQp1Al4mxyWuygBCIFxwgWDGBBKlK2aAh6xSHDzMa7cKFVq6uRXtyBvRtZQSXOVt78SZefbL/yfOM0y2hE2j17vFzsCHYGOQEdgAgErSixRvKiJav1WR2BRBKrPN2zLvbarw6Wz2+mYAEdqWMcVTq1ohDs1vOv8Jw9p2NCGj9hbNBsetrCz8VN1Reb56+HaNj3rULfN4VJ+p707J4rpCz/Jju72N0X1KQzwaQjwFQ3QGzo24sbIF3CHbN/x6oY+ouZA41BKK3BSlcUk3Ds5iyEOMTQ0hKlxcMNO46xqKqNWKgTLeJ9CUy74NJej/+m/Rj8Xhu+EIaqV4cB1HnqinHthg9ALr4EQR/eHkgBh+5ZqcrJ58BAIHBrm5ohEQp/q61/UKp4B3ZALpFEIZxNVTWEqJ14aRSgy62QKaRTIeSIDVsJjGTRSlIMuVyAJhma0h10hmFRkEJX9i5DNjlSAVGJF7gYT824Ughf0ornuq8q6HWYi0EDMqBtYZLvwYlgneoOYX7j0vAaG2vOXUxgSPxx3niuEXNxCgImxHITYyexmdU7YyIPK5DxO+A+xAi+zg2BZPyIkVCM5NG5C2uEg/CYYJMFngmy66fcjHX1XzYmqbb61IQYCftjJ4axJO/rzumrSECI9cotZ4Bo1NdGtoPSss84yKVaUOoh1dTUUmzpZukPGIByWxxDa1gpZZsS8EsixBbomR+Dd5Elk1lmoYERK4e+w1SxLoiZply/wUSbApjlqVBkHck7lWWACTB5YHoAMaaZEWByWhNkhivrE66EdCzphBQdP7almibEaDulf9Ap5AAUxHjZEhgk2ZDOVpJ0W0yN2DCUmKAFUm4dSzHIUWRUNm26jOegopjK4VKt9NuUYAnpkUu5pYiXSMOywaVqL1R/a/6bz5b7qf4mG/YTFEqD1Jh2BjkBHoCPQEdhcBDglE66GWMLGy0LUc9BF3T4TrfhVvCufiTr1Fq+FR8sV5hs5Ps3Xr3eXK5s1x9Fn/uZCBVG3z3QToDlUPP+5YmjMWR8OtiJ5t3CwazoRv01TWO8anRc77cjW+spEwqn76YP3qkFYPObjgHfTw+hXrrwI1mf0bl4ksYIQn3zsIm+NFjjrQlmgeWbEo/WjPv1ow4mLJGFRvSBp9m99JrpdghfyI8Ibn4lu45boV5pAwIMdtlJ3BIfomcBLLflsSYMKtN4xGZ+JyuAVL/kM330zqxUcHFCadbdeF6CK6gmntNH2t9OjZzI5p1GScXCWwaeSNKtMyOtDQLOq1evE0ms+fOrF0bL438ctttrzINuXB2IwJwiVHpaHIm+py4yDdIZPbTtaNhGRuc+WBiqakwf5I/Ij7xm/qTza7UIXycNCKXXS6IjN6CmbHDeUIr/OXwCd5M489VPv5qmcdnieymuu0xMWawa8D9cR6Ah0BDoCHYEVImBHxflPXibvypYOz2aFg22ja5uBjoSIOQUwzrhu37feBi2HsikcPAeBa2LO6dD3UFK5SWOTGakuuMkXAG2ewH6TyN8xWmw7O60gUKfj3vIwnS/YsVE3ryO6Y+9dDktgL2swf1Zx86ayLYrIg2dzBOqSnqL0+g6RbfW72xrDQcLC0QaLoNzQEgmX3TbjfUHv93rxz6yJysrMutWvdwQ6Ah2BjsAsBDL04kjNqtOvdwSWQGDWyfDoyjFj7wCzXe9pZ4/We+BWDDO9w7MEDTvVxAaUjx1XL07zxGxqzU71v1v6AQJ3yxEPrwWZPsOyW2a0BjqBZu/XdqvD/wsdqFkDbescIoTHsQLvQWhOm6+TjEM7FtNBg6Sx5D29UGP+Q16HluwdHx0O5MGHGSEPO3JWa8eJXEOHgQP74PiVh0EWOmi2BvL6EB7qWQKE/g6LJUDrTToCHYGOwBQC1ks5fjVmPZo41bjf6wjMRmDaB/X2AS/zc7yC704CPcbs5XOLnnKfPfjO35HR87Sz502c3d353ndPj56L8UyyfXJO9u6h+hBT6r0J5Hw/ZyuCASSH/Hgq4RDz41APTx7Yk46DaJDj0XGwGrIP+zZ7dajVcWr85d5h0RMWU5j2ex2BjkBHYAkEesJiCdB6k3kQmE5YRA+RLFMmh/P02et0BDoCHYGOQEegI9ARWAMCyyUsei5/DazpQ3QEOgIdgY5AR2BNCPQ8xZqA7sN0BDoCHYGOQEegI7B6BKYSFv0dFqvHv4/QEegI7EEE8oTFHpxbn1JHoCPQEegIdAQ6Ah2BjkBHYF0ITCUs/LrJusjo43QEOgIdgT2IgKeL9+Cs+pQ6Ah2BjkBHoCPQEegIdAQ6AmtB4DxrGaUP0hHoCHQEOgIdgY5AR6Aj0BHoCHQEOgIdgY5AR2ABBHrCYgGwetWOQEegI9AR6Ah0BDoCHYGOQEegI9AR6Ah0BNaDwNQjIeuhoI/SEegIdAQ6AitC4J/+6Z8e97jHLdT5TW5yk9/4jd+Ys8lpp53m59Puf//7z1l/RdXe//73v/71r7/xjW985StfeUVD9G47Ah2BjkBHoCPQEegIdATWj0BPWKwf8z5iR6Aj0BFYEwJe//kjP/Ijw8G+8Y1v+Mn6C1zgAsOXKy/09iIJET91Pux/zVf88jxK/Pj8msftw3UEOgIdgY5AR6Aj0BHoCKwUgZ6wWCm8vfOOQEegI3AoEfjxH//xE044YUiBkxF///d/f8973vOnf/qnh3f7lY5AR6Aj0BHoCHQEOgIdgY7AJiDQExabwIVOQ0egI9AR6Agsj8DVrna1X//1X1/obMjyg218y/937geZ5znPzNdUORfjWMpXv/rVD3/4w5/5zGeufvWrX+c613EeZ9bkvvzlL7/rXe/y6I0DOypf9apXPd/5zjesbOT/+q//+ud//ue//Mu/fM973vMDP/ADd7zjHc973vMOa67hCmLe8Y53vO51nffi2QAAQABJREFUr3OSyONCl7zkJZtB/+Ef/uHjH//4t771rXodCD/7sz/7a7/2az/6oz9arys7xWNSPpr8yq/8ChBInTk21Xx1fAliRv/oRz/67W9/+4IXvCARPeyww0aPOw2b78iVoAG1n/rUp775zW/+wi/8AsZd4xrX+MEf/MFh/yqHPJx99tmf+9znrn3ta6s8PH4VDU2fJJjaF7/4xZ/8yZ+84hWvSHhmyYPDXG9/+9s/9rGPafXzP//zELvmNa8pkTqkYUVXTO2v/uqvEAwHHLzQhS7027/921e60pUaxpEWLPuLv/iL0YNaP/dzP3eZy1ymsk/9r3/967rVhB7B4Td/8zd/67d+6yd+4icmJqLVBz/4wVe84hUyxTe96U0vcYlLDJWObvp5qS996Ut48YUvfAHLrnvd6070uYpbCDA64wA6FF760pe+0Y1udOELX3h0LBL+7ne/+73vfS9AfviHf/hyl7uc5wop0bCy6ZMu8kDv3L3CFa6AF7/4i784BMFdjPjQhz6k589//vOYSON0C7FRs6YC5jJlyNYWthe96EWHBKzuiqnRMtSa2te+9jVGz5OV9GKWqLOTZvfnf/7nWPxLv/RLJIdMji5hpkY3zznnHPX9ZUZ8RieChn/8x3+EAMvzt3/7t4amm9QNwqP1V3ERDab2r//6r3BAyfd///ff+ta3HhUGo6v8N3/zN6ilFN/3fd9Hckg7Ro8SRiZVe/Ob32xqrNlVrnIVCE+rmybkjeJ/8pOfNBD7c4c73IFtH+1/RRf/4z/+46//+q+DBgbTYvR7v/d7ZlqHw18r5vve975Pf/rT//mf/3nxi1/8Wte61mUve9lRUa8N91W5Jyz2Fbv7ZDsCHYGOwB5EgJ836urtwalOTonfwzPj+vBx+YLcRC6dUKppxLN/2cte9qpXvSoiATEG9HhIowGq8Imz9djHPpYvzqfU7Wte85ob3OAGxx13nDi89mxQTuqZZ54piuM3+/qrv/qr17ve9Q5VwoJf+6xnPUtIcP7zn1982CQszOud73yneYmolXMiJniRi1zkxBNPRHleVBDNPvnJTzZ38xLravuSl7zkdre73ZFHHtnEJPx12D7lKU8Rc4JUZVmDP/mTP7n+9a8PNE5z7XZF5e985zui4j/6oz9Cw7nK8X/lm1wRyN3nPvdp4od/+7d/e97znvfa175W7MRd/qEf+iFwkZyhPJi7PAXQPvKRjwDK1NQ3NfM9/vjjRVx1OioA/wlPeMInPvEJWRKVCcbLX/5yMQkcRJ618orKRN3bbdDgQJl5mZHo6NWvfvVtbnMb58tqtCO2edGLXvTUpz5VHZQnPWIGYn/5y1/eUTV/4zpFO+ussx7zmMeIkN0VlYmu//RP/1Rw6IU+4o1s3hQI24tf/GLahwXEUmzWgCyto5/nP//5X/nKV2ALNy8Jkj9qqjXd7uBXuiC+IjlQMimguSJKxOX73e9+0hY1iAIUg0Mv3vrWtyqrTELe9KY3vfGNbyQPMnqVMBWA9uAHP1j/aupHt6ROt4xP7VYrQKEBDoQzKktz0L6jjjoK7wBee2agCPBb3vIWqVLXxf+C0nUmLASlzOPTnvY02oE2ou4Kdfud3/kdsxtSQn5A9MhHPpKNUhnlRIKA/e7v/m6zkEmCUK5XvvKVUhUYQdh+7Md+bDRh4a7RySSQgUlyGCKyBIqHPexh0m2jWaEK4/bLaKDsz3zmM2UWaJwOL3WpS8nVNgYnBiIqSH30ox+tCRDQ/IY3vOGXf/mXKabMVCMPksvPfvazX/CCF7BsKjMsf/zHfywNzVDPWl+IEHUmt5pINYKOeMgtIqnpfPsTn9UD9pEKHJTBCRqsjJYSTAmNphTSW6SXYUReZJNpE+G5853vfNe73rWRh1kD7YfrPWGxH7jc59gR6Ah0BBZDgOdhu8ymBD/eboYPL2GxLr7ne/ianBIrLo+ztuXM6Vko9VM/9VOcuRo2RDWttM2G1ng7D5ZzNX/mZ35GnNw4rBxrfVrs4zoHha9WR2zK/JXh/rkROYW8B3sgqKq7qU3zjf0K1Sc96Unc38hBCNFlK0SeDcGCore97W32RUVWsFXgNjV18mu4fcI8riQH8V/+5V+EGY4t6JmzWBkR6RI5CwG8/XZg6tYnu1pngQCIcOx+B4XkeTi6gBDNqJVYqd487tuHr/VJlzhTvETGBCHcTT3DkKMJ6rvf/e684awPT+EHf91pAjtp9qWF93xQuOlWvqCClq12sABze5sk4e/+7u8kEWzzChhs3xEMUahkxL3uda/wjGNQ8iAAIAlYLDDwmcU1AiYGkPtQ0964jXfBpzDDcPzyAwcO1MiEAXHR2QrBkl1WaSABFd+dLAnCTz311GEqbQdB0BWm45H0irSF4BnBeC1GwseXvvSl8gVCgkwEYDEcWB6IqZYIQEMGEMvQnOQxR+A1NQg4/kBg4CDkIHLiyVNOOcXfrJwF8iasJQkG1b+x8lYWqBtOsWAXu9jFDI3yvLWeAjEg1c95znPIKlFnPRAjB/GBD3xADs5ePW4mJbSM5PzZn/0ZSwIKeoFm8gAZuUKwADkr217WLaBUk/FkgQmS5o961KPEnPaTs6aCPIh+GHzpLXki4oqVeKcHY1WbhsvYoR+CTfwsK5on+2qfqyuTEIG3v8CR6ISSslBZVsI0H/SgB5GoOrrM3ROf+EQmgvBoIuEiAUqiwOWoRbVF5IHMCHfltmBLRGdNDZvgKVOgpqMr2CE4p+8slSSyh0BXrW4mSMJNHA2UBU8lQFE7i2ALhNQGm8CYHH744RwM6gMZ6UXCL62QiFnf3SKWFm45HfKAy3Ix8jjyv3JYjYOhoYMVj3/84+FvJZLvc/qJHVaZ/7C2bIXpmws6SeYNb3hDnJVK473gcpodnGU3SLXpo1PmDvcZakw330j3rI3gBHwzCweX2M2kr1PVEegIdAQ6AmtGgPNk44vzkeNaRPlA9pPnT1vwYnlLvJbqT4gKbJpxRqsTo47IoZ43FuqcfvrpRvRAga0GfmoNOC3/DlXycpI8FVQTFPFLXLT3ImzOu8MCr8VGX17no3PpBGN5RYG//vu///vGqhc3vAwlUZAQ+mY3u5nDwNz30X1sftvJJ58s9aACn49jVNlR56g3Dignkpt173vf+xa3uIUr3HHeuRPgPE7BQ9bnNXLW5bZ4xoJ2CE+njbLhKgoRSIsWUDvh5Zu4tIIgPIMEhaGDaCNUmG3uN7/5zU866SThK4S5wk9/+tMFCaRODJazkOoit1IhHFCy7brwTEYD1CIr22sCuay8ioJJUTR/nZp+yEMeEkdLuMKiPmkXyQVnPWo8QAwe+MAHCnik6qRa7GTOoopN0DNI7Z/LXqkGE7Lx8Ic/XNBFTuATbY1usrjgYYpjjz029oTRYwgksQBiWiTNGmhHrqNBvlW0I1VB4MPCKAsSJI8IsPMCTEGMRXrFzDh73/veNy/qAdf+4A/+gFSbZlIVGVJM123YHDUlWAVg4kM7xh6oycpZoC9MoiBcxDIrE0E2pLTophBXVsUnm6+nQGeBJuC8xz3ucac73SkMPmSOPvpoFpJVrwkLcZf9c3JlvmlqZKakbERrjp9kwgI+kHHUyAQdQpFEMx1SoczCWG4kDWsiT9Rtpx3seg59pKdosGVNgGvCwl39kGFJIklnQ9fFYj2gkQdDW5LIdvxSlaNMpMgZCmuTg2zWsqQEc2mKiJpZcPYB5bIS1jtZYDkazWsyUehONzWR3He+QBIk+2kKOEUUiY0eZCvchbnOJewIJN6tIWERUTcdN5YNBpmaWbxgN1gMWTDGxMpyy1veEsHof+hDHxqpVRNPZ0PiVcKC5WG4IIzRuiUbQJP+Y2abJyysPrIAhIqGkiK2Os17A9rqvmIZZsnPMr9O4Vk6M0lRB4UDw4vjEjEO48SDddZuF+V96IupDTdXag/7p9wTFvuH132mHYGOQEdgCwQ4Xi984QttenB0eA+cS9Evf8sWseeZnVK29KY3P6svzgQv35aXCIHXm8utDSIBnmSE9Zj3yeGQKfCMtG0Qm0t65rM2fYqlubMcDr6g3AHHjrcq0nAImWMaq3vTxFfurK2M4XVXOEO8H85Q3rVX84xnPIN3xevl3wjmjSLWsqH3h3/4h/aiRVxZefMLETgJBZ2qnUUt9yj2M8WfAmlNZtXEIDgI8HRou1U1XpedInELJImE4CTPrHIKyUaIx3TCaNZwO3VdNMhTJMZcYduMnNqJngU89XzEsCZ8nLvhBJMNGZkIq2QleM8eNxB7Cz9qwgK8JLb2w8MWsQhWZTF86q1VlM1I0EKnJN1oWQwhTibhYCHeFLkmLHCQSqpG/aehiFSF/jNqJQ/UzUCshFxMTocRsIHMaxfnZzhBQoRS4hkMkkXKyisqoBO/GDGfEEsDCcU9uEF6EQCHvC5hcfvb3x6FPkkP4XEcgwUzxxpGQk8WQ1fi6qislW7ZPbN2lGCYsGBhBDCsmVEkBTxPlKPUglECWxCNRji18irKzCyjLYBkojODIC8pH8EUiHuFWEkYhG13+1RK1NQJWRJ05XXRJvEQ1ZO0rE+cZC4++9nPClyb7Ce5lZXO5gpWEwYfy3RSryu77qMgBp6wZk2rHfwqKHVigpzkEgYiR3UIP+NpajVhQVMsjmyCZ1uss8igEayrfQIxKjTqYRPrb6iP1XOaYFqMZT5ZjUyix1LIjFdeZIVVFKSoIkslIznRPyaCRQXCkI8OWU0cOfGqDpIm9Ynj0QPdsSKDV024uUjwLEOSxUJ6YMI/ZZUAMMgSr0TimGOOkRWKTtb5Fw0WR9lhaSYJ0MjtjhLAhpBzpoNhzGM4hF8ekJ9DVACVHtRoD/vnYk9Y7B9e95l2BDoCHYEtEBDaCfN44dIH6aBzMX1s/sgsyCDY8Kk+fdMjP/W5z32uLR1elw26dCNUs0EkW8ERsSUSrazW1mbehqPjNidtN7mSHdqjE/bYyw0HyHUOjQ/CBMz2SL1AKyvXQnX46nXuoGwFB+5Wt7pVXBc5OLrMpzTfjMEiwuGjS68gzJ5POui1t00u4wLoeHXTRIo9pv17bq6dQDtdEkYpD04NCNicWRW9iEMyYVHHMnr9us6yGZFh22uEVtJNDDlNDBng0IsHFPi4vMMqtCjXoT1nyR0xbYLgumq8ZzGt0FfbiVBfBe47MgQw68l/2eFsYmb0IwMNpmAioxzZUh60zexD9iArIZtj+rVbsicMgw/lku6RLon6zqqA2q014MBMfTd/9j9nKIIAnAp+YV8l2N2hvkinOiSCaxljRyeEhHRFOf+aF73TrSAzL2aBTDocLoAUvdhLn9Y7rbbkRfa8swV8ZPp8arfkn46gmQAMUao1iZmkDIQlIxjSvOW6TnQOutoDCWFe2BmC0QyabRUMLXiTDCJIeZSjVojytKYP6+/UFctWzRREt1JOzKO1o5EHs2A5yX8mE9WHlWUOyLJdo+sXeViUWtKIF5ZRvKhjLdrPcvWneWE6QnFspS8+MQTBgKRcsFtW6kxYEB4SYqHJMxfqa0WWICyHpUJ2Al6n4Vgk56fkGQ3kgws+y01kiVZMARr8lTB1rGyCBlThjk8dhaYQHmiY4DrJrjRsYLknLKaYQpd8qm2dqr3P7jFGFv7v2oAZVgB06kBvIraZxkwPzJAeJhxBQ0i+GsKyt/RA02QsehfNKGdbN4SeLelHrc++lXPyYzmR2963CKSEWOMlArgLdthy+c+7toCkG8RdTlsMnfWoJnRxWoE3JiXhiGNVAdspXH8uaWYrsmeumx1pqRBbCnU/xJptNzKzFVnfbj9vQCCdV+YpoMqOB0bf7W53S5MihWEUezWZrciuZG3s/nl422GBJlzJOnu+4DgABeFwizBzsr7aQWX/udd84ry+IQVS6hwB8jw2zE1nkGcRxu4RUdtxZNu5A9WIh0cGvOpMUJQGQcFGmeCWqNTNUvrCq9aJ64BKocrhGBaRG7F3PlkqUNxr0zVD96y2noL9bXEyfsk95bmA7Q9NBuiIaeq2BlqAdcVRJiom6+c1H5JBoPC8CStB42o0u30y5u9Bgsm5GHEOAmadw4reYGX/VsIFXHg3PQQ1AS95ELjW4zbRCkqMj0EFUTAhnNO9bdRdYuxAinyB1I8IsFr1pJMWYCvtgJin87iFatYwjPpQIsqoDqxCC/hv2CE8kwcRZ2ZvtRARqXSPp2Ootp3nelqh1tyoMo5TebG0eFVGvtIm9vaJ3GheBwgQIlLNi8sVwiLB2SopXcsXZQnj2bTlOlxFK6kHCCBVNpPtDfJImrwVu0paqjxYcciesyfwTGJYXc8HkSjNq0JpHkl2fXoZBPOuDtMkeZ3nX7KTFRXoAhqsCGjgUzlARIyZBTTI9Y9qUKXEqT1nTMyao5XHLmqF/VnuCYuDfKc5cVaTIpEn4uWV0eTmiCOOGC4/B5vt15KzWN7hLCbxaNYoBlwToYsVS3jQ7GOM1h9elBiOt+94cDF9x1qN/UKDPRAMsusrGVnvrqfciA075bA6r8VTu+tPaY9OmU/A8QJghqC+Whh8jWQTd9PxOfvenroc7WGvXuT9kB/ht0XF3v4wMN6rE581L0crLe0OuqeoNDXdkrDgh40mLLgaIhO7Cvkuidqc8+Qrf71ezLIORRESFnYkUtmREc8DZ7UoWMIlKPkltG/LtT+aqBxP5guctM0OncLVQzzskBezIHY1WbDs24QF3IgET7pa1zAm/uK1uwnXJhTQg1+EzSFb7GP9JqjCesYwwics1lZWy1l9K4sXcFTZk1PzPEgEY8IPx3zUlIYg83AIizocyN1HPOIR3qjC9fTQhKUwHtUe1lz1FQGSeI/vLkigYjX9tJ2hKSAFgYOCHEQTSULM6xg8V+W0C6b4CjReFq+dW9UcfNgOGfO3FUails8gW+GZqWnPRMjkATQOoSA5jdLoWCRHgCEyoSmynPWJM/UJoYBf4oajIiELq9FONvai5ywcjpOTgpinikbp5DATMMsoXbBJ7m1Hzctlhc28QYJnwfVojGPwMuOOzXM/eE3CdQ2HPcNKsOdgv7wGbDGCZ0WVhjU36oq5OI3oTCJ1k4sn+UkeUWFUWR42oaY4lUmahoxqVl6uQMUcG+SI6s1ix6+TgYXecr2tqBV6qAlRkYqSX2ZgKSM1IQ9kCd/Nwt9Y350Xs6Ng54AZYT3okWyF80rkh2LK8lSdYuukMLi4zI5dENrnriH4GA5LslHTurwj80WSRIyhyYBAEjG6JfaOp3kHh1zeBA2O2Hgsl6lEMKNKcXaEpD3QSU9YHGSixckBYIk6Dy1bShU8SWUx5qP3hMVBmP6nRKmYg4mEpeWNyQad149NuwX/02X7n+F26puHQe2H6s0Wi0D4gqJNHmQ1WG1Hq/wuxevZRSuNNVUcxcgKutgaK8Qqh12gb5kjh+0zcwQobz0k295FFId7vRmLj27x2FcJC0uI9YPK8xuas9MLgLu3qsrgmNBoMiImapuRbeQNDFXS/hsx4ysI/rkUQ2Cs39SEHA5vucIv4YbyXThzvJOow4kZKn7c4odxWbgF2DfaYb3IR2Qr1Pdqz5pGJAPmYlJc51o/ywg2X+qcV/ZbAXRQwp2GEXJJwGHuwhXbHFg4teybRUHWTLSQ23Th+FY6zUiSwmEi1XixQimTZb29gNMDTR5rckDAnnA0UYdJt7+ngpyXhAVlYTmZUxIY5y9q51EmpfwHQ2uFErudKtvtXHPw4Hw1p9mL6C3EMgVIGpK6xBVGQL7Pq/hplrVDzzUAiw5dicOG6ohDKCyxkfw6JNuGPAp2AA744n26tr4nZo2zzJE4mclqEjFNK2IjdvJTF2bnIbXb3va2TQX5EfiTNxA5mkRrosJQrZqGm/DVpp2km1QXq27rKDWioQ2jocTAci3k+wSWchC+0sSs6QUEd7nLXR73uMfZiJJSJAaQsS6QEGUqljVrgX12zg4v5Mo94GCPAYyb7JPjL3mQpyNvoglbQVUvaA2BMUHbRdWoEoZYy1I8KggLlQ0ns2MllW6DmIwPmSeZcaploa5WV9ncHTcTHfjpGRYbf63CJIfGoZ+VsIGURpvWeN8Hs2xG3tLqURH2xFstRAFAkw9KhKmt0EMKzC0GR/9ifkGEPTnpZu+K9uqZiSePdmq+QQNGswmSd9J8SHLyiNj73Vl5vfoKoTqoczEqSHMg0tvKq7tSq+3Pck9YHOQ7wWJkSTmTGlf5ZBb4WY88HGy5L0sMBHDSTAwxYI+4ZexOGp1hnekr0cOszV62wGrHxlF+exp1A3C62529K0KLs1tWJj2brCmbeF2KdnbERXtjOp2Lk5+2zAeFtnosqBL/kbBwwN7iOnwCc9GBdld9foPVkavklUhWlEPiQG8aYjaEmbtZLmlQy41QjVBV/9KmmS240HRugR+is3NSZwdtTejFxEvvdatJTVhk5qJ2FeWF9Es+ToLVfjsPqXYVyVBujdPa9XotWxeYGnXWHGRWGg5hmV1l5E3fp5LhK8eaB7xR+z+Wb66etALjxmVHcMqJoF3iiUQJVnMiUhJSD3UV834BUmFNsassmZW6QLYd2fD7INIZpF2qQlcSnQ7TGU55FAfo6ZA6+H0Em2bsMDJo0DozpFYoZwrOOOMMUDgRKY8za0lNWOYp0GhZGD9AQG0FovI+wxNqXmdrm9evJDirwq2S+4Ob0B0Owgwp/njj4DzDbb+OczSGFu7aixJIy7CkbIx2jlMiZOgxGikGw5p64wAIwuGgT9OsAqY+mZTWsRUs4gr7Y1zi5KNz2wk6F48Ne96EK1wsUxPxenYGi5tHGyqF5F+mW5RFHeigHX5Qy1aAOqtRB0stYNlbUgEBySBmGc6sa11Qsok6zsL49QSKZvtdwGkFAaCwc7ltsOx5RQXsJg/EnjyYmoC5cU0B5Yq4mgklPEmGKx4+sv5u3xVh0NgcD0GweIJkeVLpV9l/qRN45oiHvEBTpFFwk21kTNBGzIDG9kKpkQey59Qb82sXmefG8ydv0uVMCjOSNpxdAiwwISlVwbuLlBkV44FoSBNtzq06rAsaTM0ylL86ZEbS1h4V4YHTlKQ5GWH7kytOfTDL+79mnWbK+vutsHzCgmpRSC4LubEOpTNHUGgsHIVt6tiFwDMVUmnJkwouWjUlyXRCNG1uRHKxMoBd4zHEENbCap7CieQTEwtDkPvM47qC60YxaG3CNFgeDIpUzY1LPZJycm89Q7yLPObIgCYx7poL8TLZvKgyCv0dxu1Gd8sc1ZdkJaOSxDlBt1wxkFkPXQdDo002znAmNXTZkacCkqxzKjSKF5C665YPGpJgBdSiRx3QUR405F3ggAibtJXzBrsKMTp+YYS7QzZFD+5y8nABm3Az+xwWkgCVG3sUlY1lZdKJrhria2/6ARGsoMTGxQJgCq4ruwUiFirRY6pIhbu6dT0nrgfCQCQwQhOzsFqYpgoqYxOs1J/lr8AEO9Cpcg20NHfRXCwYbhGz4SLkevBiFhR1vsqEyhSAY8oozKkZJaZA46KJmq74S+RCdBHjKwrVgVLgRg4pi4nLZUj3hiCp5rqytqFKekB/Sm9SBWT0E/4QJFBolcBmNQWypKvQHd4M5uYJSUoHdnfJKtY0wqxtsNJ0sKBKV9AJCgTgEWRMhJUPhTJTQBlxtE/dAt80dasHPhPuTAhbncveLkOS+kxDQVyBoGbqL7T5pqDm0QpFeLfOPTm/U7ECNQmBuf23er0pY586eXFUnPLunAU/h2Zbhrsz/NUMlOuEGG9JFTnMNW7OcfdGNYpPYbGbquaMGBBmxFcJi9C4vHVoC9jkhAW7LSHroUXEMF8oJ3621p2o8iuDkcgIOgkYC1BpdsWxQQbKkmHW9ZaZOhwh5mTESI69L1kwv9unh6F5z4Y6ZKvD9eSnepGEjcG1JSywSbZCzAkBAbOsei4cSeESBeZX9Gjj3f6tuXgec3jWUh13xR5SQieeeGIkx23CMxQnnHACKNxdW8ICKwVFoh3yAAe5++GK1uBgq9OuL846iJFra1OHIohO/aSrbWEhorjaatLUiTCJEJJJtog8QMZXrBHVO6bKbOY7gJu2h/YrBtnslW1x9o3kCP+2pMfy4eUvVnNpayyWiYB2tZy8KYkqaQuIgYIngy+Ob1istZrVP9WjkvJBtFuyQ5aHZzXx6s1Z/az6ujXOg41iTpbBLtpxxx03lHDLa/hCYgrOW5JEQ3lKJG1HNFS3nHw/PIEj7JUg37osjTt0sZKAQ1LgRRAtz5VjKENKHlhpO8dErjGq7nqSQpwPW+rMjFAip5vJRk1YmCAXBciWLSmbFCr2h+n2YAi9Dmd1pfMNGhDDu+Y/x1jK9gVtn6AB65ulRyTrwK/fJIKJ818UZ6PW1pXCNWfn/2upnrMNZnu3kDSnpRfo7L4FyQNpXqXGAIkTHBF0nfkmeSwLrhA+iWc/V6OCYPi0006jkyowVXLwuCKH6rylKyogw6ISQ7ibQzhoJ/dGEIU3Fh6WC0c9dGDvwvLjY/HgLgdhlgRC7FlN+wk0Vp8Otlm2SbD3J0m0I4MwGZdk2B+IvQKKrSYrQ7ERHMT4a0eFo6Oh99Vn7ErmPBDFvliMIVDREz55TskcreU2HmHC7tMWSxRMSKQgzUSYYDsexqJa0RyRZ555phlFfoROOr3pOFyoLijYHblSdIJI/zYuHE+VDdEcLDrnnZia6VNUTpL0dmoLfjkYxnen5ywmD0P2N846qs/ImqYrlhmvf9c/rmEKGpz0tnSp4yCW4dLZMgUTiYwgBw6RtNFjug0aiQxDY3YSnAhgTAXJKueqY0SzC/ZhDVPLNgkss3ktML72dtg4TOcy2vsigZARe5BDCLvlEUrwGssKR5wiYcEWkArJy1gVOLVIInjm4jfnVGZonGm3NDpC5pFULLPEsqfEr/Fa0OaJFT8dJ82BNqcloW2VIjDmYgOBInDX3GKFUWKRTkaDggMNCh62EU0WSf7WOdaylJCH8dBjgsAhOehBFeWiAg7UYZwhoglrDhx/STK/QTApCHSaTgzpAVpOGBbrhK3ndJJe7gLBQB5l4UbYuyAz3Hq8QKdpcs2pg6lF/3qTtud+ccVgAnCiQvXoY31jYtJPLIHJJyOZWINZNjCZEb4a1jDTBJtakSvypqtoiLOmJvQl7WQbvziOKoR0Eeagk0brHNm8IhWos+nQArRRfAridw3JcBITBcp78skny80jg1lAvOR9RuBN5f3zlajTaNJLPGbNOqQ9zaBq6lNVrLEWECGvniH23NwI0qIftwg/RohVZvW8iusMF70mzwSYjjdDxBFZImT5aG71r4EAtbKS4qmlnCmINZG1tzQTEiqzfadKb/SR7dU5CSFLS4OPxZahsO261Q+amReLl7+MlXVny86RER+thpVN2cd1azTLQx08V8ITHdZsrjDapmZxZ/P1PJRGJgvI6GTVLRkS8U0Pi35FIRvu+L1AyLtjcqNv0X6G9Wm3JyBsv5u7FWR05TJHj4nhgjocrezEqRY4WIM0t3bk9SxYuWxCsvkgorkM/hCrrDxPAQ5WWws9YeAnWAebWGjYCeIZMYumOGfWC0rVsYRZaq3OFjXvVmheXRHdIt4Szx9Tn5DHRRzxFa8ZRlZ3SMBCV1hgNPB5FAg5xDJOW6ifWhnvrLA8BF4f34azQSlqhYlyhMrQ4yr41ISFVijkUfgoU3y+t7WeCA2X6WYIpsaTIPHC1NDupsJCXwkYMSNsWiGYI9rQuVBvKpuF7NXpp5/OzxGqCBbSuW26Ig8WUPySWs0MF0eIeNiA2T7v6nAsCQ6izVjkv96KMu3A65BMVFHP7Zv04SgTVzgGvL5w/JyA4L9RGdmxUVtNc63XejMXzqGdBnaSVNTgX0Nqhb/pb6uPuS7y98yX6g3poYxGD3ngGMQ+6LDanFfQIMgipZUwku8iGihFQwMP1qkc/rDVlhPLn1d5YizTt14QYCrPutKdCZ+NtdE/ebNykbdRYHMs+NDKkExr1jQZ2Wo9hWUSFkIggTppENLgq3DCYzk4DQvLtusiIm6i4JNakn4hFhFUgRRSY3lEsRyG0W3AUWmmViQmeJCwdzrdzJkwtlIdqQTOhyEEliqo7wpOW9ctmf66ZVsVptgmbBN7YKSTQpjHXJJmnpZjnCSVIIoPuQuxfuCxW87eGF1aizQLb9wyuoL6yQAX0cCaWF/FurnEIhINcn5D+2KOUsv8EgGtWbAXNIfJENx6DyWVswpSD3XkCPRsBVVBAQKSBei3xmuOfpkO8/UsEzLgfMopp+jHoOQeyEJ0rdTBCHZcHGgimqNf7sOzYUzngQMHzEjkKVTAO6tvYC6MlPTRRKAINPACWTUD8SckWaxVviLMFLRyBcsoCb0KX0pNUSuo3aUGFnj0kHUeUmZJEkbMklmQLtG5XAnCRJUgFSiaDgJ0JZPF/2N9MBoxrtC00WXSoGaKAP0rEACwmALENMRrroOLmssaoIpwxvkxU3aF9p566qlgEZ7JfbhoFE3ASEhMUKhMvc0Lzu4SFcLsQF1OJwosuwraogTNKHFdGVbWLb2ZKf3XJ8uCBht0KoAIL2hBQIEYji9+4UUcGW1GgTl14BvJTBEM0gVGomJts2kMSV2lWGpr1oSfxZFtUSeEGWIo9NWs8RTgriu7LvaggKJ9bTUhk2iW4nGX66N/+0IUjU3EGp2TK2JssuindzIpGhKS6KEh3lfJBcqiH3zBFA0xy2LjeCdKTBkldh1tN0FJZtDSpVvnGM0anbJgKCEqBsJi0k78DAdVHQpHWVV2hmoz94g3HJvgospYj0dc6hCVpM1XlPiLdyE/o2KW9fdJAYvZE/I24TtK/OFaxIQBC9WwSRIIQ1vwzw7LTGEKLkQd8HKGyOQ6kUSqbB3+SrOS/OHQNBTZ5ju8tU+ucKdCC/xlCoaztlqxz4wkG8gIhFtJly1etFLSOczLsGH2loVhHVesbowtj4IuEx5pU5Hw0sqI2giu2A2dmJRllCiilu8hacWkj5KRF9HDbrDJbMhwZc9qCrYBGR9mhO1tEhZMtE9N6qnPEeJsQAORCKtdKfMHZIHtcyCbQknlSzcvjUN0aCvPWqYslQyWUGprE72wXmNfQ4OvIQ8K6KyudtYELAfP6kYeeA7OVkS2wnwt8db9NB2IB45+LBlmlz1wEfFa58xIXswCb95b93SrQLTkF2SW9ZMVFi0QAEuJbIUR7ShwpSzZOmHoBGlwYB+GfbIJZAbZFrXRhALyCIBsBTwt6w94wAMiKaPPWIDSQmru3LvUecqktiSHMyaLZOOBEg0JcCV5MUs3sxW7yuRit3XTjKyhZHI7woO5NqLCRXFsJN5JrHMLNENqiBzaUg5hF33yImGgQeqTsVExi5qwwhpiwyMdvuhBt6pRluyWbvKdLP0Eo1GurEPeYuIKeXG0wEeybHHz4MzEeWYqV6vR+tMX4cA/xwXywCuTrQiUOLQkTc91IqyoEED4gAYeHf7Civ9MMQnD8LBSDF3lYZQY4gpS1oMhzQpiZuaarlHMoUiQSWLMCSe06hBIXlltnv0sUQheGHRLXkTniBeVWGs4eHSqStRwdBlPBhPsnrkjP7UCqF0RSUGezISxxQjePmWXwYFkrR9lLqjNLYEqHGzOCUYmRHfYvLmCC/hIC9h8zA0E2D0kmRc7WWlQx9vKJZfJibzn4YcfHr0RTvRL7Q0BdMu2PY/X7CxtFotZYsPa2JAjmVxoMsAX8qmjV8p5/o4RWDXABUOvCwFvrXBoyyNsmybIYiNwwngxAG03bfogihZbChgs26STuOMQdRUqmzMptEXvYxeXXYAvoXHRLcuzYJ6GiyFxy2EEZl0FvVFd8S1kSQ8L5dAd11M4KmGBQhcNgZiIt4mgqFISnSHTJ/7phEBb6hjEww47LK4gDBu8pttWA3eEgLLFuGhloqh8JnvydD4OU7C5lNlYJAaRMikIECMpmKOh6bm7bBPRbEALEMzR+QXyZyVDIf0xQREgTYADMWLghM1iKn1a9SUIxI0UVUgmuDU67YWt6NT2O9DEjSSeDEV4gHJ3TdxEWD3ZBNEmwbXViQDmz6pP+SUdGEFD69/cray0gvMk5hQiGl3ECE/g4Ka1XJQoRGTjUG6+2CQBYSI0TepHt+CKhAUKKRIw+UMaEgCGz4jYx99KTPACqqJNHFFTt9CwxNI3IiHNpHPs5lKQJccF+Sh6MzSO8B2zn1qQfSAzHFB2FsHOe5MixFjkzA6qAKGckhdyAagV3hMtrAQmCeEuWDAcXdHErF1nqnxFqsmiCmiuoMQcoSTTxL1wFkaFJAPI7JokAsBxh0UwNAHTBHNFa4QTW5kAZxkID6uBubw3FoErYLjY8gKFxRIjIECDmtVCb3J/fHr2yCyQHSkDdMKZYONd+IWVMBfNywfH4QBVMgAxzhNeGFcqjRRxRNTUEP0qK4ToEiSOGh0n+SwjMZNzlHSQsMBEVlKkR4wj1QVh+KAhekgysuC6USAjlIUhY010aSvDjcUwMWWMZi6AzOsiw5wYFgPaVNjJEeRxoRgBQi7TEQkIrYDDM/OVdygswXdZPFMm+RYbcySQCGav5K2THgXWCc2qkRAKZX9sFvG11Z4vE2ZaTIWHT0/E3HGBuJKKqgigq195Yw4osV1knt+W8kzrMQJnR/ch6WDsVRK29PW3AzgTTYT8lQ6mAqNdUX/SKA4nnKODWgVIHTEj7XtJQhgoBpO1pOm8JV/95T3TYlE6KNiBQIweUXPJZXrEhot7YcVYcewcTItgtWJrscZlsIttmBpsVVNveo6thVpZGQ2sAcuvAptJ2XPopuY8X8mh/bfYglMf+yyOFmi8w2hym9LorikzxVxeEzQ0IYEJM2JJ4l3wNGITeDiuxdH2AHNtpjyH5jy/QfWgHyY3IEIA9NRnSy1MrOiwT2oFKOSZPoeBAm4HBwy1Oog5OSHIMDvrqYtoEybBhI2tnig2mYvK2GctRp45yqFHZCg4DAWnCLIV/BNuADUPr8AS7Do/RI7bokZCgnJNOA/ESRNz58tZNegaA87auzXqYfNw2PAwKfhlvSAYQ7jmvEIOOZYWPnJu6WTfGHyTNVNpEUszJ5NjMOyNmeKeiXz4QpHgqHXM11JlwZLrt5RAmAwjm8DzUXl6XAKLXTQxF/j7xFcs0MpC7DqR0xzItXNski6hZZw0Aona0E2LIEb4DAUDy/DXIqsr7q6ZDuvUIabLpJTk8PPxi6NlsjirCadIiIjpJh40u8UN5oqgihNLtrlAJIe5cN1Fju4o+0zK1gJHQs/2UWRtuHCVKtaD10QpbIuiwZLB7bGga0I3AU42an38JcDw1xDCCLNUEVEKRQKHHAQyLdAnVBHAj7I81Q4XKpsO78gaAToevrnonDk1CnWjR/bMpWKzT3LI5hBF04GYMv+KXuAaGBtKdBK22l+AmBp2kzeVIZzZNHZMgMCrN1+wM198HizTLUlmewlGXaaDGK348xDDUONyaEfXwaR8ngJeCBb0TIlwROcKsZ8nrpmVhuB1QMMWMmvpnGbqy3BEjOYHWoxYIW4qE9H0CVIeiA5Zabxgopk1OOAFjSNOVK/pFsiMkmWIqIAUVhHjNNXm/2q5QYOYi9BaJdlzUHBu8QiD0JArEZ4Sdbdwx6zpC7JJFHZDw9SkkBr31V36zoJp4sMWCRxGzSmC9RMHArCYVQEdd5cGjc6F+iCYEQ6XW9zhVbs11zbaam0XW7ZtOTBtYUEYC0kgXPeVleTTQI1MaB6G0hXBHrvpipkLLAVd1mNHjxhBcJMJF+3QqkB7jzzySKBb2Jhm0kYK2RqH0HRuCAMRIz0T/aAwLkrK5ht9yCILJQZLV5uvIHThBDOd7JGGWpFCKfYwdsSIYotdLQ86Jxnncv88ChzZGChaIYD+y33QAbyk0gyB6bACo1viWpkjNosMGSBfLZwQABFVRJgr5NV5DbRZAxg7xFi6LPZMRmQrUEvJIWDWlF9966uL5BvBhN5mEecepPwqlpc+oJ8ts86Bl0SKBi0ezBAzSk8U5BHCCTOERcLKypjqgVbr2az5i6QZeYBykc31IE88u8gQ0wrWjdCr4GOOYLF7EOsBKPQpwrRmM9AhCaopIIDRxFME4K+L9FllysPRcZf9RQnRIhUkRAV6QoRMUHn4MdOGX0YxBcImPomjEBY2mg9zWRJ06kQrQxjXikvh8SJaUfV8hTKR4I5Dz6GsoIRxwQXg40Kz+gYZOkl6jIIM9eWYLO2+WlSYP33imq+kFBQkkE9DflwBhbGkM9hflh3sLuaHDVUf1OxyCBtp5CJzeggYvmfN0QLCYIJCrRgsLIYb8lQ2lyg0DY1l4pJ3oZ7EDHr0K/hulaWkBDsVjZPK+VCh6ad+hYlVWatwdKxMljQKzqajTU3+Kw+PBZBR4k0y9KTCAybqhGUnfhDDNUs7HTQvdFp+mI6AEZvMiORjZVyBP9ti+dRhY/ENmjhkoRK8P8s0naHAYlYoONXgYI10ZctfGWD0mEdOG+NGPKITWiAbwgyOJiyYVpGPW9t3mAxHNmgcz4bWNArVzAhVpJGKkbTmlq+0kgIyGtRneHf3XmHYHWSAjynQJmsH/WWKfQWX8181VscUNlNYAihsYnMsf4w5M2sdqSDoSqwuCGEqLXmWKooWW3bEKfKV6ahFQwuW3sBLDalw+Ay1z6XLzJSsKJ8v8jLyqrwxGUyWJPq0UIrKXJRcIHUIsNQSQuaCB2LKVQVMh/CzPwyXOj5kjBfkBQQNCEyT6QPTWmmBY5FMmdeoIbsEtMyn1KlZHVDiCqtOfay/9e6iZXMPi80kMqR2zHjkeGFNtCDyK9KV0jPjbOkhD7IJvmKiv5ZObon1wuIo12Dpd5Gc8BkYZ9ctB+RBh677MLPu+htf/TWc1Iy5CF/lLrk6/ASdo0eBSya+zcpZUEHkAFugMUexBuXdRQtEi0FDKuaCV6pFzwiDhgWdYGPrsE+z4I1gmRWEVzasgEg4cFosoITc7OCgW51rS5grDrU5jbP/wQbqQR3JFP4AjzTFHi/ktmRaeWUaqqZnIYRlEebosY8S7mt2ay6k0Ry15XgzzlyOvLtoQSdEl90zHUJiaGLvon7wlyrxB0wzulXHLdvIaEah5RhnCZgrtACLm5UCneYOWxV8eKf8WDtY3AD1K6kmi0FkmGtBvzgkpqk+AsLPrK4LOiEpgtUJhmIcqmBIPvHCroyNydp5zEWCSUMDcfb45ApNnfm/Ap+YcclQxaBJz0VbZDAmInAD1d5QRS/4yUylXRa4oZlscLZF1w0lqoli2AeSwGTBQRjJDuuc2LDVHEida2X6ll0OEl3j8OCF0eHsum55cfhVyVAGFxyginI6zutuKiz61XIp9sYO5OkcMq7If1FAZkdExj3LCTI4ECDqbKOzM/4iW+xgLQZRHVpXZMy8iBCcTQrNAigupZWo1lTWlgG3EyZkY9Zs1jLITIGVi0tpmkMcyDbfm7ppy+bYBgNa0+1CX/VDUCWFvX/ACugv9qGB1otHKHL2Tx0YExSyeKTd19AvV6iAmho2Q6OfRlhZEAxnjI5QpakWX61iDILh1NRQZZ/Rmi4yILpVTWVTiDTTrMrrv/6/ZGKe4YmdYIlO0goMJj3kzAKjbQoBuKlQmmC3oCl1RMfoJM8AFmxQXbYt5MJptttCy58g1hQ4hiDTrlsbwJdDBJMkv4PmMJFUDkk2TnHadRyivdSbcGO5rwhj60O9oyFLoaCOv2mFsxB14i9fig9npiiRkmfTCR9veNT51gSFPI/cS6FdYc44MTy/EEF1LN60CJ2akG/1mSePqKBZfaaEwlNvNUkzqypVxhGX3IGe0NqSHyGfDtkjkQYzzfmmkzQWzeroOXKH+vHKGT2oDEnKQHlwBOacVEOAKE/MqgNPg6bnBJagxK3AxF9srdLPucFfFkrPeotqxoqVRuTMd6ESunIRJswElTNZFTRBRlU8C4nKCMvhaiHZlAU1yZVWUU2HhMcU4FAbskeWEMYxVhF02tGimVEnjKlZJCVIJXs6z4Fqb3kxC2pSk8RN5UgZRA8E29AsCAcadFrp37qiADcEN/EV2SYk6KkJVAQzgpoEmJWeYTkIS/p9VVYt/g7ru2Lu1VEzuosaklW672vVbjSQRlI32lVcBLImEQCQH0uUWYsD/c1WJmVcJoVgUHnViDT2ZQXKy5iCCFAaoh8lkf+KOirjY+YmVMA4/QQC2U8UEofRu03lffIVgzgB4jcRjsQfC5YThxLlZZFYvOG+elaLAu7wS/gKThKR55AWDdl2WQz9Z6Iq6tNEjouyREnT1XJfbS+LwSwQkaqe6ISF5P/xjK0Lcmq1JlF3nRmMHG69tdvLLBKGsr04RUeYzfhqXr761AkyU6J3q6RkhOWPhWTcuJVSlmnko75beqaeDIVbYUL5moyY/nXb1NfK6qNPBQ4A947lrENvp4wYZCBGnzFfpqBOjcGxw8G9tpT7mKC7ZF7W3uxYmzq6hZLTKeOmWx/OAAmHQNWRqC9H4JaZOmTE1LNXDBECmDuRvyC82rQcQk3eC3bwv3nVOslbSxQscNQtbSPwA3kTxBTuQS70Ojeo4azFwiEVCDx5gFWYWbAkMe5iveSyKF2H2a1OrAJauaW3JBgZDvcxyE6ymF3gjyrbEkAe5TWlIw8Qs0TCQbfZ2xIFk7XcS1WgCrW6DRzM0VIChIbLMYQFyJqLANFCuIjN0ChnyrQlYG4lDgTDAgSidPyahiqggd4FAQDRQ5UHdBIV1/HCdZ/QTbxAuesaNn1SLg4e9umcq2PoyoKm8pZftcUvnXDsg8Wu+GiIMKC5VV0+Ia5wmmWw2YB3oEAGf96GjbAzPIcY1MQ5t1YWU1bGWWEhTdGDJg1h4HX4BSX8VXBBAw3GlSLUpPG6iSUR5e8BAc1hdmAlyDcKspvOfQWalci6Q3+Z/Vn8GjYcvWIIJHGZEGBqQIhqaEaM69V5i1uER6YGGTAxO/SzDA57DgWSDGhiLqZpIGu0qYkLdK6Q0Jm4AIFbKHFDHthVlGjCytE17EgXt05BNR4pgnEWI9Ji1DoLlcmnD4cWbSgMAQALqH11y9/oUJhGZiT7RCJIxVz5Glt3IhdkN4Oavs0PTqZWOqEUZkQSajRXm5Ach8ikw6ROOC1uYYRMgeQgo1RrRpno8jzRDAfyQIWHdRa9wnSwfhCQOMMRzQmbhLWcY4hodGjhY4iskqFuoFBwC9/dgsaQYBgyTbaCBIMqS8lx22aRZ1DpKsuQxcuyZSmvuxFNK+In+iaQgjLGxJ5uGv+m5iH52orFlkTgKM+S0bH8ABR3iTjuRj44m5tkBCdxhfypSdSsBK6EIjUVyJY+GR1DSOuK6q1bhsBv+MLRplD2H0xNS4TZYdFsgKjmbtTES0JDE9KCIKwqQypP9jyrQEPoM+3igksTSKYYnQsywU6rWkiePlFojae3cgo2KHIU5sbEYyJk2g4AnUQVOwtYVjuUWX0XLQCGo7fSJbASP1hTiRcFUCC+7toYgYAV2l3KTOCoKPMR1lxbIwY+OkQevqTJc6UuRaq5UuFKshWCBY3PgQA9mGbkjLI+7jBY5iJKHxKA49ZjAzW94T4hSW5mbxMFTZizqEDYDArJOim3wmi6RSpM0IdK+5vdKmcneXGhgkGreNe2Vl+rFHw4yqacvDAoJqbAZBOSw1fWW5wayOvNpPK6gnlFDq5eXKhsbUupqA0RQ5awyQTzOprBNcGmuIU10QS7w7OpVtstaAABMuTHImoKTQWjGMt1HzV9GIdGPlVoriSdvTAPAocddhhlFKhzQ2VmZSSxm3m32vnL1HMU5umHCPEnPPYlzOOxheOirYyqbWfLpySX3jivHAUbeuRKcmHLVMg8Q1s4DEE8mCNB46wm3DtWnbSITm3F00dmk2dpuWGpTFYnJM05r0b1ZnW4i66bJlM8qrPnKtZBYxiTYiGtMpYY2EKVd14tQE4c08XkDj0Nex7tlikgCVLz+iRsAunsavsFzPVQnnPa2VVDg0F5b0IgS7PwTAygCe5bkYd22HLsdAb/3hyty+qMWsgYi+GSCuF865Yp05tuSVGzwCVhIW8Ru3I99Z+3livwce0qO7A52rzBQR0e8zzyYMpSjdI0Q/7qZNitixwwh/Wch5cSsvbxSWRkGsOeRFpf6J2/tFK2Wvojby1X4PHbwZ51TnOUYANhLuiwD/GEZDg0h41ZoA7z4xCd6JkUOYWafQ5p4F6KOefvmfDYlQUaJeWRojk7X65g54z3OIsAfaI5e4aPvAPfWIrHtpO1mxI52MixzDpR0MqxApEkx8xfiwIbUruq9amMnScpb31aIKwOZkeJyM9QNzkGeEHGhjQP4Y1R9Eka1Sdj1p0JXa5UzSpzxixtBGZIgCazaGBFHbdhACUrzcvsTGQ4hNB0gh0VQF6inC8DItrEDtY11A10w25dQa1qnHPTtyLsyG4BGpyEdZhuCEWDg8nK0cTjWmSGp6FtnU6l2UQYNJaHvMFN/S3dPDLm+AlKGGEuMWdDJ7MYHcuQu/I78qSzyKgkzVOmjPImZAMNPFs0oKqhgQQ6kjOEK/pvQMtBOVSOqxN7VyZwi/pSD96RIe6wAI3KWHbrrpMpNEJ8RKobUrPaoSosnLAQVHvFg3QXHpAe6wFl4IOKnyviZsvrzVnRHFohYomFCg/YNRWs/VGHX8hpgI4KNlcPHDggpJGGlxkyhItO9TibkB1GIUeEMtvnr+CcxuZ1YopJKHRLuWm+0Fc90C7Ot4SojICEBaPc7MhNdKi5yZqI10DkwRA4EGIrjWWMEff4mUwN628tpL18Dou3I0/Q07NJKXAX2CPaJWso8SG7weTRCm6iOky2ZCpbjE1OT3G4Hdaww2Bc4CtYvCNyCFJ5SJCnRQnO/IqqplbyIHXWZmEZsKeKHdmnCsEd/qjVuuYLyYl5WbqsuGbX9OarDofrUx1xohzKSQCMUquRNBNn8ti+EJX5Z137mSjP6tB1xoUwcErwoiYdiIEOCVXTrcoQoy84lbfQ71SO3kZdOndjEcr6ixZm0U+K0IxUqGafhuNVzGqS1bKAoQRSfczNiwoCBl1xdEgLnWUNhhWwUlpHhSBg/kHrQL08gQA/QA5UyOS0PHPkE5XxnUPD5s+/hoUPZIuM/82O4TvmeoeO1ID0R+w5ROfkgbeXhnGCvHluxdJDtZ1Em6gvOcIIqCAb7m0mNoFRJeWdTUSYzKlZ5JVdVKCq05aT7iyqPtaO0Qf+G1jm79liEZ4DAeAn1aWh6XO5r/NQQp45sj7TQ9AL65fPdLV614o/Z32Gzn6vFZM7K49W14Xa4aLlaQFoepsHq2gyf82sz8PxaUYcfg0cOEUqi71nBVrDhhNXFqVWV3OKxBI963yeVvPUySlzlfnMQJMC3vJAWbaaLixEgK54KcJIn+luqbkd4+k69S4yJAp96sVZ5flp5kpBjPHhSIjlmjOts/rf8vr8BGRXcON+++SV0cJCPbP88/RpIDgwv+THuuwU4Zw4j1LYXJyTYAo+ZwzF/PJJfJqBpr8iQ/zoM12N4ZVQEG2RT6m3Ldkx3VtzFw1bri9zwjXsef6Vgk2bf3kllj7NcJvwdeGEhc0Q0bLQXeAd5wIYShtTIo1cHaEvXnIxV2sZRO6p9Vsczo9UQXCiQoZnZEW31Eb2ndeouTNanMjghyGMK6DVcBQ11SibYMaCV6XNxp2zwfxsLulow9GLOZHmruBQslOmQPZExldmYf6dNxSaGm8YhVXrHFiS+7DJg0LPL5FsORd7CzG0pAOgzIi08cKdv0Bb/FoSYhwukjbzykkZCuh5cSMA7Wawvz6OY9hfciQEto5aMQ2xUZ+jyzrZV8Q4T+HOL/cNJtwszBJDuo6zjn7IMmAr+5I1XWcycB8B/iYBvsm9zIQAAEAASURBVDpJSDFMGZIKRMJ8I6USvUUYn10tVLAawVOeS4LJshRt2SZXbErIkrDsRlmoz4nKs8SmNjGcGAlVwEdeyqo1AxS4LPHUmJWo5lwPbHP/2VeMti0mNWsWhsAFUwsa6JqdwFSuJED/UY5Zz9KmrN8UtKLysmNEkRYIMKIC7Xa0b/7ekBH6KPcnAZe4heJL5RAS3FGNvgieY4LGktUiM7RDBRxsyNv+VxMMI5NAgTRQDSJV8NVAWWH7gx6qHrx6dmJoXPCRFWJ46aDNH7ZltL7HU0evx0UBv0+tgJuS3WAk86wWiTo3ljlvtRjqk17n+GrDpizxUa/wt3ziisTHorkP5tEJAg4cxZF9I2CoMuUUzjrWhpdpohXTQUhOGD3igYV93kCyLaOObABZHsTaOr8N2cC5bIckFpVx04Mt6DTy2+lwl7bNwwKyFc3rD3bpjFZNtiVJ7E2PGCuOLn1f9Yh7oH92nldsAeIWesJ935odvroTFv5SN48V7AHOLjcFkaMYik/OheCR7gHvbjkcNr/VwahyTlrtWvM4RZUiFvGSzWoZAXE1HvNuw5vnfzCgAjDWM+rY53cgUAgtLiUZKjAWYi3BG1fY+SUnh4mLozhcK/2rYOmyh6y5PKi9Pu6XgJZgxRANtUa3L2HjTk3PS8unqOAdLYJ5EY5um/qjX3XiE5kUIeWwjouCJecaTBkOfIvGyR42ySvCTlSZhcNdjrpJ5fAp4eZ3H0yWB2/WIlV4cuBUcFcQ6OgKVO2um7icgsBb1OqgRDwbEr615mAEjltAhrk3a5iIMNJhVLZYhOmYE49QcgTmzjq6Ir6Vy5DvcF5j6WyFoWVbMNeREBMEuDfxIsa5GBO3lMb0FaTePSvueLYUibOyggEzNTv0MBDAtHJw1OyIEhvHnFwRkyuPsjtRnS7AhBX2DI4HvWRJHHS0UDmT4jWr0lvyTehPIqe7mrhrFCDzODFOnDNR0y3TwQuSAChz95oAfgY2OSbjK14Me5D0tW1iFh6Eow4SVTgLGXqBp+7qAQ1e22NGMiDIEOkRmFyG3TVT0sKz0QNJi1Sj9FD0ME1zvatPKkCQPFsk+QhSxDsZJAfk5EitOVHWiYVBJ96HJyqWTaNHerDFTW5NFvfl3Z1msr2vgjNTpsDghDyoACWx7sQQy92yeBvCuRtn7aCKWaYpjYhfsZxLzzk4LbhVockrLTfihrdiGVZ0voBAnrvzscXWx5rxIYcSJT5rHncHh6PduMbQOdjC1llKbNrHm4x2cJSd6sqSau1j0yzf+0GhZuFmPbIuM8iMG/szq9qev84zsSbyZJhcZnbPz3dHJki7bflY8XMLYUe63cOdMJIW9PBL+WN7eKbTU7NSCCUoGvd7NOSZbr5n7vKHyQMn00okIN0z89p7E1k4YYGjdmw4Q9YV26SiIEcGHEWzOyrAED4JP8DEIgicmFHHCsTGzh0J0e3kux4hqIKAnN9vqdaJSFvs5HEjQuN0gGNjXiasuSFEtmIzfrNoQcQro+ERKRuhQvoabWruF0MkPpzL0IOgSIQj2vccNScASSpromHlYvQTJIm0uap2ff1KolZGcV2TuKuVPs3d8QoZFqFafe9g7TPHqukMbYWjojKRqq08caM0BApdt1UOHKPQGa/M8dietIu7MjumT39g67qDFZ6R8fSj52UkPsSHYjZ5YhGdhYq58UYZ6Q+P7ArIaaDoyw4bS4RmXz1XLF4VgNm1ljYSZ2IQbiJGrgEOfNw6WbMYglwBUdZEz2YksORu6l8TAxk0QFDBR00hKIFBj6jbu1f50BJJ/DO7avIX7popwE3ND/xgvStkRidCUz0ojH7cSjHA3/o16ttzsEVvUO4gqVAZ5m55HC72YGNGyM7+Q07qoFGnXsnKCmReOsY7or0wySi4PCQj+9QVtPHRGwHF59I9GEf+TZY46WEY9gvtCIawmfCH0kn2QVJSPH7lBNo+EhYESZgtnUGJqBURMi4K6aDrdvDwGoWO8xiLCFEWZzEIDCFUOUBIUuscka1CIMCVpGhyQJ7Noy+0WxPJC0qhn9oqywGgv3kFAV4cgNceEWI3EAwBak7vIr0o0HLYhNg7JURoiRnpIrSmLMOlnyGdo1fQ7ONWDl0LbqX8uE4mMYXIgSgSFl7lIMNIGrFABTpF/UXanr3az/FVxbCXNwoB64UVkBtK3Yi91PAm79gzd1Zn6cu6Vm4Unushhs1xXpI52uc4iKDsdlhDZa7Xg/xuH8Waa30PZ9Uyutunsx76+VROcIspoLefJY21ke0SQQABJusBfwNHMX0eqYUSCPsZhw1kTUPS9wrOm0v5dTTTL9yi5w4R+TgqLD0pQBWAye+6InLzEQtx8YVPeC8GYEbtnwjG4gkREY5dSgGVd+RqJfritViiVHB2wOixreeWdIMhHBmQ1/Dx8IIhOGRyEzoRKIqdZBmCYGNRPHcd7pDjUBNtUiRo06E6OnRqg1yK7tJI2RintLZzbU0rSPBz8hRE8noTQck+Ij6zj0j1W19iQmGwDe3EqimI/dAgK6FtwihHI80hEHKIQ+glAmQ0oSQ6AhGSRH36R6QpmJ3HxcWEkgvqi44QiSShPqocWtaDylw9uEWCRnPZHDNy1+g45VClt9TGIxg8VyE6wvTmrghQagkLoBHEC5s1F+EHpHAAsiFMIbccDW06AZdElToiTKMLVk0HARZOgJupPvHLRFgBQ5igbhHAJ9MJAkiI0NQEhaZBAMyRavoo1LOAHPs8HgJGDYfBsDqkiyB5TWDkNTSMZ4B9jT5Rqy0wUauy6RtFJCzgxGV1DIckVjtWL1dIjotaSaZEJ64QRbPwScmJW/6arAhW3GuOpIsMOyuEa/JEuUdE9sxah0SXoOIFSdBETR/yKeWEU+Qhu60FWKmPoQjzgQnZwPd4osRkscAsNIESIgkVrTEK3rmrOalTARpoQKGvRocAOnET74Q3CAa1akhSx0mK4KNuCZXrahpIK7NQ00RMmVJLPRhFMk7sMToFc0eY/kMUdQhGNclVaCt4EeycDo4H73ROMKiz+aLHX4z2hjw5F9zUA5qxWx2cQoYrgSfKU+nQbGgokaXoVrX8kB9KBExKBCvXSayBSALDEkaDCmCi5i6qQBLUIdKGoEHZ1URB/Ym7/VZHYFEEckEZbUhxmHGrMGvsQ2tCO0Yrb8LFiBmG5n0TaFsnDR2HRNvq0OUh0ZinQOuHnsk8DfdzHaD57GcEYu5d3QIHwtDNztrUYTnH+LtH2WeROLGFKLwRc2JwOPp6cEXUITQSzNsHFqF54kAQoppbqqVpsK9um1SMZ+tSDCZh4ZYIqpGV4RACDOGEOGHaAxPJCDM057fNGVRUBIwCSk5hQ0/UEdULyE3Ka+Qy0q7N5ynLwqAwZj2cixALehDLW4BVGbbRuahJoIVO6A1xUxl57orQ3B3Sg+Oi9whih3eXu4JmoBkusgDTnaiMj7MIwD4BqrsRl053Nf9dkMIcpFUU52++ZU2Ao3w6lhh2IuTGL1khsjq8O7xiCBG++j7Du7oStM/CTbImchbZEMvwa1FHx+EOZ3MkLCJdojfy7G3Mzph44XOcZsohtiwgmLiqVgW+tkJz2pBMoNQKG17Grw2nsJO3uxCYWJd310Q6tR2BjkBHoCPQEegI7DcElnOMF34kJGAVPzuMUCF2pdnDFGmoIA6p1Wo5KjT9ZIXhEDIIzRBZuRZix7teWahslNE0B3wFhN5e4ey6h+ptXi3Uba2sfzvb9UotCzibmDM2e7OOYFUmKL82BZWb+k0FO8Y+zcVtfm0Inu7t3Pl9d5N89IN9TkmM3trORRkQm43b6WG6LbFZNFuhQ9v7PtM917vAmVCoab5LTDS5iSUIRszZZ5/t902ca/D8kRMQ0meeVfGMGHjjGEIleMuyFNI0u6VUJDe37KdX6Ah0BDoCHYGOQEegI9AR6Ah0BPYeAksmLCaAsNUsE+GjMFrNdduqKoze3diLr3rVq5wZ8ViBiNHjprtxs3djse2E7SIEPD7jaQ7vi/UkiEelZPHiVSwe6JhOPeyiOXZSOwIdgY5AR6Aj0BHoCHQEOgIdgU1AYOcTFvb/PfLt7LoHFkZn6JSEc+O22fORh9Fqm3bR9jXKHazwK32ext808jo9HYH1IOBJED++402r3gXrJZSOaXjjg3dSOnbkVNR6aOijdAQ6Ah2BjkBHoCPQEegIdAQ6AvsBgSXfYTEBTTzMr4IzCKOvgcgKy51Inxh6pbc88O/0uycLRh8YWenQvfOOwAYi4NUSNMIjG95dsrt0eZ1gLveo3jop7GPtLgT6Oyx2F786tR2BjkBHoCPQEegIJALLOcY7f8Jiy4f5t6yQU9qogpCsR2UbxZFOzKFFYOJtGoeWsD56R6Aj0BHoCHQEOgIdgY5AR6AjsDcQ6Ee49wYf+yw6Ah2BjkBHoCPQEegIdAQ6Ah2BjkBHoCOwpxDY+RMWewqePpmOQEegI9AR6AjsKgTyjdejT2XGVPzyt1dNfe1rX/vIRz7ymc985qpXveq1r33tifpf/epX3/Wud33gAx/wmqqrX/3qV7nKVUbPWBnaLyj75Wzv4n3ve9/ryVCv4x2tuTpEEfDFL37R6J/+9Kf9irYf1fLaqStf+cqzXpuFWvNS309fX/ayl1V51q+A+UHx973vfZ/4xCe8vud85zufNxBf61rXGv7qlg4/9KEPGbrBEzjQu/SlL73Sn6xKYLEYf3Htwx/+MGK8FBmXDzvssFnvF4uG3iz+qU99yiuKPvvZz3o/+nWuc52b3exm+RNUpqDPj3/8437Nus4Othe72MUufvGL5+hR0ANevPOd7wSanzO/6EUveo1rXAMv1vloLRw+97nPYfEnP/lJOPhxK5O64hWvOPrqdA//mj6CNfFu+Ete8pJYjGXNT7brkwzoUJ2Kg6eGL3GJS0z8jhsAyYaXuPst85vc5CYQq82B9s1vfpPc+snzet0vfF3oQhcaktGgvYNf8feDH/wg4+BXzHVraG+qmpgXNN797nd/9KMfBVQYk9GH1+gmufLSbiB7pNSkrn/961/hCldozi9D6Utf+hKZIT8Vh5ggSdZkljrvIAi1q29961uvfOUrmbXrXve6lIgi17vKaGZASA7+UiI/AHelK13J7IY/Wq8aDWpYHD0AjQlqDCbQSOOb3vQmvFD2o/JsFAFufvetoWdnv2IWdrznPe/5whe+YFxvXgfCLDuZQ1tZnvvc51L2G9zgBpaMvJ4FoNEgUBC2j33sYwTs8MMPb4QhKxMGGvfmN7+ZSSFmFM0L1FDSSIgOEQkrhWxrILoJ27W9G96IrITX0qOZSCDmVre6FeOTJDUF5pH6+MU9T1tf5jKXMTUTbOrs8687/w6LfQ5on35HoCPQEUgElntUL5v3QkegQWA0DMg6EW5xE7lKHCbOGad5+LPTwjbOt6jJr3RzpHhyt7/97R/0oAeNesC64qY/9rGPFWaooFvO4g1veMPjjjuu+X1uzjTn7DnPec5ZZ53FB+Vf+qljDS91qUslhasuiCv80DIv+Rvf+AY6EQwTOQV+8N3vfvdh8KD+s5/9bDQj3muDocGpPf744wXV9S3C5sKVVFMkzz8WLEUoJXfzwAc+sP6iM7je9ra3PeQhD/n6179ePWllHUoWPOABD7jjHe+4ahxMx6+wP+UpT/n85z9vXMG5/JRIwCvPESxQHBIgRn3HO97x1Kc+VcAsxjBH9a93vevd6173Si//3//935/85Cc/4xnP0Jwk1E7EZg972MPkcfIi5J/3vOc961nPEoTrzccVAnyLW9zifve73zDRkw13sPDtb3/7DW94wxOe8ATJJpMChWka+ja3uc097nGPhgZCC7GXvexl7DbEyA+C/RiWn8S6853vjP4kTMz5+Mc//oUvfGFoRF7HZWmIxzzmMbVy3lUgFTTiJS95CUjvfe973+lOd6pKh2sQ05x0EaRsqCxEP/3007cMEbPJ0gVjkRka9OpXvxpWQHMFDhJSuEbxq14YhRjIQTz4wQ8WbrmlsrmLzY4++mjQVTIEb6997WvhJp4Hb8gD63TrW9/6qKOOqrzAiDPOOINWRv/ZCawM4VfVDxw44P3feX3VBXwhRSeeeKKoUmKXnF/wghesg5q1tCDOvv/970ckxWFJXBTV03dpr6wMLorJ2GKxbvM6ydFQt8cee+xNb3rTvC5TwFY//elPZ9BYD9VcwZR73vOeZDIziVl/xwtmYZmgxW984xuJAca5wphc5CIXOeGEEybS3EzrE5/4RDqiCYvH7ChU8kiXDAhJk72S5IWMTOLDH/7wakOyvjXrBS94gd9qxALZIpXh4AVqxxxzDHtSe/7yl7/8yEc+khFGJ4QhphNlTAGaVWANoCEPaM985jMluEm7r+CiI9e85jVzRrVgdnCwvsAEwepbU+573/sCpFG32mr3lpdzjPsJi93L8U55R6Aj0BHoCHQEDiJgn5OP+Na3vpVLJ9ziKPMpHQQ4WOPcElfSPpW/dry5SrwHHlJTJ79ylAUPwnURy41udCOe5Vve8hY+t0hD59VT5M6K5+3KcqxtMNoH0+1EzznEThW4p69//etF1IgU1dgbRwafGPFCRNmKu971rmDJ4YTforIzzzyTC8vzdvDBBin6YSjjUNMQQrhHP/rRAjPbm7ZYbYyL6sUwInwROE80N0V5xmJjkNpM8wl3OcIM26RiEumhJGB1BQS89KUv5btf7nKXk4LBO/EkJ55smKagqDIOGYLJF7/4xU972tM0JDZ2RG2qCzhFUM2JDLEKntoLreEor9pWZxMJOIvxmte8Rs82V5EhS4IA7JBRgsxd7nKX1U0/esYL8xX/C4BloCRrRMWyaaSXPIiLhHwZD5iUxBy9EEgThstf/vI4+7rXvU4g6lexhMeChySYpAktfAUsGYvrehAUTWx9i1FN3xDEQOUar2bP6kBYKlBGI6rFLewYZh6z1Q4WYCVpInbCeukq1kNkaHvfHjjNwjiMrsOJx1R214YwhFU2QTG2n9UTq1d1c2gC8qyEUzbkwRyF93qWISIbjmJlt2RGt9gXXFCIWzJfNs+xTOdZeQ0FlL/85S8XKuMIruFdM6hbZBsI2OQjRcsUy84430Q8GJMkWCJDtouWsb2EKqcGFnG7zrOmIdwlrsyvJmyvQy6EkzXTs2wOBRSrh4Vp6NnBr5YJaQL6wsShQeKMdaUXTL3kJillJ0dpcKaJNTaFWaIONHUYVT2T7a985Stq+gyJpxQss6SJW7e97W2F/WCUQCFpaICDK1WR6aavF77whfUcCOuW4WW3G7s3HGtHriDPvOKMoSSjpTBwGO2cvpuILDDrcctb3pJesBJkSfKUkMh0jLbahxcPrtz7cPJ9yh2BjkBHoCPQEdgzCPCKuLw8M9u8PEuuz+ixUiHrySefzGnmbjpnIT4ZdRPBojfnNTjNmtgQ5k65whEUBPLGzjnnnPoUgHFtswtp+Oh2tk855RR+25qxFeoY0camJEK4etIWwgwuvujIr5Kf//znT5Jsd0u+iKlsCAuu7Fs6a33SSSeJHOyMgS4dcT6lD9fTpESzeoAwRxkOEgFO/Irwo9twlD1Gwbl3/iLHcqBamoADXRHLuztekLG63e1uh0jUXuACF9A/ejBIFkNYLpqqe/W4L3KwHyjaFALZ7sbiWSSpLLo48sgjHVpJfGpcmg3tf9pZFWJFpsB155wf+tCHij0c/xb21NgsW+1gAalyUqIXuQYCH3vygnBCgu+iAhFgpl3Mxazvdre70Royg2yUCM5xXKbp7LPPrgkLt+ialId9Y8KWNJO0xCQvZkHcIkEGPQ0pSF6vBTSLqQgkSgikr+5Od1ubb79MZ4mBLJUTKBI6gih9yi/Y70W/aLlJWAhcaZbsBigwGsGiLL997kAWWapiBmoyI+Akk5EFk/uTH8EI6uZWBpMyX1IVzIj983oqSnQqvah/erT9mc7ZA4snGUF/zYXkRADctMUpMTOqSFc8OKMV62qr39MfQvHMfmIlOWSIsJiYZT+00lEmObJqsekI2yLxR8bIYRw9kIo1nCSCKJcAU+rsZBUFyQKzJrROA93nPvcJvTCd0047jV5YBeRwh+rvuQYpHvTgI3M6Shj+slGymQwUK+p8Skj7sDIhsQYRyxvf+May5PE8jjwskCW82BOdNDgQNgeCGL1Yg2gl5Ic9r+gKlK52tavhPhNn4bAYgXHWWNJw8qroJBXMI43DbssQkZAttZ4O4Z3V1d6+3hMWe5u/fXYdgY5AR6AjsI8Q4PPxloQEgtVZ0+bv8vbc5UVxhma5iSrwFDnrtsK4UJxjV7h9wk5xCw+SOyUpEC6sW5xCbqKPMjfd3zV/0OY0te1N+97CzhhdFCGWsLXrNRymkwkLzq5gwKPO4gd+LUzU1xZuniAQwEs6ZFykQwfy7c/bPo1uBVe8ZL05TyHxkTOVsJCnsC+dsLglbAaXfVowridhweutB8vRwHX2fJD8lL3cOB2QNNu/Ff+YCBw4yvVwftapBYw2uzrBejfLoi/RaX5VEHwKYEDBiRd+rDphgRdCYvzFvsjaoMGguIAGW8ciyRDXIJLMNOc+BJ/CVJulkQirc1GGA5znDCfkBx0tcTDH41f0Tuao6S2/6laf4F1niJWjSzPJRt385jd3JiUzCKJoH6ZAzoLiJGHOZ0HSQZ473OEOXl0RmAjazc6hJFmhmrDAfd3mQArGog7yHSJzAVsOJ5SVK1EhB1J25oLZoac1zq+9raiMZS960YucAfHoirM2o9YS5QJUn6QB5U4qsQ94zX7mdTLJfjpjUqemztvf/nZq6ImbyEpEfTrigJspMzuwiotyPay3nA4BVqEJ1HOgnSqgRyZFZsGgqfLocZLImSxcxrhGBUzH8QeZLPlrmW7PCY4SAwHLh4+7QB4FNhqaJlVVnxBGtsJ12CLJQBI6RmxwgHOIU0PbKCWruEjarTt6np4abZKYsBLJluJ+5ActQ6y3p2OkY0hLtVGrIHW39NkTFruFU53OjkBHoCPQEegIzIWAgNBOIKdtujZvacJN1JanKKTnRdlGS4+QC8thtS8qAhf6phdbxxrdh6wVVlTmH/vUzkEhT+EK+iup/GwnRKQSuIMZVqkTMzU1wVgmLHjJ9bhE9C/KEoroM7zMOmgdyHW5AK8kDNwyKqv111AGghDCrG382g/PEcmA7U27oC7aEpetgJjYwCfrDAv4bmNQnxATSompputHD0IyZyv0L9hIbIed79QVkb88RaYqolsIiPT8xYgU6VkjCpOcMJLjIBXDOnRHIiNxwF84GHRY0xUTlzUTcckKOSo/oXdugQhWOlfWrRh1HnhHx130ogAvjwNkW+ymDogxwWpVXJQHdFHo6G/UR62IC24O8mQPowWMEM6ZmhGzedRs5sueiOtkRmw411dCjHa7gxfpOK6ZprNCMl+UZc7OpQURTPGZSjTXViSkmZ2MJ92EgBxoDbAhSSvJKhkjDJHgE5zD3EWKnNF77X9ny0wZoW36ZPck4JCKgKHAY71nRsitUzPEfkLUo9stlyHZGRh6SsLBDZUDPWsTHJTxZWhUDUpo4a8J3MJGDUlt5rWKr9NLITkh1fRdwsLRoSAAsMoWMiuUo1g9YfHfsKyCPb3PjkBHoCPQEegIdAR2OwLcKY4pr7RGfb7y/3jM4lWe1obP0Z6w+JCrai9XnJzU8iPFS/467ZwvX1DNV5tjpiaXkZWHBX6w7S+OuyMDW0ZQXsAmehH0iuuGXa30Cv/eXDz574S2M+R8X+cs7GDnoBAQWArM7CHjpmPMkjXKEjQOnw8jIhCJpb068VGPepSQgG8tlrD57Ih77Tb7VxBigVoYY4Padrpo1qM3TcxW66+0LMjx8hGU29oVJIyOReztbHsKwJsCyI8wEhRNTXG7MNJBfQpCF0xHXOdFDLZJHS1pKot4bUeTKNkK2TH1mwr5Vbe44CktZ16EZK7TNY9iOZdR00xZfw0FEuIYBRmmPnCoUZ8oWkAlpiVXyVAFZ1VcRD8FEXU3RJIH6kMjnPcR0MKNPNQ8SFPfVxwRr+rQOY4tTwANmy93xcQ9q+JciaQDxlGiLfvRBK8plFZmJ2h3ymCWXkRvQmtZGxlDApmZ07gl0vYAjr96YzqcmwM+XuiZyXIEZpgq3ZLC7VdgUtAAGbNjTJrkLEsiW+GEnYfsWDzJ0O2PyCYbSLfOU+AFfSRCMKHIZNLDj8OEhVSjV4dQJUpHIJ2xcnjKsYUmL7Z92rbZg4kwp2Qg1p3sjcyAl9lkXvLiPi/0Exb7XAD69DsCHYGOQEegIzCOAG+JR8UtrlGH0IKD6C93yt3xlptxVUgpUBQUicCdVK+z4Hbbf+MpSk9UYk1NMDCdsBCWcJ29jwAyDqj7FbraQ1MWa3nSm9/MaY7n25sKK/0qMvS6UK+g56nbkj3iiCP8QEYdEQ5QQqTdPD9egKcQQK1T/V6jwMsXL9X6EHPXxEEqMudtO4PjXR72CYUoo8Gk+E3wADHpDwh44qB5H0Ttf6VlbPU+SI94CA49+zNMx8ToBMYrGwSoQBNDOhLfHDog/HAQjZuvrAe50rNNclG9SMmj/jWSjLjXWzDEWtIZGk7M0V1RlkSA/VUCI7GCDO9u0LPkCMwn2q7ollj6+c9/PsHwBoHmcYxIWAgIM+WHBuAAxEX5BeFrVbqgkDx4OQVAIttFzDwiMU08VOWPnIgZRsjTDbdz17MGnuJx/MEvIokePf6wZW8Mpl/08JpMTKc4fpaCxg3D6doPlET18mhyUsPUhryhl4N4/+Kpp54qhwUxGTQ5AqDJoYC6drWeMkZ4RobxlKaUP6o0kF7PCUoQ0y8vNCEV09I+J8Hmy2JghNe7MjKOVIAXDnJ5fsFnmO0yKBtFeeVSyQxS0ez1EMTVSRkYzjnuGqpFwoIRZjGq0UA86+QxKPmvNZCxK4aYYtuGOyK7At9OZEegI9AR6Ah0BHYpAuJYvpTYw6dOIbwr0ZS79fpGlREv6vYbBJw/Dzs0z3Rwavmv/jbhhJnGnqG4cXQ6moi1vLJevCpm8Ka06rIPm4j0PKIserETOF1z2Hb7V3DKiQYPQovSRY8OONj2tDeb+6I8e0kH/l4csnBQQmymmpcmClOVhSVJNnDs9Lrir/d02EgXTqsmRHF8w0BNNiToF7eYu1jOprrA3k8nCLy9x3H7s1uoB+yWY5LAwnEvKBn+ek72huA4hwI04Hi/ABzEYLWCZ/hJiM1eU3NXEO43VtT0wyh2xWXHsrJg2ztfhViwFWIRy7hltzyBzSvOATlP4UA4HgnMnF/QIWGT8xI8S52sOdxy3MbvF9hRx3HvlWiye9QfCCaS4mQi8dVfB0lGlYhMxps7pQBM0MNl0lj6T8SaAo2TNLFpDxzI6LmpsIqvKKcCJk5OcLlyqpaboXFHhstLUkiOaFP07r0bgm0mqKmZX4mHVBf7IJ81rEZWKYtzBPKJMoOGpqqSWaAYHuTJPldXkCYgD17xI4XnxSVNhkXqk6jTcUeNkF1PEjUryKIUyjuYtWMIhvCyT811DgFoNw92QZKpd4sKy6dowuw4KsXsWA4IHs1djwjNM0dmwTJKwuFT5SqWIfoVdzeH4HkmtaI6UwmLTXZEVgRH77Yj0BHoCGwfAauLFWj7/fQeOgKHFgHOHxeczySsrZT4Ku7iC9ZApVY45GXhtwcQnvSkJ6HQ++1txDXBAI9QnElVhUyVWvGA2bne+MFRh18kAokDBXab73//+3Oja/OmrL7tU16+3XIhaHN3DV/xyB6vlx0KisTqHmORYrBbK4URo9vgxV9lu5HewO8IgLKz014y6ul9kxWt5aMTwifb7D7pW4vAPapgmnoWxsjgDHfUnezwCym4IPzzsIOHU+wno6E5trBSNMiDxIqtb3Lr927Iw4ToCh39tK3QyLFz29r2zG3Seh1pvneDLEnN2BJPmt068cQTgSnXIwJ3ej8yC+JeR0v8kIH6LqofkQkBI2Z4IeTLLABU8aU+L0NEjz766BBmaTJ5lnUe0hEZevBHFoYAOGVAEnK+UaAjTISUnInnLTGYr/66OxQG1YSyXijo7I8chBfc2q4XtD/iEY9IMcuuoqB/c6enNu0B0txd0VdHWsS31AeXg0Eh8+blcSHRMn3BxGZ08/XiBo+ByMW84hWv8GugcS6DXjQ14yvF8U5KJsKTZc3zICrwIvxwsnNPkn1yVaaPBqkrGuR3WAAidUicRntexUWPrpAHwkxznZFBcx2FqHtTD5XxskkJYoShH8E+pinb4rkh0j4ErXYyWqazUqIHDhwA+/HHHy8NwUobCMLOTbhCsxIHQ7B4Bs2BKJRHGpEnf4RCB+KaJPXooOu5yEqQMdQiz+zCaBjalNkHNkrmJSeyHpI2dpSphMXGEt0J6wh0BDoCHYGOQEdg1Qg4lcpnciqVx5xjcRYFJJxRruHmeH5JngJqI1thL5dP7xmEemQ9avIRBdvKttDNJZ1C0bujE5zIYcKCQyl+EMkLZmyiOqpdd90rAVkGlGfvuZ42kNcWa+XoUTA1nEIwVjrrITgUI2XCAjI+IgrHJfJnDvj3toUdmrBL7CR2jSTh1vSvc7vQfplPYAn50RhVq//P3p1H23cU9QJfD0ScB1RQBEwUUEEUURAEJIZJAkGZowQICAEyAJExCAECCyJJiAnTYkgACfM8GEg0BkFAAYGnojgPqCCoqDi85fg++RUWTffe+5x7pnvuvX3+uLdP7+7q6m9XV1dVd++j+yId/D2bzzxhe+YbC1hw7ciDixVGkDw84AEPGLsMkl3jOQCE32W7WEXulkHPgIVi6SBlFR10bIRTRKJ87Ip7BBMv7wCLG/j2eOUQNvw47uHchJAQ4XTyIom08Bo18DpngROu8sYCFoZJYI7AC8n5pVteaM6R5NYc4VBB1ZTJTEMswkKixgIWSuomfHjgQlcEUkSPM1yKWVKTcMoDqiIjjvCY0eWjNaWNkUbtzOuy3+/kpcuhGQyBq09+8JXPLNPEGWQAJpx5DGMbjBHIGyxJPOgHWImRtfqBnJiwGhWoEreKuAl/G3pCbzx2+TMlebDdBTId8RBmcurEIRfREz/kXMmDQReBItgCdnHSCmghCe5hibO4X+bXRtqJM5MZCxCa0HBwQ9Ox6NAeViJBJdPKkYoSh7YJMTJnUjBvWInr9ixbZre1BsPWCIsFyQk0fIUkLTR4yW4mYvuyQA9Y7Mth7Z3qCHQEOgIdgY7AsghwD/iu9oHtE7I+w0JlOLLa2VL8t+UtP76c4/T+Is5kb7cZd9oH7MVeOoJuLHMIcwe7JMVGDP6V55brpqd8LRfXba3zPCtvhFPBJ+el6LuzErbT25fnl/QjDTrRASap3enWjC7Lc3EVtrEGWFuRY85bWWWnaZ4nK5/7xIvQ0/CNHRZgJePN1/QGpcN0ZjfH+YuJtuDso0Amxgoja3xR5qeN3c02HIRNu1giD65FBJ9jNGfms/vPP/98t9+NIH+J7204ZtaKAmQgDuojQkRn1sJqQGGyRGE5HFcSyE0yxDI9spsKf8CaPoPCWTUUZJN49RQpAswT00EEIRaRuKrYjr4SRXv4vETnCLjKbqlovaUgOAVMQqu8ToU24Eby0n010ClRbd3IEYNAwaBzywfLoCOWQSRMuulJAWHhD/E1OPADTc+Q4UGyMzNRMDQRvoxwDPoo++uRMZ3ZNQEvWoUP7yxJKs+qXQx7e6WGcIts9RQmImVmqNf6ppzwzGknUULRK7Ge9vdrtIWsT7BqBEO5VcR39NWAes8uh99JMfLgxFbIeUlEDt4wRgBS1KXxQ0LID7EclKKSyGCarhDfhLmgQ644GhIVive2GqAyYDFIJLTTGAPETEQylFK8mKbS/4M0l8806DFbLTqWnpBYiBFjM1p0clCGFYAwhs19QXN6cqxfOAQ+ahZZxQjDYEA5OwJJ7TpQpmkCnGhngV1M9IDFLoLfm+4IdAQ6Ah2BjsCuIcA3Zuiw5PwddKf5EnZ3ncfmMLCA43cK2FXOMLN7OBtjZmJSy8RgJ9lb3vRuD5NpzjbiT4oItKbwYN3BTBanvXRvE7C7a+PaueXwK3h0muDLpZuh7+4zMwcFIDgVYdOrrmsYYBmX2+n4vOSSS7y9kuXnJogXv0W0gnln45FhN+gicm9cxIijBFyOiX4xlx1v9mZKncKSN+o5gT9RfrDvZSZHy35dOjnxCAKcHCOiiTRw4QCWcBr5PxwShbk6YGEW8wp8SsptGmj2gUHEIC73Azn53BWUyyoAFC5RrOItymjX1RJHV1TkMDiN/7M/+7M5ZCWdOdMGyO6uaIVe2+B1GST8EDgIQDDKk7jOYgwspUGPH5v/mOEsVR1pGRCFMdyGUtdSHiRc9TeJojz6aDouYcP5qKOOshEdb3NoqWWO1sGrIwaCpGV+JvjDZ511ltsHKOuR33lxQn4Z4SHS55xzDg45ww9/+MPjOgNh5iCZVnyebNocMVNMYccEnEYhAB4ZYm62jnu7R5aUIA98p2rciZn8cHTLwpnWOy69r2Zc0M9HVYJecqfJfjtRBJQoVXVnoSo/8RV6mHdLBW/SPgbOgQsvxCEexx9/vLNIpWYz6CHVZlOSFYXBPAFzlgSFzM+ESUrzcA69VWFQDDShuu4Y/ayFlKkNSYmShyyAExclXEQyZBAzg4455ph8ukDCeaizzz7bxBQoEa2I97PgSr7ZJAwavaNVyLMDIB5pJUTd/RFvtfBSVdc0xl4eoRfREXRKAJNVpAIHvc5MCT01OzwKBspHVdriRSZxK+bVBoYUNriUg7iMp6aPJclBkorIYl91DXs+0ceKiGiUGWRSCPlZKXJZEebWO3qjmi9RXUzBGmelQ9MxJYtFVKyI+0oniLMbPt0nh0RXBH8QZIVJO5rPfvazrRQIuvA4dpWpbWgDOV+YWhtorDfREegIdAQ6Ah2BjsDuIsCQZSVz2Bi+PHlf/WUhsfx4IBwz1lVwyDpna/KlOSTePuDnD5gyEgw7p3BtPlcdYfEgxazk2zDiWa7spDA3vcgA/ao8m0wBHq9H9t69wDKbrkrO81WLvBQn7fWLr8XidP1e75j7jDZbTF5pkT9BqiFpL2Zj2bPSsMfZ40n66oCDI9/h2WqXKytkI1qhU7azeDK8LPYlymBxMJsJ6J0ILYc8NxUdFnCJugx/tCU5Ni4OsJVxpQlXJ5bBAf56ZO/ReQrDxBfi6zqd7s1zfAyjxvFIHhivroco6UX6fozAyyYcn3YR4MILLzR8jOk03OHAc3ZPRNwKCMIcIFLr5S9/eYDmFEkGsHjv5IT3yIHh3YHaI8Ph8IvhUN0necgESbCdHiY+x9irNFqZycIzExxCJ8btDBNLXTa+toh1iuTzvsietwPki0UMqLgGXx1j/AQd118v6YQDPJnvIIoWjbujByRK12CLrFgbZwN6nHzoGe50CSSIok/UJQycDcIgn5gZ60RMAXPBmzX5MEbNI6MmhEQmvXxEJngHt8rtzRoXBEUTXPzR02WEB3uiFRqlB8wOpLw+AG+mj1cnAMfJi+TZ6BhcLzoBiJEVaIOtt34gogtwiF77i0k/VeMlJgEvMPXI+z5cbaCLSOBgcMFgmXQmEV/LpapBVzOb0KjhIzzYu+1tb5uYZ4EdJYDPcc0q1Bq5NdBCV4amjEFQOyaFyWV0XJwhFRIivOYgN5g/LzPplAmYkEPiZHbkLCsLCPoACv7uE+k+19RTYy04RaRVQbwsH2lktW7gTE/yUI5CW3hmjnEXRBauRQ0PuA15oAPJA2XiKcFDhwTSCT5B06wxIuaFr7xu3KbYRAHzS0zH6CuJGsq+mv6wte74i2CUhINgh+CO+QheYimfbrEwGW5fDUqUNL+8pYJcmb8mgvAEHD784Q+b2uYmMC1nSTaq+MurN1Jax6G2gJa9yDI7TVA+oqJkg8rVQU3QMKY8sTf9SyiIk/t3Zodpbg+APnFTTE9JoOC4MFDVtElBBqhcC6vexVs5xgIW4LVC6Z0WHcqgtcw1rVQ04yv9QyAt8eY1ERKIBFcZgx6stbHMHrDYGNS9oY5AR6Aj0BHoCOw+ApxML2JggjMZuYiMKg6qTJwxnb3DrNxEteVu38w7CJlTPAe2F6+Ayyq4wKYsO4MU35U5a9eLucYJZ07x81k/rCX72/zP6ogpc8oOdvhaTFIGcUlwp2nbaDrCZdIiM5GnykxEhCnMO2Um6mlJU46uMeZs4foZS6Yhu1kHda30MRjBPG3GHH+JM8APD7LQ4zYwH/0tyWaazRd37zljWMr8NsG9x7B8PDBSmbBtmflzwG4I2PdOi7BW7bKyknFuC1pa7yrnkH/lTYEGwthBAw9KcpXZtd7Bmc6A/oqqGGL0xXcYsgAxgkCTsO/qWnsyaaDBAljeAts6XHQDRCp4EXbjSxnLWkRILExDqjOsx6zwLD+d0CO+NDOd+PF7vZHBYGHe8JEHgk1Kk4IWWeoMekIu1sPFwgaPizjxkeCTOBAnwHoTp218eIKL16RfHBKY6FopPElfwozjOBkRDREq2/U49MuXKfacQ7OM4+RUiHgBmcEnHsgkeFEe9LUUgBtuuXmKDW7JlmxMpBFxSIT7DSUcclOlZaqCB8yIKsKwpMAJ9CYFs0OsUDzIFIMDzWBXn++XJUkIguIa5EE0hDwADSCcOh6awoQwC2dCjEBMULsCiG14NItJGFMzSBM4Ny4crQw4lsUWSOsvrSKwYlKQJfPImQV3ImxW8xgR1BEQCfjyk3VQ38mbQTQvJAQfb3zjG7ftqgI0YgkKAtaOrCqqC5qYRJxtL6mFsLaQNeJUhLextFoFt4QKbngjnKIVg0GNlp/BHGqEqLtEpl1pHiyHNgSAPIgLm8uVPAQdA+F1qiHq5gtBghsdW0JBwzgmgDgoDLEqohuw1ZYR9KIQg2g0ETQXvMdUtItwOt1G+WiUMvERW4Rw4oArAiN4ZLaKDoSzrWmImR1O8IkwBs2yv4TWQJiVRkGciwaOkS3L7ChN9Yk4UJWxFFKS+qizgnrE0tEqqyGdHDT1zkEGK4WPLQH6BLdWBDImutdyK0e/hDMwjCyCqoyxR4SU1B0lVVRYzlhhENEeiikMCl+TybEqm8zvAYtNot3b6gh0BDoCHYGOwC4jwDdj2LGi2DE+DBr2H48r2KpMZyYOd4LhxVGP3W+upgMFvBR1y54wNLkl6LD/PAoriunGdmdgXd7SF5dXN06PSzAumXETtlTZ0Fhai7xQfkWYXBme8FUfGX9VhAXDHCHHyG0pCy4wf1HgmrIaw9KNhnSKe8CtCncoyXoKHLa13byWJWY6Z4whztGyu4iHtkzmwIHFrIz9eW5/2t9ZYEcJ48s0Z3RyvKHBDZZGU0jIHrh92soMhQPjWF8cBlaY76cwZDgYeQABA4aP+2R8bfDqGn8j7FrI+MHLoJB8chi0pQAnhwBw+z0yvig4kOKwQCsMCpBJAQvSyG4WK2ExJ8EFEgaRgy3IAlicRJgJHU2TB4+4W0lWDM4RaMjYscQwh0EtFAyH0+zlniR54COJEYjvgJd3gbhMO7pK8qzgn2TLhHbxAEBTjJdCQjiW5XQzQI7cOxXCKYUwHAwNmYSY2zHmSEkt0pxGiJnOSpJwri+222Jz5qgrcCBqyenFLQ51LerqoIlPmMlJSc2YunulU+Ivol1BAZJl9Ep5/fWuUwNqVxx05AFlaHPVCA8xG2QbPiamYtzIcrBKBiJtVtJOyuPTlnu+PrYtudMcOGCVZIKaVBsUOg3aybA0qXbQgIMqBmFeKGNYzXoDR60NijFJENlBXMSH5AxypQmAR6hCKI0rrljMTVd1OP/JQ1anqAVuIIwyYVjyeIVe0G+0n05pS79yEnlk4osXDEp7FMaGKuYyQRIcxFLyKWGkFBO0CjBJCJyjCpkvEVZRZ08//XSvvxW2oKhVJxVUWdzOSxxUFNcTV3L+QjFi7BEOzSxiRqWU0y2ZMbg6iEkhtjjclI8WS2jFJ+KSmI9YJwRITrsUKkBi7RM4ACjKrEVTTDTKEEfFigc9MtNpeEeZ1DWD4pJOVSy+ao4E0idiPeavAL1RGywp0xSDHtUHOohZCpdcicYaWiy//kGvksqgFJYFeroj0BHoCHQEWgSsKGHnlb5NW6zndAR2igCDbKIK38yBbRs1XufOgWTNjBVmR4aIVgWI7lgtdgxznAUjKDDGBpooVzTjK7KIl48YiJwc8QK2nbf62VtjXZUFFkiP9Qupia5xRRwb4aY6CcwtbBGY6BfKbdeCc14Zh5a7YkuQ/T3WHVYsV8dRFGXco+bkVD7hWMWZ+cIl+mWDUUnWqr3Waco4UZ4LwWtlvA4WBgXLO5wBIyjC4jNoWGvUcECVY8aF4J+gCYoxIxhZ3izR5X4fffTR/JPNy0MEFPg52NZ9PqdtavLZQg0HcPEEfIgWbPVuZsStks9BmeRzCmAZCGIpxGbg8NAyEDkE7IlPfKKDJLAS7BAkGis5f37FZFlxTNRVoR8E3TgO9MPEwHEOYwNZSV0TJ5rwNQwHaYSzYwjTJ0cIuYnDpedd8/0c5irZXjLdTv9BHAgwURdpMi/MIL2bwAFLHFq9M3dmHoJgSPCofQCiMNAG5yaaJppXb7jHZFZ6g4+f1Viy76rrzhiRQRyicCVFRD0+JamqTPlokDKERVQpH09DoQ0qk5ibxMzH5A0xm5ibzsUATbBAWIQeFsosOVks3cpM0hnsmqcC4oJNNA8ZpicVyyptAn3hOfkkYbqkMsRGYQhMzLVsgrDRPJatQb2XxZZJRPx6pxQGtPBOSfTyHYGOQEegI9AR6AhsDwLskmkjZvrpYEfsPtl1H3yUmUzSCc88i0WCZcbDYbPaW7P3NRYEqWpNf12gXwiy5Mot9LaJHfUrq+vRPJ1ivdkchgMnx47omCuSZOdP8IXsss5fXtN2dH0mqoDClXVOqc9EsXhkOJxlsFk3s6QCwitw4K7HPue0szcPQWV2Kg9sdKPgM5M+HNj0tsd9ZhbOAvPwE2cZeFlZayLB43UGAWj5joOJwnM+mofJipQqoioTgZUsP2exKG84ZjrzSnLeuKY255Un8K4SZHMrScw5/e35O5ziM2ejpobPPIXpc06sz8zCnHkxLErYdSrnPmaWn6fA/Cq9pDaPFM1TpqQJYcfZBk+0lcVibs45FhSvAKVJZBmifucBuWxrLD2nzJTV6dX51TX6Y2HikmakzQu9a/MHcwibz+Cj3c3sAYvdxb+33hHoCHQEOgIdgZUhwI7hvTisbieKz8N2n96ZXFnDOyckYOHIBoYdCOfTSuycxn6oAQcvEOF0cTCmgwX7obfjfbAHCAebqM7zTxxyHidw4J6QGVv6Al5CPN7b54jHgYPgUIf5nAIWzm7Yl3ZCfms13rpHhzw4hUHziwq5tQSNdbe4D+g710B43Gny0hz3HBeLzuwDHLa/C1f0W+JjXPZhG0Om53cEOgIdgQkE0vWaOEs5Ub0/6giMITB4AjYLc128w0wUgM0qYavNwYF5tiiTwiYTtnFs+9jNdsl25qbZJhnbcFtw4HDa2eNrzbmvvmEON9McHLiaECAPS/7Ew2YY3oZWnPJwFMXGrHepSm8DS5vnwYJrt9n5IG+T5ajbh988D9vQIhyAQKk6XsH3XuFZrW3o3Zp44Oo6B2cZ8ssy3iXRPd814VySdemv/Dpneq++w8I5IqFEnzn72YutBIE4viWYvRg1ytRH3YUpLNZuW6vsSKS7OLUoySmBGiwwZ2YM/ZpAxiT6hAr9aAhXIWMz+V/T6GMjtFN/h8WcErLNxZw0dmZhntPOG+jF9BUDfLr67p5FzLV4//zE3d0NMDzdBD7xzEY84GZi4BBvoZtGbH8/DRwcYA7NvL87u6reuaBuvdvOU9yr6uM8dDoOgZJtEp8uD/PITJaxDNE5B3wZSjTWnVjsHRZ7I2ARYmQGUso8AS+V8VZkV7+8GaWvausTLFCbvQwIyEs7rul3m4Rs3dhkT8jfUdMokFH3xGwCeLHZbukFbFBMLso6d+rOJwPRVqQTuVgSlt5pp3aEwN4qDChBUJ6P0bf5acsi5hqbYIGOxM9KOaDoZVFANvqoIbUY4MQPDxiL6pjkUtIGdIKEtxbZpjOg4bzpha1LUte2RZ8QSNvRqPkhK2UizLFAB6sq0IvmesCiQmYvfiVRfj3B67i8937XwxbTAYu9CG/nuSPQEegIdAQ6Ah2BA4LAYgGLqXeQbg9w7hf5OV+uBZZ4Al7l6udeXvjCF3JIfN0ePvcTJ4Dl+/nxeT+azYvjXnotjZ+q8vNv8dNuO+0sCn7y6oQTTnjGM54h9hHe706JLF9eu9447T3kj3rUo9x45M36NXU/0ef4dLjByzexPygASmTQ68cf/ehHu90HtHe9611Q2mnAImaoX+H2q2yveMUrItTlB5b8RpeXiu9UDFDDgF8795tVpEjgQ9jizDPP9AtPfhnBloIr0H47zQ+AGwU68eyzz/bLfOKbg4Pr1dAPfehDTznlFD+xTtp3ysz+GOjei3kQEH76wAc+4Ac4/JoDvTFPlV6mI9AR6Ah0BDoCHYGOQEdgeQS2PWDBP2Epck54Te985zt5FJHDhc79Ujk+Y1hMPx2rNZE/k2DLzHSV6acTnOSjlkKbk4Ulpp9GSa6gCAXY+XJ2iVWRvyTsdun9ArBt9vZ4RdAvmazSwfPMYlWt6mtWJzyxl06ibJnajXdyJCUqakWLFYXq63SZZZ5WDe3oa7Tr7wK1sgo0DFPcBXWk3GV477t51rOe5eeOph37wdZdsvX7cO5poy/E8OIXv1jw62Mf+9hgHCF5aElpGgNnnXWWX0CMn7ZSxuVDxOO6ZoxsDC46Ej7VyMpHR7jTT8EJhnrT0kknneR8Dcay6Z7oCLQIEKQetmhh6TkdgY5AR6Aj0BHoCHQE1ofAHviVEA4J18IGL7eZm1H6HhwqT+24+svzqTyTcKvCCYl9XQUCyniEVFJDwafMSdDjUXxVAEE5mi4LR5mgFgXkqJI8ZJXkoXyqIoIKZxeSYNCM1hXIRqOAfAktquhpFPBXTtBUoGxR4fJp1A3i1V+PVLSJ7epEtJIFUPA0YK9wiJJVE9Epf70H6DnPeY5bGHxLXxEJmslG5mRbQVC+8lFFizKls66nCUuUj0cJnQJYUiUwkc4CHPLjjz/+uOOOc9A6zw5EARgqVjUnx1N0gtUoU8meRz7KJES+JsNBwV915QeA5VOP8nM5oaJ38dVTxH2iWPATX6MAaojLb5lPymXdqBXdL6tIC1U4p+A9f+ibg4IFKipf0UlqEppWOFoPzGV6m9FNb3pT4x6MESrUAoFBUsGSAigEKTR9FPYIG6rHV0/FPigHEQeKYpBamxldcBWIANzjHvfweipnbYJgW7jndARKBMiJsMUHP/jBLbkkUvLW0x2BjkBHoCPQEegIdAT2GQJbHbDgVHBs2IUOkEt778Cb3/xmP9IWzoaR8HtOzqh/4hOfcGXdu9C93zU8YY+4MX6e2ilxZZTnKvtJ3qtf/er8HxuzanFv/HQWd4X1GQ29+93v5vYgYsM2XRePPvvZz37kIx9R/mpXu9r73/9+95m1csMb3vAmN7mJX81Vkqvzvve9j3PlRc0f/ehH3Vi51a1u5ffqeYB+YciVCm9J4NN6EYBfLLvqVa+KBxyi7KS9w+0f//jHOWDu9nvqFcf8eX6XzWeca8X1e+UVFjt4z3ve49A7BPx1vcJBd1W07mQ7Jr1bW7uYhxgeOGPes82kdqIBb4EJ5xOHKqJ2+OGHw8TNf4+yv9LxcbTe/rN8TL71rW/N35zDySc/+Um/mefFAe78owAH++fRKbCjDC6diiaMiy7IR5aTiazQAKDQMTouHdzoRjfCjzTk21/PVkxBQLmgAABAAElEQVQtAuCDE8ijhhlweQQoPSUAcnQ/gELTcGCJhwxM7ZIieGIJKZIAEHWjm6rYY/eGBUgaX/3Fqq9GzRUkT+FzgxvcwGv2g7iDBh/60IfinIgEYdCEPmLAS6qjDCJGh4zFuBuFm9/85kFBo5oGoP6ir64Xgqiu6Rij4CqKGVniYchAFO/5d22BDIgjkBPCrCFP+U5o6iwG3NbBOaw0QWJxbnQkKuJBn4SQ+Zg7hsz8IrG4VcW7+pTREMCNsm4q6akqb3vb27SOZ60nt0HQAJkgcMYG9oxyyDNYPELf2OnpZZddFocj3vve95oXoBMWKanpDuHREVxpETNQwhXJgb/bYTIx41KJAdWKtwwaMm0Z2ZKlsTT6gSRq2gWXPmIjpvNYrZ7fESgRIDk9bFEC0tMdgY5AR6Aj0BHoCHQE1oHAtgcs+C0XXnihKyF8DG45n+ea17wmP8pXrq/b6ZxV3juP1F9310888UROIFOSp+dtCxyeCEnw/fgzj3nMY7g9biB7jYL8c889lz/P8+Gj8rIe//jHc88cVudrpYPnkcCBm/zoe6Uf1xp91Py9+93vjgGn3D/3uc8hhSz/kKvsKceJ783He+Yzn8l35QghyLv2a/NencDFMpZiGWeccQbvCylumy5o/YEPfKBecPDe+MY3vupVrzr99NOFORDEhvjL0572NE6pjmDGSwG8B06af+6RLou2cIyVf/3rX6+KFtE58sgjn/KUp0QIxhUPR/pVBKAWeZXyH/GIR9z5zneWg0JIGGylFXvRi14kXy29cGaeS4wNbyh0T8RfFLSopA1qwMar4AyHKyRvectblIxOaUJdP7hll16txz3ucUIGONdrbzTgsgLK+ArZ2CeXjtaTE0x6x8TLXvYy3TFk/soRJXnCE55gKPmrULrooosg6VJAAIXhJz3pSQINwNEo19TrTtw8h3D8IiC3GWLY05ZMxI0CCkcffbQxEkqAkqBPSI4+cs4f+9jHGjudIoGnnXYa4kgpGbKnL96h8MhHPtJAo/CGN7zh+c9/PmeYH24INKGuWjpO2EQcSAvpRd9T5QkhAL0BVO/KSa4wMTAQnj7oQQ/yVLAJgGqRVe/dUAA/IVFGR9DKAZbXve51aGIvRocAeEfDta997Yq4vghqEGwBC3gaAjmqoAkHrZBho49JvTBMz3ve8/D2qU99ylsh7ne/+8GkZFVdQ//0pz/dey4ACxDDpCJh9kHEy1DI4YMf/OC73e1uKIgvAN/YmR3ud5Bq7QZBpMQjlNF30gVh3ZHwW2VwEDrxxoro2gte8AKBD2MBbcEL4ko5lFyNpYNbk8vMRfkXfuEXdBARMa9kY6xuz+8IlAiQnx62KAHp6Y5AR6Aj0BHoCHQEOgKrRWCrAxYcM24wd9cWq7MVt7vd7Y455hiul51tKPBL7Qbzgmx38zd4HcocccQR3D+PODz23vnJvHFOyJve9KZwa8877zyeLe/uHe94BzqcXo6ThjifgiO3v/3tY6O+RFkBPph9eI4T995WPC/rJS95yWtf+1qHFNwmiAJ8YNvdWrdV66/QBr/XMYRjjz3WeXiuNTfeazi4Zz7OWXCx+KI4cSXBaxREWHjmL33pS1V3sIJPFR51cqIVDqRP5CjAVub3OlXBffX+Qg4bHFjPQHDEnU+Imt1sb7YXW+EEXnDBBbbHnSu5z33uY9ddbEXIgPtn916m3gVlZCXuete7CqCAEchecWqLW2REPj8cD1xHXq6taTQB6y0AfkBe98HCXYeqJsR38MMphYOwDjaqLuggj5ErizgGQIF+tB6cKC9w8MpXvhI+gbyNek2IL8Q+vwJwwI9EVPG3bAU1mGOSW+71itxsP3QiBGawnNGIKklBRQ65OBcMuccQUP3iiy8WAOKKh+Qog22ixTcWoUAQjHB2CAUCxt25AK6v4bj//e9v3AlVjAtpMUy8eqMvcHPPe95TeWEacGni537u57wnUjeJYnaEw08Y9FQ0jQx7RPDEHaTJlTgIzh3TEBoQAnNGwGiaBYcddpi4AEjNAl+dhTHW3vgQ8ZckHkCJLGBJoEdYwZkg4Jx//vn4MRzekSlY4NiLYdURRDDpfIS4EuLVMOFNQ4ZSRaSINxzEZfSdMESsB24ahZvYELly5sWI+G0OQ1MGUyBsMsLcvDb3zXcHKEAqRzfNaOEzFMSh4E9mhGZiUPwtezeRxi2U0BHyMIO8CFbfiWjJxkT1XX908skn7zoPnYESAdOhhy1KQHq6I9AR6Ah0BDoCHYGOwKoQ2OqAhU5ymXgpnB/eiI1xO/CcDdahvxwM2+ycc2l711w4RzA4aRwkvpOzFUIVNlFj59/ZB34d39KpBxEE/olgAbKccH41NziCILe85S05fvZvK3w1YfOcY3Pf+97XI14ZT88vTQg68GwjdoArYQJb0xjjiNrr5tby+viK6qplw18QgTNmn5yfJqLB00ZKxEHCRjGausB7rFof+8q/4grqoyCLcIO+a5TP/OQnP5lbKEdwgXsfoRaAgMU2vtMlnEA01dWiww52xfEmXXqh0OasYoynCnbBC044HLiXXFanKqTVck5EE9xmA6S/mtARLPFpNRH+JO/U7RLdrFxKzekChrmOTrVgGM2qs7bQoef8gphLPDI64iBuW8zcDDcuABcn4irn2GHDAOGw7GxQlkMqRI7EVhxmIRjyXccQVREigZKuycEkTEQfFFNFzMKAit1gSRBH+AYmuOVOizjgQa8NjaMBAHz729/OUYeeMfIUNfEvQQ0UXKa4y13ukgigjG2CLVqnuvM7LrkYRARNCtSILtkmw4bGUAJKbMhRhTgyg46JQwz4/AIQ+NGRFjHFVBfgEF5B2dyJAQ2ZEQu4173uhX8fYokf9AkDTipS6OiXTGd8IKykkz5GSqf8zU7pLwqkQkRDeRziSuQlx0JDRAKSMEEBwkbf5MWJMzKkUZc14a8CJAfgQoFZHf15PspjAx1xTL2O6106uFM687TVyxwcBMhPD1scnOHuPe0IdAQ6Ah2BjkBHYDMIbHvAAgocmHB4/OURcWkCGnuknD1eLjORP+PqAddIVEKwwA62Wrw1G+acPVWUsWHLc3OEHh2uuA12XiLHzLa2Sx8cTg4S16h0rnIMVEdNcEQCDxwnzpKDCQ7V8xu5lPI5fkIk/Hls4AFBe9oatT8cbKMcjdrHFrDgoiv5mte8hqeEmsMavEq7+pw9ncqmpxMYRhMFLAm1+Mt/1iOUNYcZ1DzFgI5z7YAGIpEFZBXmunMIOb3cP4X1IptTHYa+RpcDFmmdFe6J4ALPWVsyNaGkgwD2vR0K8NXGtXytc/sxJpzEXddi0g/K/MajjjrK7YOgUD6V1qgddcdekELclQehJYOosJyqcPvVuBMAaOu1MwLRIzw4D+KkAD+5rKIwZESRYGWsBQgcPVBAvniQAQ2HXI6mgaybSqJJ9gQyyBKCYMSn/oogkAejoLrBdSJAQnlPJdAXF1BeGgX0RUMMkM6WLHlEKnzIp9gTzNUSJDIuIkQOiagOZ0NAdDn5yghFGZ1gjCuOMSEqBx/0RcWSeKT1Bfik0Vf0jRdmyC2EtYJCyADQWmEoqUWn/HXKA1bmFzrOQ4l3qKsjWViLSMXwSZSPlJGvvNGBnuCdsJEYIgTEOIT2FFAen1k9uEri8ydQgNLydOZvsZc8IAgQKmELStU1LgG17e81hk0rk9d8n+ZWyZhxJqny04U9zcIzS66jQHKLVQxPNxEg+AuEaRyyZCA2jQNgfTQ9T+FpDhd+uiYc8BOU5+laicPMsVi4pzMrxtgpZoinBy5H+ZA4TM2L7Bqy0/MCzUEOpzkZrLJkZvQuBm6M1GLczoNbS3kCgSSIT8V2UXhioKeHOMFMtsfkpwUh646hQZ1GrTGaSSETwQbOA7oxyll+tYloHc2Z0y0n0cyuoZlW30ThAGqwO2MgzM/DINlVZUYHJ7q2qob2Ip09ELAYhJXM8dPKQwEG2EjLtx/OrfX11a9+tYP6IbjyuesyuZScMR4s/81xAOcd+Py8TVvxrpyIQXBjBlvk13GiyLSnaNpj54oLRiBou1imDXOZoRo0wVXmkTpz7lh+EnQvQwGON63nOIZ9cm80cBcAZSxxO7msHLPBGaVRnyQlrfuiDAofenK5pSWNFOLJp/IyfbUDb557VYHOJhEeNVjEXDiBg41myUgoo8U4MBI5GpWQjwdd1nHHWPj2SU2OQIBWJCpqqvD2oRfcVk+TrFstrkVwuUEdUQYVk35by9Ooi6y4gwE1LjE08j3Fv7AL57+siyAmSQ70XNNwkSToKIN/f/nhuhDt2uFP2ZPDw1dAAnvIClgISYRWRYRgiAgAStwBfSWJhAsOySeJDck0ChLZroSIkkMWhoykER7dQcoQuJ8itgIQESJxNKLoYIj+ChPoXVDwF0vglVBRu+3HI0MgbIRbaR99gYBEW3gsR2FsOzZijAiYG0AQEKpzysb5IwcZArSx6lU+amIujiaZvF4v4kIQMAViTE+fUvaqiv1rR2AbECDtYpQOB1mhdoUfMyiDceayzyAblJWVSEDfIiiQepvb3MaSNDZV6RZlaEVnpiwxwoi3vvWtrVktZZqEQrOeWgWsbgo73Wb1bEuuL4euFskVBcaDPh5++OGUJIYdDRtsVPDXGTrcWgqdtwKFkCudVhWGKh1uPYrzdMaXprrDHe5AQbW4gVcMGlnw0tLKOJumsGhsRXZ9X4MHOIja66PxwgMtalkZbNTiZYit4K4B0ttwsCfUdk1do+x+Ytyrpe2RVVgfW7IWKWMBB6BJ0+SO4B155JFjPLQUls8xcFZPAX0rqUiiIXjIQx7CJBijzJJxeJY8WK/FykkOqWjnkUlhJ4Y8QEwV0mVeGGKXjivQPDVx7G+1QqWWJojoGDMrzGdgmA5MQSCAwgLtZGW7pIKL6HpruETVEcw4e2vLJ2yeljcTxD1QloDjolb/qpiJ4JKv7ZaqoqlE3mw6VvlGjUVBgOFM5FjIyNKuFdmq1gq/0qXMP6Axt3CuX97wZQttZhMA9DY3E9CBblLBXCyrEEVnvZGt4NUcW85ssg1Zljd5GXigAC9SpNEOnD2zViazlils3pl0/kKPxevVYzivWszyK0zEEmDuOBEMNAawa8JM08EmyBjtZBuSvOkav4yJq2s2z6ryppsZZB+LMqGpyK1itJlTuhUOxAy8QK4ogDd2E+3klTiEwFN9eDBDwUtBWQKqUauorfYr54K065eBtmzhwYbHapvYB9RqmdhDXSJMpcwl54TShIm7JFZo6XhEppW3N+4rJ40F4/Q+4bDAmAN8NlpYGbKbpMoEOiZMmSNNuJOHcilSUnkcmktOUmApKqLvY9NbjiXKSwHsxVnJaEPmIDG18nlhpAUyyidxX+k+ZMscpHQkiUeVwb/KWKs8Yi4I0GQZPPtYLeiUtndZrExosfyaaU3osr88Vb1OPqMJbjOEqZssn4ksmTmRkI9nFwE459YnigzzTAGZrpCM9Vp+AIUICjH6VdeC1ao5X3PUWGkairryowsWS4BHLQmZSSGZUQV7VK3O5lOJWPiDPgD1hW2X9FHDqsyyijSyWnFNQ7zGwsPCQ0Ex4RLl2RwOrQiyuFjBK9BulPco6EjIUUDC+FbE86un2a9oNB/Nn9AQxMgzjW9OkWcfcR+Xd1x+4bzNT0of9dTVKu/4YDIyix2YYj6aGpZthmZ2cH6avWRHYAMIkMzdDVXoo/luAlIX5pEPw5ft1XoCIpheL+1KlIAFfcV5U4YtXqqCRIymYne6S+jiJOWDLCfN3HQtzhuOspgERad1lrp1DSco06XU1CYDFmw+byly1IvZql/WDgsrg9j5R9fl4ueWSp6Vt8QIjNLMPlQWbeMtyzxw/GdJywqFBjTbDPQtP5Pz4PAap/3UU091pC5LSrA+BVu9qJjKshb48BkuvfRSLocrohaysvCa0rrv5UqC44JHuGWp08mMcgPnPc3czqpdatb7mxhF7BY40ORA81bmdgeFtqeNHRt0VDMsBzgwosiDVaAkSwZcU/VeJLa4sYBDhDlIGtA2E7shkzwc20K4Jbq6xj6J13iVrGba3gCevfLZdOYUkXw7W7rGRSwXfaQ4RfCBm2J2EXizbDkAuqrM/U6C4FLSLVSTTq3MR42ZyjRyx3YDAQuOtxuprgATRWwYuNivagMWJqwZRIBx7pMMEwz6gfvNFmLmZX4mBAoJmKupoCNv7NgqssCNZySYjxhIytKMZPPCecwkJeHQKE1iYtI/TAKTke9tbnrpm5fTt2yXdVeVdgQbDvQk7xcDQNP3mQEL0u6FetA2vka2cn311/TxGjiSyWxLVskDhFmGamXAQgERTwJJhDwlZkaNjmUTmkFCQoMam6Ud0ClMwEw9aAsX+mtossV1JAwW5R+/eCBoYroxUDlZgwELvaMVrSyUqiGGgBmka4bYlpX+JodAM/pPfepT4UCo4AA9hc1NFqY1rtTVxIw4EeMSXh1XBhqIG5Qkjg6a3lKnFrLK4D94EGwyFsnD+hIExuJCXcMBCD5g9Fp9ifU1uhcpf2E93n7uCZzPNJ8mJEUpmki+TRKH0rM8y0xQQAgjJJvfLsxmsWFw0OAkWI5aWb5KCEub8Hx7ZYiRtceHHUbEq1p4MKNMDIaCly+we5IUi4EW1i49wjBS0sImRijUij02Fl1v7bcFESKrWPTaXzrIeqC5pCaBQvl1MK0MpUYD+mupFhDJYjaUBNrFdKt1JQtEYh7YMazLpjePmlrJmUZrsJ6ZuT7zcJtNo6DL1ic0vQ/CUMYSxSAwmbMY3kLvJ1DWGMalAnKwpNfUATbi+AyyLDlDkxQigTdmKMlBnGkiGp0FEKTLKFycTHTBIxxaeg0lzoXGkNI6u5ZBzFZDk/wgy3Qub38QPx+mnsKVLOHWqXKDTqXin0534AIFzDCkMIYgl0AO4091OYTEaGpa99koNKAEQfU3e7RMoqUjh2Ea79ewOWA5J8/knKnhlBMLhoS3tfDQZsoxmgQGBbJq68mkM/UsSw4r2WlxjsMSGPy31ZfpV/ADQwnoxUD7qhWDEuMiXRVYssXFqjM6F6vYay2GgElkCk/UJRi7HqoI9rjf3jHsXTx8VDOFFhJTaAMWphXXkU42NznV9NXEbDIBvRBahNSU9Cs/zFCnn2gkWsWPH5WeAwOR20bZWky1butsQmFO4LnwIzNX34W5ceKyocVXHy21GLbQWwS96Le0QSkuroXzbvwE1r8CnFtd01+g2eZKTmwLU0H+AoG/TV0zJ7i1FlBvcVKd5s/CyKJDe1P1EZ6GnrcpcVT8ipO4SQla1lphAuyiS3wtax8Q6GQLBPue68XA0E0v0rbeZYtWCqENulpH6FgeDpOdpwQHa43MLCnB8gGFNZEnBjRNgFfAQnOcqLJr1ln5hsCSCjcCAxat8FIsZN6dNCF1ZYvLpImEGIQRYWuRCmI/0SiLy7JFJCy1/GcyQGz4h3BgIpbhOTEp+USdW65r/FjHKPj5bDzi5/BCmmrGAkRmjcURkWidbMgkD+ZpWAXL9HGeuowiOGDGzhwjwfCN4aAkGwlj9rpJQqx9KqpuRrNkWIyDLcI2fiGON6iDbRlE5BM/M4v4BWXFCCeNUZVnFImakRNiZpOPPhFBIz/eX25OAbMqv46v7BBTPuwuqpU8j4GWrZM3thCLRU8VbssrQP3qu17ota9Rl4jSVLpZyoO5xi8wZ0mOC+PKExuz2Fym52mhMP+ydQkMC5XSaVCl3hlRopMsYcZtWWxNad2xXlhTLD0M0bh+3oIQrRti0UwWsrMS8ZZ3msHH7/oJc8AnmWQWIkVodUd0GHE40KVsRYrLxOTZRWEy5oificzPUtLXyDdhFQZyOAVJmbmOB9OWTN773vcWkxKOt4g4KARb+4VZcn0J6hcUPFNz09Qzgutra09T3jMBC2JHjfo7Jvo5DASO+Fpuyb3AW+hWVpQ4HB9P4I0ck37mBdG3xBJ3os8EoSZSuJNaJKgeq5HtESs3j4V4EWjOofNp1mDVy/KImKg0rPWM2mLIYkkB5S3nNL7oo4nkNxQsAH7+wA6GFd3kJLJ0seqaU0UrBNdfcmz+65E1b2b3S04yjWd6nyrk8rE4pbWCsjlJNTgWCJMsXCUoIMv8PO0ia5FjoAiFUig0siGjC8R6/ShGq1irhtqvVAz9gqYBZQZhg/oWsMA5fqBkXZRv9QWdwnIsKjCXEwzTTeoKSzGSjjvuODhgSdrCU64KmgZISI6E5YGBpa60Fu2N2JXyY67TN9IVNo7GnZ0nzuK0MIJ4ZvGwa1nPFgzMaN1T2xQKa5e6JJP2HPzejeWHni1xQBOf7CHxV11jQODKiABTLID8oIMmeSaZRJraJaWiIXoKf+sfZKhyKxZSJeUF0iDVNA4rYfDVMPHoBClsBbALAwddI89plLQtxowu85HSF3CxgG1y2gczldiCViBve/EoqUkY8YqTktRO00hphWtquoFUu5qAnpON5jgbK7qpACQVYG8tD+lOmezltw0BUrEloYpAJmTSqucihuXPTKQWWtB4od6FbC7TUTZ2HBwYE2ZlKDTeL1vZPjO1hpr1wt4yw45zSzslfdrYvRK+BLK0ga1jGiOfbiZhRHhZvHTnCDhXGsUPxix2/B8viioPWVCh1gtLjO0s27ZRWBRGl/VOlynSYNviItJBuXnZdiyXPFWkqCn+iU25MgYNdlF7CkTJ2MozFjDh5wtzQMZauW404KD7lgyjFr4K5vWUojaaVoocOENP0Vnj+NgCGcYUbxYyC5NwjAWrPJxsQIHDeaADrVn8CoV1UyucKCYWmzu7RvbsqNOoCgBQPvkBo+UMBfslXMEsvKaE5qwjAivQsCDq1JioY4A8WECNlOnjHLscs5uoM2kYYDZOkknWFLKWdZ5kiJlHFgXHPzlgRjleuiTTQEDe+5jIgHUkKZBGHpSjCqVjlk9XnqAT7C3b+CED3H5yO9YEaWGwORdpLqf8K0ykGdL8ujBdqupsKvEaxjCbhIRPTHwUTCKWTEWh+ipOITRPJhM03iMGyCpJ20zAgqFlQBkeumPikIGKyfYrO586NetNBNOhLWA6cD2AqQuhSaKMmCYxY2yUpjLhCYOE7HFSoqRwGHeG927OSpdjBH+7nqIV5q9DHJtBqeyj6WZSGKlYAh72sIelzVYWk7ayUC8+1CzrOvSGv6BjAQpGAMf2c9SSSSAhQ+Wm5DBrzU2qzMc8gpXC/vI+THOFU8XJ50xR7CKMxC90kUz2OUVEoYHRemGGyjziiCPMbgY2Hmg5q4nMtX70CALCWBSI+JTw6ISOWisnW0582wMWho1s8dmoDG6kgLeFh0TK9ynB9dXE8DF7TRix2NicZ7iYGELm5rbJ4PAC1aMwiaQ1TAxLFIVoRTEllCxpZlqLfGCOt9gh90nQwYqrllPrHBtR2Mu5+V9+JBDHpxYpuLBy+EJOiJkYpoRoIrkUs7BcufAvFEJerXDipiqaTmapqagMW0p1T0XiGRm6VrZyeZP/2yhWpXW/zZHpqXXXkRNsO2EhUmuJjf0WkNp+0QsIZ3+DGjbEaHn75k9cb768vaLFslH5OEeKY0mZMnpUxzbPk9UCKF0L9pLC5bQOfcp2M+0Ja4YPbyjZeZA3n8kABWekfBUPgmH4lsaXnFiJYa4AFa+6gda0pRc/AkNUOTPRU150uZoGD/6CV0BafEFYRxX6UTGt+xAVAxf8VyAnCPINmXFn6eo1fmDOdqGALLrAZweQTAEXJqBhZUry80kglLRraamGAGU0wWjtUQxBlo2K+CSE+ijhkaFUkTTCnB3ADyFRdL11nc4l0sJqwhlll0uQdTy/Zl+qTPmWH8JgMTYWFk7tZhkJHZRDvKN1PdU6STDoLFScKxO4SfhqXPCjgExTUh8ltOIvUTRBrLg2EBQmAMbaRGAPQUlD4hSqmy8cLQDGmhTEg3+1fKTza6Tbv4pFux6Z45Y0a7xBZCcxQy1mAprGi2Hql0SxLQQj5ijfDoYVrh2vtomes18RIDBbFaoocSarBDicyTI/01RHRGwJ86Hp8kVKIItJ2PARgzbp2H8mZjwSuqXt6UkWtnxKKatQFD6+mrY5DfPpuhP6JXBAXVMR6UaKVpitxkvw0UKcPFBBlgOnSxi76V4yiHlcFkers/KUXpSniBgANFUZ75BpdVaMHZxkJSjnKiRhzcKScSmLrS+ts0CwG2GUMyhAGxs4nOCWOs3WAwerBs+BNo58YW6qmyfA2lFYNyOfyrVg2Tux1mcEn6T50P8+4XhEYS1yHrIhCaLCJcMDKFL3lgVWngaFUfNBWXpCJvFDnm0MkIdwXVSxdDIO5Ts+4F6AQQwO8U8SSmGQr2u6LFG2olFAJVZR3YSyo+YvyYyZGPlr/cv1msf7sgIKxmG7ZMbSb1KAcXDPmQgxvXxEGYiQ4GCJQElHenoUsjBzjlDlVwmBEroF5Yq3ssxq0yZyaABTYB5xpU4ZkESF30EDDAYsMO+RT8kqSaBOTSuTLhWXAuadUIUtOvo8y5M6X3kEdCyuKL14BBnBUwygIPy6+WhFsGGMBMSlRZcmxECnTCjziLHKjI+6lJVVle+mI7ZpY9p6BDTTpJopYnByuGZRICj4yxiO33PMHCjxF8Qm+D6p0j21ZwZDCZo8R8QcwQPDDw9Wh3mmTDa0WAII+uKDT4hNgLYY/X1Ta9sDFoAmqdY8S6mFk59AhVntrAr+lsNAs3B1/DXY1hvxYwFRnqGPHPnW0VNOOcWKkm4GmsRUmB99riBdUxIs00GToDsuqBipkna4lM9JU+PQMowliailPJdSzMxhCu4x70uOArSYiCN3DgUHDjl1bEGsxuJtcro0xRvEoSCf6yTiCw6AoEmUuaPcdQ1FK7qvvyUIYzna1Rzt7/4/tehsCCst+NR9QXeuZmKSvcawtdlSLcrI5cazdHQzy0iUsOPfIU+AcC9d4ww+RV40wRyUT7Gi4KNigpbatiQrjWfKCwgiShZCeyNKUtPO0wJNUMBmvsvAAgGMCS06yqEW/e5oWQR6ohUFqCQDJ2YBZ60zu1ldVqBEEkSI45CmMxzuu4KaPYGCKpYQksNwwZJiAXvUVcAnkAeFAuTTuPN44SbKIIeoOGnGvCM5APd2BoaviIYPkNV1msO+FoTbUUAcAzQpxvBMUJXHJ+uHJBvNtB607vgxFU/e8B/sGXQ7RbFjdojTL/qjjI4DJPsiEX3xtyyqF9hjxzvsKgjCoCEzWSB6oY/8ecPE0EdHpmL2c+AvHXISZGFIlmzyMHwtWqYeQ0QTSZDwCzMRfmdbdF++KqIVeaWQSWRL08KMYPhLMfej5OUS9r8ypoA+BpGknwnFVMyngAWypxiOMhAWJss4Jiatjr6W3Ca1njggCBDvrQ1V5BBQJqQ0ZTvzqwSZT2mvHsVXM1TUlc/PpoxpJZ824GjRkLw7Nl/mlxR2a44cMvy+6Mh6WqX0jI4kkyDihumgVcM6FfkUgmWF7mJMi3GndauP1vSsKwE35+/YD2iWPkZZJtNsd/4etJnylHnmry+hC2mCRyu0mfHCA25BkU3DAXvyDXFa58pQrfR2RDcyYEEfylHdSkctBxELjRWBe2ZVhWcJcrYSCXvvcKBCWRekqHq67q/Tog4BpgKU4JBRHn2Bg0XEQIvpZMCiZZW0WP4E+DhgPm2BMgeGzBiunU2XMn8DaRNzGgc8pEkQ/KjC2dN9o1zNgijA8LCxT+ScYAKjz0RHrKFMBaJIlsxW7neiPVELTaZFOJBGZKLkOh7Nqc2oSpdidIrlI9g3E+dkFRoQBiB5MOky3xRr1QXhoXnIpP2bcqTIHlOZ4uKYiBwJzrI5KTRilgQ3mZjuPkjNNWX00ScY0x0M6xohEQhmMI8xTKtzZBwzifDNWLHIR4rwUDsM5lJXE6pBHjDgowkVpymv9il+pkFbbXN7jtoXJsbWsk6sBft5gLb6GQ3xwiqbq+a2rzG63BL3GmytMC8IpUwekVWHK8si0TW16DiLcekTokBRmh6i6YS4fFShgQcrkLMJ1AQ1RJRRQ9/sImFWa+ceqQY+bRAJroRI1IqYPR1k7gmRWOmjjKiKw2aOgdnXVZfqUVgBnULTV56zvfHgX12+OldcizHfeHTYZkaoi1scKqzXjADpYMCxCDlIMVs1ioJzaDQprcqq4PGyOcz2KNx2WUMcaYcCYglHx6Z3qD9NRKMCluK4wpzYQEenoCRTLMZsL5vQKW62w3IoQF5HRAFoJWU8qlqPrwjiX2CCYuJJAoFZ6UiIjhtr/FgY2BNOhYn+MLloPRiyCLnoYPQIZYALEgkVUW3YttwSBtQsltBT5aSTTjruuOOwASIt0miEzagxrZQne1AiJ0jh2TLAaReaIXIBgpGNE6eoRRlHM1QhrlZxIqc5yKsb5TFPeCxORlbrIZlEKKSixQFN5SGvAAELnNGX4xHA/Y2xgAZIjZfTB079MK0gBhCtRNMlcTmAEg4LoEIGkBIXYJQgheHIVEvCmifghXlDhmxJKlrXR/JsVXBpApMQ0zTOTRZtwURgwpBFN00NJzUYQIqR2OhC0NQW0AR9dMSQGSZfYxRi/uqO0AxZspboAlkyU0488UTrurmPeZZTzBGoOhlIekFRwYslHQeX086mAAa0ywdzpMJkCZnUEMkhG9iOPhoscTElDUTJc4VG/7pfETAptj9UsVrwqXFzkC4td7d8jclIz5jsq21x5dSoYiFs81rAl5ZO+pQAL9R0piisSplPe5jyuqbvmdkmqC9BZ/rQYRNqpy0gh0ayjlhNlBRjpbWsaLltOFhlfZnWfWwYL4EM1ks2RDcaYvgwn/yNfNov9B63x9MsLO0DLkiaDpFPyUf0wSOgEY8sHwn2ho0H67gwdFyXaPfwqyqb/woHndUpOKTTCBCrob9shvJ4TrJnIeBFW9BFK5yoVVfAvRSzLJkJImdpE9yxoJDJzN/ahL7bz4cP6W0Hl5DbEmfy2ZxgDdpMGuuIjvuI1JgL4jugswrbCHH7ho8tPVjRuQNwxVtgpEmOGTdYcnczoUTPEAbdMdPJ+Zz8wMSlYB/2EjtquhZ7xlkM94lYwoxV8zTLk0+BD6YpiXVeG2LmI4vXBg+LS36W3IYEHaILlLDoFes91hfaSRdEXhicvK2WT1hRvM6wmG7QVoy7wWBrS5Y5moAYs41RWuYHD2iyxilqk9dTci5wiQcCiQdPU9GVdXt68wjsgYBFgMKpiEBj+AlcC2KUPgN5IrLheJgAqnhkBaXaUtrkZ/mgaf2mI/g8ttAVm0ZfdSaaBSb3tFGLWlRGuHCZE6R8xRVnaZCHIMiRxqTyMSVUCf79NZfo5VTNHsVkM52UN73N9iyvCf013zJHmSrHI6aSzkZ/taiWzOC2/Rs0Y+nFj68MnbKKdMUGatYzh1F9PK2a4FuWFKgPBVRRsm1dTuTDFuxRQA5OVDRqkVYdWYcmfKKMHDraUwk5yhugEkk5hjKbJlfSMn2UV4uhZvmURiQeBSlf2bLqJnFlFDAQRlmZoOBpiqsCPh7JzDRInaqQo65MtYJ+FGj/Mgdj6JOOnLA4MyfoMLPEMnySuALBVUVWAQLGWpIIiYoC+m5MW5YUswqSnGiopSlHXcIsqKFMdC1br8haO63NPsiq6G/JnpwQVFKUpGSi5qvCVinhj0jLFLVhUOpFVEQ2Cht3j3CiTNVEkCVIUTGeIkuxeBTlVSQbCgQ1Zch27C8NElSxf/YrAoThoIUqYih5CIxICsfsyMGFBmPO/OLwc1cyfwsTzF9X6xm4FKZobOlumcVhj9JsJee6prO2MQUjyvwyDRP3EJ3fFBCn9EItlAUizSl1S875PgrNmmW3QOi2LbaBHOOIDYecrU2O+0V8IdrlaPnQyZg0ssmMHB9ekE9mKgkW+aU8WHfiKweJQ5WFM8EhccsSXBZQLpkNhs2fLEhmxhJCLXqnL3Cg9rOYzpJ/XYNhZmZCFcDasjIdrOzi7DaW8ulgAoDuzgjiWMUq2Rssv+uZ/D2mMlgwrJsVPwKCIjXsIhtFgKqell9jMbWespfYEqC2vSF+QTyIjX2IsnCkLbtiJXYOBALImIiJyw4srrbkrufEdQzGKhmAQ2tyjHFofonl0UUwETwdKyYfdBxvp1yJEBvVcJQTlijaxVHGe1gc78WApw4LCyfZAareSDLRymYesT9hRRE5O+9cMOeFJe+Fx07OWlMwn2ZYyY9MQc+zzjoLaHQvVUapxgZVWaxMo0Z6hSTs6VaSY5jwoGkRMTwQS6Sc/BUKmeChJN7Tm0RgzwQsiGmJS+liRb4CVRnz1qesFWlKk3agBClKsbrYmx0smXVNHh9ltFu1EmVafiJ/sHCSvZy/IQ6jQPu0bKV9ulhOMjOYqGiWDIwxWVUpycKwpDANTlZsi1U5bYtlK+hU7SblSFTUZLYEs8ogKRQqItXXrD7WYlWg+to22uZElbH8imAWZnZXjyb6PvEoiEwUqB7N5LMqXzFZVT8E/+f1g0dlp2YORFmgIqvRkrKvbYGKsf51XyIghOcYl7/7snfTnTIFTEaGb+nCqXK5L3ulK9G0nk5T2MWngg7iBWx3lqgDYhFvTX5MZ26Sv5UPpqdydHmsa2o5quCCKlKOOrKYk2aVEKhVwDkybgOHxIk2iHnvNdO8KrnWr3az/ZSJwA1++HsRU84WddMo67VPZkoAgVOB4VJJhkqs5MHXwHBMHvgJfiRL+NhNQJ6ndxzAkP9QtVi2vvl0dO0QDDUOHBsM613LlRCYbSeLDk+SX+RVZSh4h6tBbwtHjq0y12e4pra+K9kbq7KL+Xrt/j+bmXOYN6eSHyFLt1/5nN6w65wRSTCh4ql0FouEfRcHWukNmwq8REAJWPhFSS6is42ifoOBP7Uc9YUYhB1WcuPVLePcOKya2K2v9uS9k8suvdBVbrBhBggtDhWTDllDmMB4IddExMc8dZ3KKWmnvEUrHA6t1AgfHhtEUWTNdBM3ERTj3nO/XUM2B/NNPRUDu/IVLHYZHY33Ij/BAh4ZbSN0RWmH5iEhLXRkxgkmMgkK8uCoDg1PHmw+jfWCwnEmRbiN1IlxlMXQJ7ROxJx55pmAciYFpGLcdLWG8BNSWlbp6V1EYM8ELFaIEUEUCnV8nTja6GY9yCmX5KotT0V2FZafurgq0792BDoCHYGOwL5EwObhvuzXPJ1i59kIZfhWxw3kcOHsD48d5J6H+FrL2Gz01sn4iUoXu7z42VJetqhftsRl8ufLfHtrOsuWjUW/fCSt166p85psyHvFMv+/PGtQFfZIdECgxJkCLpm3WQkcOOMQxyqrwmv66myzK7TenG3z0DuhGDyVk8zlxic/R69LCydwABEZSN4Y9ApzGAhAZvoa4qHkoMfFT4A/T8P5bdGKyy67zIuxnJ3MA6RJahcTcNC7wKGMVcmxdy2+MLiRy/3mZzqryMkREjLKDlwYYi91GuwLU9PFSUd+eGut/z9YZXcz3WzFMMHg7rYIiCDYwD/ssMM8DTEwLxQ2Texa0w9xaDG6IObrMm/phfIhudauC/ESYdIGLBTmiwoACfzxaZ3TsQNvYiLbMrNbQJEWPgWpdgrP+VYTh8xAAPOCCK4LOWo9NtZKujwicAPACa9b17jo3qruPItgjbfFkbGqv4G/2e34kgJxUYLL7XabgIjXW8iv5n5FYcNfTTfHkfyloMgAVSzWAwfBKcp5cIdAGTJDToSJSYKbxeLR+ih8M6h5iCLKhgD+bty3HTTrnQzyl2Z2rQl9R8BobDzAapCHlkjP2QwCBzFgYcGwcNpqoEyJvrjmRLSCJiLofpLKIm1elcv5Zkaot9IR6Ah0BDoCHYFdQcDCJyRhH5XfmwywyLlwzHGhHA5b5m9Pwl0MtuwFF1zgyLFohZfGt4EV/DMDrOl6xwZIU54rzs3wiBVb9YgzJgJiS1A0xBFrv4THVq7KtF/R4cZ4H6Gj2g51ck42FrAwagxxh0E4AEBod2Vxy9DHoTG1t5kWjoRLEOwfMQiWT3ZK2kdhUR5lYOgRp8tXaYUHozxRXUUuk+1fFyJ4Efy0rQpYkBA46AscMmAROHAFMV9tzyYmEjB0f5Dn47AAH17XQNSKnJIkx2kFMsYxmz7/X9LfxbTzIHaeWcvey0CKSk7AYhwdK9BToSgCAC4f6NnqB4VDNE4ccAKzVghMfpXgowo92Fr3tsgyv0yjACtvu/CaDCEhhTXKei/L7GKaMjSpCbaYAg6DEzjQKs4OOOAgUOh3fwc5JA9qgUXMa+xUDlICIn5FmFyJcznM4mpMS42upu4ESnjm4oxRQCzJIQJXLYyjcUkt11bflRxDL7RHTggM3ogZpe2YErYnZodFx4ERd4gcNhElpE8ot8GABb1EDoVTndNpw2HRZVpLQNnPHZBAA2EU0HTLSUjoIO9V7Io8TDf6Rdpnuui+eWryC6HRkqFYJ6IVuqyMVcrSIqGkv/sGh96RjkBHoCPQEegITCDA/7TvZ+vJh70bvgc3mKPCe+GuTzioE2TLR7Zw+Xi2ARmL2rJ/2Ho1ZfmZaXvdfhPKrp21m4vOIG5DD4iwj/HPzNUdx4bjJVl8MJu9vAhGAkO2bIsnYDdPtEJ5EQc/N9hucpblq7TNOmcKwlllSLR95IZxS7TCHNe6GEdbpqI5/RWkrH+Bm/AnQTHoA8AhrnbbvOVIRwSKie+kOpuHC1H6URwMOXwz++HZOodNXeKB/qDbkCXJjyHm/AsKCIhkfpkgD7Y3cULAFB58b0JZflVpvJEHjfKCRKwwibIQFRxEMchSicNgo7rPKYIM5o3jYMAi7oNwhARrJrAiIdwnnhg6WELWZ/PeJjEwN80O115igpQdJ5+EwZaeoc98iBEPYLqHxcwOjZFP20TY1fo4gUbUIpncTuMiGBQneipqsAI+hNEEPrt9MzvkxkWkwJyNvgRXOKQoaB43oYxdxWp8NcpmvXsNqnu/GxDaYsooIO6ja6IV1M5gtELFCFjw/GGeqkMaFP4CrRymbEi4VkAq1C894L3yy6v0JD5PAqvGNF7K5iyP2ApJIG8zT9CYRDQwzEUl/B1sizIRD0LQkZyJgGPwQLoQcTLIYRnC5nDcoMI0ItaI0NWGHuebj53pb/BgTLVuDg4KT2BC09JpYmrGV1xselJY+0x5uEGDTIYaHMR285kD02PzTGy+RWPsM2e7pJMRM2fhXqwj0BHoCHQEOgJ7AgH2Vli3LLZBd8hBA/el2Xzu57PkwjLjndq24r8xoMes26SG/gQUDC97WU56czbYRs5+L3k73QsCzz33XOcg+Lp+etzeptYt4oxy710TaEizlUnqCDdXgUfqvHSUZKixVhl//Mlw44N5btj555/vjgmG7ea5ig8Zj+z0el+9SwFsuyipLRETH+GJBEemiA+TkenMXkx3Iqr4y71xYcSRb4+w5Ne7BSzy6QIJHoh7rzZ4NSdU4aeswn9mjDJe+TxxYhzlwMFXnp6j415NKpPbc+mll6qCjTIuw4vg0tg0dj5f0CqcVfLAtUYBDmk36zIibGVea2YypfgkHDmhgdYB1i4xQNx2NJw5JPGz6ylLC+BQVglRHBN1T/Hv3ah8SGPq7oy65MF7N5iLJJ/nmdR0gcOgC+UerIqmiTIwHzT0jTI5JDN+tYF/m9TahIiJdyu6n8/PhLlDvuHRtSV3mqObPmqN4VASDDEgITbtQ+DLp8aFYwkZAR3UfDw1lfwYHBj9tr2hL8u3aUJiujl2BDHzJQvoNTA9LSkIA5FPgg0K0ZAsnAlV/Gw8UZSjjMtHyObTZRJ6GqDF34qUSIGrLt4RHm5F4OCYgLCpl+yafaZJVSW+mh1Uqx459E322jLmi2NZ1AId5UABtRBONfEwPYFgMiZLTlXQWghG/DfiayKDNA+WjEhOw2wIw8Tb78eLjpns7t2ID+bTJRMxbTU95/ylut1cox90ym07qjIZEBKlbUhgOe7iaF6eIiREckK5ZflI0CFCn9Q+/N3yqJ4OfjWpRXhNUkg6c2Fk22Lk0NuIzjnnHF0jYF5oGstiW3KnOSlmKOewtkTMC3rGm0cvvvhiVazCxH4sjGXlsgrQJCIRNInwvZ/VG+yXhixbjuMJc6sFam94dOexZWC3cg5owGK34O7tdgQ6Ah2BjkBHYHcR4A+wzGxM8aBY+XGsgDPARuSlM3zTxORyM924rCwkl/O9rt+OnJ925sgJZJQ+hh4xpNBEkLnDifU3HFQWHjpO+bZenM1YBiW7mQnF5/emA7bawuBokSkpAoKgvV/t+pFjZivHgF/EKOf/lDeZuaBiFn4C0Ad77FpnKFj8bDX+Az8tOEFNptcu6LsyTl64t89JQ5l3xENzYzwDFtEoG1GOtypCj0+rOiuQ8+BOxKB1izKLPPDhk/ADl8EBb9x+fTHQAjT4lPbXcHvXuKHhunCxoncaAgsHz96mIeaEi5joLGdAJnxSGJRXETIkhDzwS8kDb5Nn6K83gimcY8c+dnr/kksusafnML9z6XrHwjYiILLnPIgD+eGbcUJgzqX3oscchaS8owSZBDtpJ4o6DhmxBqNGpI2jgU7bHQ5aNGruxnuBooEW88Kt0IxYDIcn/T286dd5553HCbSNr9eoCfew9QX1EAHRoL9h1nhToB7BBMgTHTEvnP83a0xJhcvWJ2pNPMIzb0QAAgI82IBF13hcJAT/pX8YdAiMkkCDg/sggz0ypqkEUAaCkJO20Pe15EfrJoVgGb2hR1o0K8HoJBR5IAwkJMtr15kCQiUKYMoYFFNbCMAPzXBNVc9wW1aRMMqcf6CRH6FJI1g+XSCtUYiRSVfMjJ1OUW4OSREVU6DkgSvoE02YZWJS5E0xGEoMQqewOSIegawJSBRbDuFAqIBmjOz2c6SdtlCezqTlxHapl/TVFSCNpJeXTkV7PQQGTGRv/KXViVA5kaMtY0TMcIh5E1/cpFXRLVfTOeDCHs3jSIi/Yg0CKDgx0Qx6olQSITP0ElapIAIpUlCigT2Cyj8Ho7mGSXpbtMLc9DZN80ivjXhJMNIGAkFTSfky8tWWlINVYUo0rRTWDhETs3uwJF1N0sxikia2Ur3DeLDKdKYOEnXCYCKQHDJDjCkKCkfUybik5gk6BIBIOOKh14A1gqRiLGCBWxJLBxpZwy0eRKjGouHEm4zhR2E80JPittCY5n9jT3vAYmNQ94Y6Ah2BjkBHoCOw+wiwWux/svmYO4wk9qJ9NocmWEL8edu5nK7kkt3vNRCxXW9bjzXD5ePKuvdbHZKXb4vM69YZRooxVdG3PcjQZACdcMIJdvAqv4gbwFFnSSvApOaKZLsLJHgXwi4cIUY8f5uvxfjDAw+K78Hvqmjin1nPQ2aZ+RkRBqgu+MuZF2vIwiBiT3PGkGWq8s8R9BRcoGO5xtcoz7jkXTAQOVdq8Yr1zo4oNBjNznEMOuqsVdwiaBfRruyYrZwsTSeYv0IkPAcM653NwMSBXc4l0FBJgavj3Ye6xn3iXegCMxcnXsrQ7rjijTy4GuMIAHkw1gpzKe3doZxkDaiPXVP2MZdJGg5YghgEwM57ycKZgD8/B57kxFmPmW5GVhxLGAiRBadXQKFpPgx5syGJGb6TMzg4yboG69hjj2W1cwD8dgAeVFfMCxp4zlmMRBliGPKXlFQLcQKmdxBwIb8UnqylvLHgepE6B9QxkI/ahHbFPmCLuOMYS8oD+gbCySPT3OCSAZTJPFfH3OQRCTzFyZqSE2MR9/9NdgGL8lGb1n1BMZJm9pkvwhMnn3yyA1NgjMIyiZY4mmAfYYAYmYQYZsiYX4so/SIFwE5sOGb0SQSwFEbqFre4hTFq0aNwzCCt6BG4gGYit3zuKMf8pb6IN4FEGWj6KCJgKCkrBxOELSqCmBQz9THlyZv+kmcHstofbUWEjiKNogkQwHZFCjJcTaB5RG7h4KOWYjobibIKsRQp8zZKCkqYw/T0lCDJF0zEcFk40jqFPawSdTwILLZldpRDZrw0R6RSLXBRehjwGxyhFc01Z6Zy7Jw4EyGlH6xEVBZmxGrpYQqwREN5CoqAEVcrl1+lwS1wQG2IedRCGGX5ZJjMkx+CJMxB3jK/TMAfD4oFD3C23mFSwCL5LMuDXTjGQuMpiYXYSuamnyEzEIgDgdiYm3ggdaKBp512mmEtedBZwTLLmZeJSpOfMr5TlpSOcKRFynRTmIKaCJXS+chqXWHYOgcHvYrgLn7tAYtdBL833RHoCHQEOgIdgU0jwGViGjK52LLxYSoxj6R5nnykkiGGixdMsnXs2rHdmT68F9ci2lMA7EgGFouHyYWUKugg68NsYmMxW0vK0sxEbobCTC6/w4dCVWBHX1ljNpqi3bKi3sm0G8m2K/MjU+yGfY8NbgAP2WvzeFnllh2u7KTxlJizFXGU0Sw3rFjGohI8LtdShAACCn3noyLL9NTZkgdpRJz+EBBBnLkMWCBXZXb0ld1p95VhjXJb0fD5lPlYYnkzmh1ixzMcxBR46WJS7ZDhjZMgnzzYvQx50LXKS7ehygv196KLLhKO4b1oxVYnBAhPxUAwg1sBLA6Mr2xlOOTxh5LbHaVRcHbGRy3wBvgEMgaOr15RE5gIHAQX8GzUuC485FIyEcEbd8UZE9zyMVBzjoaAGXp7+4PeEUngYmlRsfKYT8WAr7wFrXP2MGye8r3bUWhrTeeYgEAwN3PW4zk+BqV1vFHDMFdWLa7shEcU7eKQI6QY5uEDYUpGc8mVjvNF+T98Tl2Drd4pIFDCxy5LqoIlJ+2FTUU3yBiBhL+5ae9dEG2QWx4s/x/DwHcoY8mbZcE2fUIf8ntDcvQrEPMVh6WKyG5qHQi6Az3FoGHuDzKsU9Qp7WEulAqkJKV1E9OkiKbzEXjJmxlXOdVG2Uw0d4QMRAoUg6EjAJDn82f1TFA7iukUDlHT33y0WMJioe98eB1HAQL+ou+r+eKRjgRlAiBg4TiD6UOH4NO8oHDaeK4q5otLDRSO/X9KGDWCFPIgCD44EPrujACUUB4TBkNg/oqLibLhwZhqiDSWh30qHPSFPAhzQB4DpDd7VJWc/6sFl54h56qg5hNiFsM3OHCwMtBeDgph8R0BqbHmEBcs00EnMnSQgpqYywZI98EiIuOmicLLa54xxhbI/z8RsxysOahzB0v2zI5AR6Aj0BFIBGLJ8ZUVlZk90RFYHgEm6QQRe1BPfepT7ZDYGLTTG/biRPkdPSLMccqAD7MSygwjR3C9sICZa3/ej25UsZIdsbdkYY46b4epLdawJKmozqq2Vx87nLy1QaclSmrXwXi704xgIPDnB03wlXA1TYSJLMzBJRB4Kl30wVpcMra7sQMajTdYRibPBE3OA5eAQSyYMlZSu7aFneUhafxSgYNdlAdjZ1x4O9NjweVzX4Akc/aMcuVAVj3lm8GBgA06IVnYZrIDLHxOqAr6OP4wzUNWXG2CMHCijDJujfKqiOtdzAuDSx6moeCh8J24W/Te2IWCYEzo09siqD5OPpUy4cKtqiPL0yEPjiQYXH718tRKCjE3QT0x43jFToEJ1zoOA64zzjhj+YBFycPMtO4LzPkrtiVQO7O8AqYPZUI/qMLxnhZLmof6jVDaGHEQ4YHmQdBkn9BjQUGszUklh7ZEhRyCcGxwZpWxpjecbz2a1k4lPzsqXFacMx3RmTkLZ7F6uyMf9ERHoCPQEegIdAQ6AnsRAc7hSmIKZd/tYXAGypwl06xJ594ZfLYZHeLYRe9UR3ibS3anqs46FNnxqfLbr5wW21/8B9vpbvjvincaXJGZeRiOwiIaYz9/UPaRKOZrDsr8Ns2KdQaem8Fz4EHtrjzw9FoO2xxek0+bP5hjZOcZXE6RnWR/HWW3fTpPlcHmlswkDCt3pLHEySTnPvOwJ5wxOIsUlwAAQABJREFUHdEIIuaOrXIHFmDl7sPyVxvm4W35MpdLw9DLF5anPM/cNNFcQ3AXg6g7urLhaIU+6nt7nmK6745p+EyXyac0T3WkLh9lgjTu6B6iAKWDIXS7MxFA2yvRCv2dP1qx08IJ5roTPWCxboQ7/Y5AR6Aj0BHoCGwIASaU7TU71TYbOYocnom9/Q3xNNKMfS32H7PSkV335EdK7f9srqltQwYlX2vOncZ9CYq91njnnAs4g1fu92Wv2045UCCGxecUsNiRN9WSOiA5DoO4dgQ3pzDc1pneeD8gmMzsJvULNMX43mOvbJxJ5KAVcOTHDR2HpIjZ/JHKg4bSmvp7xVNPPXWM9I7iMWNEen5HoCPQEThoCGTc3cm6g9b33t+1IjB9UJ/r6yVtvD6WqOshDtDawtpau8r7Bdyq5aK7CTz/xv5a4d0V4sxf16G5ptscXdoAMuQBDk7xwGHOAw4b4GrzTdh5NinMXK/PmHhD3uYZ29oWHQZxQEC0QujTO0TEQLeW1e1hzIk5x8oEtb08yIGXNFq2h8Mt5MR5H2sWHeUHreY5+7OFXdgGluypLMBGf4fFAqD1Kh2BjkBHYAoBa79Dqkr0d1hMwdSf7RyB6XdY2Gl0IdnrGIifj9OzAgFb9d6snfe41+gIdAQ6Ah2BjkBHYJ8gsPp3WPR42z4Rjd6NjkBHYLMIdOW5Wbx7a59HwE6jl4H5dEQ6Ah2BjkBHoCPQEegI7A8Ept5h0X8lZH+Mce9FR6AjsFsILHbybbe47e12BDoCHYGOQEegI9AR6Ah0BLYKgamARd8k3Kqh6sx0BDoCHYGOQEegI9AR6Ah0BDoCHYGOQEfg4CBwhYPT1d7TjkBHoCPQEegIdAQ6Ah2BjkBHoCPQEegIdAT2CgI9YLFXRqrz2RHoCHQEOgIdgY5AR6Aj0BHoCHQEOgIdgQOEQA9YHKDB7l3tCHQEOgIdgY5AR6Aj0BHoCHQEOgIdgY7AXkGgByz2ykh1PjsCHYGOQEegI9AR6Ah0BDoCHYGOQEegI3CAEOgBiwM02L2rHYGOQEegI9AR6Ah0BDoCHYGOQEegI9AR2CsITP1KyF7pQ+ezI9AR6Ah0BDoCHYEFEPh/hz5XvvKVv/zLv3y6+r/927/9y7/8yxWucIWv/MqvVH668H/913/98z//szJf/dVfrcp04dU+1fR//ud//s///E9J9opXvOKXfMmXTP/22X/8x38EGv/93/8NDZyX5WUqUJFV4EpXulLbwYV5KHleYRrb//qv/6p3kMGwrvlb0ffIEPslZoV1/6u+6quqAoNfVUH23//934GgSitF2TQAiQ3hMRaDpNadiUncGjJ8tkNWtq4kUTeIuvMVX/EVpRiUxaSjd8hG97/0S7+0KhBfkSI81SNVxspXJVf71RBj2HSYOcRGltjEdDBwg2x4SnL8LZ/qGgFrcRvEgTy00lhSW1M65AGruubvWCt6RxgU1h3C4DNWUj55UBhuOoXs2PgSBlC0dAZx03QFL04gNsFzS3n5HAzrGuHR+pd92ZfpXTu+WsHqoJ5slwxYKVl1LficEAnlyaRBMTdbmst3cyaFkIfAAQ9jOCjm01KbOXYwIT/oAxz9ahlqCR6cnB6wODhj3XvaEegIdAQ6AvscAVYOc4ctqJ/M5UGL2dN/+Id/+Iu/+Is/+qM/+uhHP/qHf/iHd7rTne5973sPGqDoMLx+4zd+4y1vecsHPvAB9votbnGLO97xjt/3fd/XQsm2/uu//muUf+d3fud973vf133d1z32sY+95jWv2ZZcU87f/u3fvvOd7/zjP/7jiv7Xf/3XH3nkkd/zPd9T5cdXNuJHPvKRX/u1X/u93/s9nDOIb3Ob25x66qnf+I3fmAV++Zd/+cMf/rCSJUos5pvc5Ca3vOUtS4+LWQ8rqFZtfe3Xfi0evvd7v7fKX/fXP/3TPzUWv/mbv/mxj33M6Bx++OGPeMQjcFK2i9tLL730gx/84O///u9zCX7gB37gDne4g34xl8tiZfrv//7vkf31X/91oAGc4f7TP/3T97///Ut8PvnJT0L1ve99r6b/6Z/+6bu+67uOOOKI29/+9le/+tVLUmtNmw6f+MQngPB/D32+9Vu/9TGPecw3fMM3jDVqUrz5zW/G9t/93d8ZXNzieXAecft/9Vd/9aKLLvrt3/5t3b/d7W5nHn37t397RdlcU4yAyU9wzMGQyRvc4AZV+TV9JZYmJhxwgmHz92EPexi2x5r7rd/6rbe+9a2G2HT4wR/8wbvc5S43u9nNKieZZvjQhz502WWXhf+WpMB1oxvd6Na3vrWwSGb+zd/8DRn7gz/4gwTBIzhc7WpXA913fMd3ZMm1JozaX/3VX5FY4kD7Xec613noQx/6zd/8zW2jdKl5oXeE4U/+5E946Te84Q3vcY97mB2DrjIQLr744ksuuYQOofpMn3ve856t9kMKsKSixCGgIJY/9mM/hqVgBjgmFwEzdsmeTP789a53PSUnhi/LL5+gEPAMh3e/+90SWqfEzAtKkkdd0hekDlEHXearLjSmMJFL+dELkgAH0pUlI6G84bjzne9squYjBCmcP//zPye6BBh697nPfW5729tmgQ0kSDvl8Eu/9EsUmgR50COjQD9UetIypGumWzvEoPiRH/kRIgTGimf0aWlLLW3p84//+I+xDF31qletSh7Mr19QJQez/73XHYGOQEegI9AR2B8IMHG4BFwI5iCz71rXutbRRx/tb9U7nsPP//zPv+1tb2O4cy2ucpWrXP/611e+NaFU5KKzQc844wwmFMvpM5/5DCuf6/74xz+eT1JSFq1Q8txzz2VQ8hJRZteyLFuTvay12jR7+vnPfz6vGwI+QVzXwrIfDFgA7U1vetMLX/jCj3/84xzpb/u2b+PS62lpa3JyXvayl8EWwdIWV+aYY475/u//fs5ndgS8qDGs5ZQ8iPUAc5MBC829//3vf+5zn8vZgABf+ju/8zu/5Vu+hamd3OqOoMOZZ54pGmXIdB/Pb3zjG1U58cQTBSDKwlFLAfb6i170ote//vUG+rDDDoMYD+1rvuZrkqwyfONzzjmH4c4QJwN8GzRJCE/4UY96VOmNZK2VJyDwi7/4i8961rMMLuKGgNAazbGGfvd3f9fU4CLilmvx6le/mpMmwMFdL31v1VGG0tlnn224BbaEZoy4OSJCV8Us+C0XXnjhr/zKr6hFFEOuJMw7OZsJWPB4X/e615mb4UTpmsHiK455vPzkpzzlKYSHJ0YAXvWqV5nyuiayUM4LZMH7vOc9jyOa88LQ65eSP/zDP1w6cpx/8wJE+u4TdNQiCaDYTMCCuBJIM0IH8QAHw/rZz362DVgoSVyf/exn02Z6QTPwxl/zmtfQrieddNLd7373SluKVrzjHe944hOf+OlPf9oUExnkef7lX/6l4KA5BZD46K+w4DOf+UyTIk5tRD40zD7TREMZsFDgPe95z1lnnQVS8hYlpRERQuL0jg3f5xtbxT88EAOSQ0toDnt6KqJnIovo/dRP/RS2sx1z4eUvf/m73vUuvcNkDrHZJP3d3/3dqUzMwYCXECocJdEhSIC99rWvbUkqVQSFAzSUhS0QMV6wzXY3kCAtIlxPfvKTRSt0x0iREApQMOuBD3zg8ccfX8awcEv1fepTn9K15E0fde2bvumb/BXpqORHPJf8GGtLmNWHRgW1RIZ4ks6BTfSAxYEd+t7xjkBHoCPQEdhXCLCSX/va1/KrmXocSBZ2tZEevWXysjIdlOAkMNwZ0GkvtnCwn/h7dsPuete7MssY9y996UsZjnyPZzzjGaWjHnUZ63xy1puAiIYmKLdtrSTHYQdu+U/+5E+y9jAQNLlng5EC3gWfhF+KYc4GuPDPLvcpmdELZD0SAGJrJtloq3TUo5Z8NjdrXpUszO3ZjHcaPLCnOZMiEc4X2AZkVTOCsYqN0ggmJM6D2Ej/oR/6IWWgxEXhmPGxX/ziFzOv+WYlFNJcOIa7zUBQPOhBD9IpO8MQK10X7goXHWXOvDKA9ZSLIpz09re/3dD8zM/8TGniV02s6muAzwPkP/OuRSL0fUwm+U4veMELlOEsPfrRj9Z3DokJJVPUDz4lV3bRTQFV9E44w54qqG2wm3enn3561TWNAh+80IAMOngwFoMRtLKV1aYNrtHkZ3LaJ3BQgNspgGUrWNDKyHJQX/GKVwhM6MV1r3vd5Aq86Dg6JGxHGHQqAA/5Fx7KkhIxiQSMaBICkziIVgzOzbLuqtLBngiCvWs+s0glrnxa+iJQ1AIf9eY3vzkQdJxLKXAjU6iOPDhvUtYSxoUPB/XhD3+4A2iqEw/0ofeEJzwhHXV+r4lJPJzUOOqooyIMgQGKSHmIldEu3HqEAl1tCoutqK5RmIsS0i0lA2tKE2yhLsJw4xvfGA6mEtzMC/Jw/vnnW2ico8FPtI5bTF7jGteII3gZZOHhE49yUgAKDsTgvve9r6MoWVKU8w1veAMcqjg7KOCArBYpFlwNjtqaQEAW8hSp+Ptxxx2ny9S7uf/KV76SqiQVZooOZutx4OhHf/RH73e/+4XI4fZzn/tcnLxTt1SVaplxlK0P9ARzKSsY6q+AWtLsiR6w6DLQEegIdAQ6Ah2B/YAAq8i+DQfAHiADl5nIfWo75gy2TWMmI/OI8W0nsC0TOWxKO6sO4trQE61Im8wRBmEOUYzSi2OEORyrpEQcpQ7zeoz4mvIZiDr4Ez/xE2y+6SZYyQxxgRUeF7fzAQ94AEdrrAqyzEeGqbPQY2UyX8e5pk4183Myc8OJP/uzP3MqhCN0t7vdjRFcOQDJjC4LYfCc7Z/ziyLf/SA74TaTnTiAUglL7NU7TWDoVSkFIGlK8GE45NwbriyrPQx0kmlflDNMcmw/ljvPZd0VprXrmoZwibnAz3Fcf4K42Jx+iVOILHBoldQFMJoggoBlT0NyHFDixT34wQ8O15HX8fSnP935EdBVh4/Ig5lIJtud/Al+VviI83Ove93rx3/8x3nONnIFLMaIk/MIYpo+D3nIQziTSnIsbbC7RmHDvwxYeKRrxMO8oHDGaGY+BWXQxXdErDJzkwliAARXCbjE9sY5kGOtkxyS4E6QizN6F8X0lN4TjDDKN73pTdNnpifF7yg9MQgOrb1xqlLgD2I0DCfc4YKgQOVSko54KFCeILBvjxrMebMVS6aS6SkCW+Vv5qsuw8EhspNPPjkmhXaPPfZYXSMScLjVrW4Vszv40QuibsbJn+CQLhV9AAuEy6i3EYGbYJBGy+o0ydOe9jQ5DsRRSg76lU83kDZwum9e45bCjBZNFszQG7SEuG0GboyX8yCCSi7BJW+Unt5Zm/Q6JcdTM4jwiH2AUZyUwszwVtbtCQj0gEUXg45AR6Aj0BHoCOwfBBhDHIwJd51dFVs3NoJYSxM9t6HEkmZBsrFyN5hJzW6zmcxadam73Ddj3Yb1iQfG3ATldT9K23GiIQ6nrUJHDOx2uhGN+YnCHumUz3SZ8uk8PJTlV5g2sk4K8KDsXYs0jUUrtMhzO+WUU+ydlm4DR92ZZ7Equ4I+Ag3BmzF1ssBpcALGgyp9+Ip5fecZ2opEKoElKiI47HI0He3eQMACVxr1kcC8T8VnfrXhL1rhjBKHPDfPeRc22LkTnA0+CQ8kyjv6Tvj1S4hHZCoyHdE36XgvjtBXAYsosCPhiSor/MtX94HA9JQXi3GCRsxCYM5Jk2AADjCxk8xdN1mMacXY/KJ+aA7tYBJVDS3/lTc4j0Mo6HDaaaeJ6pbzghfNGzfEwm2QzAEVwgAan1YUI2MxEZKwLc+xz4CFKsS+knxnFswpoUDhIfOx7eP88LZ1l8wh3o985CPpk1QCCJr+oi3CNHCIkzJlK/MMsR6JQfiUFYX8zB2awaSrcBCID6mjOqYFuCS42rRFM9bNJGtCBZ90WgqDp/Cp4nd4Fv91YMexu5SQoEN4BBAtQwLcgsvzCGcycKAS2xuwMAesHETTqpnRrHJsKAtbB8aYJq1kqCw2mKaRWSrEi0rKpXSw5LozCbGVz8kik38DYsr6FJikgKhgCsg8oWFtDlSXqdbd65XTZ08bUL0A497ti0XL7pOdECNS6r5VwWWymFP2Ek2ZVdFcKx22QlwCNE+tB2ttqxPvCOwnBKwsPjPN3An/LdBgkrr0TimxLFO1ssY4da4bmJ4KhDdYoTeTclV+hV8pT7qOk2Bxl8Atd93ll2qtxyHzkfvNxrAfqCMWRAao8oM9QlYZjhxWGdasDsuN2E3rvEVfuB82V/nAzBi2fvCwMT2GQ4cCqFDvEeAd2ePFv6V/0FhqM5kKqoDIelE+ZTbYY7eOQIxzZcGy+HLhSmcmh/LyOMGhSEHmMHWczUGEUZd+fj7d3YT5Qp4Zh2Rbj4IZ8mCP1KjZ13UKPQMW8PEVOJ4yoqKwr3ZZhTaAD7pyEQ/h4bFIIEVmSI7D/5VMbgABjE23wg5x7QtjohXpNPrqLY++Yp4/Wcq8HoHOK0JQVtGIW6/BAo3BhoATR7rMC4YoxQKHEqvBWuvInIYCS2U3gwGSj384VEaavtAe+k7PpDyQcAEsJxHELKb5d4SNItLc4LsY1WXfetcj8KU1LeoH5Gmaq3oKBxqgVAIomynWBbNj0H0wzR0yMs25GzpFwZJ2i8hMlmAl7sNAJT9jIjE9ajObWGEBg+6QjsAl7WdExhiOFuPdT2aKIS7lSne88MKLcvTaQR4aGwgESWjM3xVyuw9IbVHAwkCaAJYBE95iRuKf85znkAa3ZPM4Vom4yeAypD2EJz3pSU4WlY9mpsUInPJifDgNW0U6Z9ZdbQFrg5c2uQ/shNjEZsVKGjUx4p0uXqPlwDC0HROlRM4777zVmg4MNVOOLjOHU3evpAtjRPTFsUxi4w7Yavsy1uI68pnCjs46YkqwV6KqWA8WQjaBBYPrwko44YQT3MF21XZat66jdwvQpA3clNYFry/K3d0F6PQqHYGOwGIIWCWtxYLppUdKO7FfmVY0DAdvMcrrq0W58YqdGqBAtIJb2sNNaftXZS/wz/1gSNjv4m45akHVWD5o4LGrHIxOuoidqq6ljV51yB/l8tp59Iu+dbrB+V48WHnxYIvVOWqH4TezQnGrDBzLmI3hngL/QbyJC+rIOksjY0+Do6B3js+owoZ2FLwMspAHvore6b6bHTxwISFuvFPuNuRLQ3yQsv15P7bC++XYb8zjGuSkzdRrfSE8Bijx8VWn/PXIuGet+AoZEuVp5OuXr8CBuU96+54iyGv12g4iZDcOehAgDzZUyw38pL+LCUPsZQ041Bc9Ck7wL4jjq6clDp5Gf72UkajD0Fe+ll/HcGTJq2TKjpgIPuwQYoAIm18rpNEMcm1nHoe2pLb5NJ5FDRy00S9s57jjBCy6rwtlL4AGCl0W25rgFg6iFcw/lyOolKqkVuhY19a8U4ay8tVAmG5seK5vyUNVcX1fybaX0YjGitg6UZJCEi3qrzimCxHmiGgmEDhZriPFC1wmuNJN1yvESf0+UXUGYaLW5h/pIB3IOYWAW2YC3KR94jxjcMhJIfnC1tViASLU0KQHxDopXgImbRni2FYzaPOd3aoWtyhgYSp65YxpwH82VMbPrKAgaMBByExU84QdsMCMpVKtNNTEAnUHmVkmk8rGDJaWITJnXSDTqnSr8rpvWYKzxJzV5ywmWuEImWlJZ41F2eckNWexGFAwbsOAzslzW0wvyHOl/dti8+ewJjn87t155xPiPhyPFdKfn5PFShJOwS9SOqYEFiPba3UEOgJzImC9YEfSS+UOGzUrHi2TIc7empPUZorhit6wFrD+Hcun8ZiJjlv7lRPcsvLzJCO/0b6lNdEGF6tDLWYiL91ml1swYg3skORZl1G2WLMgnY23r8i2dsbkggsuEPV43OMeV5qhSiqvMB5iP81xD9sSIsX8VVHj3MBP+qtN6IvOsqBElBzjp0U5AKwpbHiJg58tcJtjbK0EizIveclLFBC4yVvrwSGCtnkpZCjpvvVdN90cUYXH5Zb7hPvNK7MLxTrnbmGAJ7PaXi9JTXwHRNZHom6tTGpkiRfqkbmQmSCFg4EuHVRQ2DWBm8KWrQxYhIGHpuiPN7ygb2l2/kUgCRokDZ2kvOsJYoN5o4NPPUp+fJUJpdjnj3xw+ZAZW+iknT/2/9u78/j7urH+448vd35NCvn9SpoUQhMpmhSSEJUMFQqpUNJMqMgdIRkK0aQ0KFNUpiYp0izNg0qTUmmQoaT8nvd99bgse5+zP+ec7+d8vuf+ft7nj/PYZ++1rnWt17rWcF177X1E/Xj1+oUD/zMy9gscCESMt+9RMj91NBt2LrzwQvE178sYsXe5B3IAiz+FUS82z3rFm0bFOOe6tsjd2JSqU/bAWmQ3Zo5Z+ri2nGDuHY2T7gMXgfB69YlYp7u5EvNp3XpUHLzMqeWczIEBX+leQ8tx4KhTYBxJWAiFfdsi4U6zmJddbAaHJz7xiTqFV94sxDQNpPUiD2xxO5nq7FCK5vCKYmO+jkBPo5nIgt6xIEqv8ViZ6cYrbycxKROQvTlGVH6TuDmbMTsYSw2wYrumjH4sa0H+Kbn0tsHoECrMoHXCvmOjG2i8sTOMShrsPJnpcSAhzPH8JseyuE8ipWXHJun3l8aU5kZQv7RpfwWV5AnSBbxno4m+Z7VkqDobIVvlNQQYEA3uk+F+KyHnPLEh3gvJmQTbPhZlDIU6lG5Vnch6woxbM+ixyD8BIWWxJ1BQigiBEJgTqKGDAzyJa1fHNIPMs5zbMxwkT56LSogsWBxbOttT5m32T3nKUzwnbBdAexrmKStF4XsTh/uEnG13yUQ3ONU8cEOlAbnXzZyNe97znu4T2hhfz4xwMDhd4iAWr1wIV7vibtH7z1diSSiX3orWX6uIAviDDE+2b7sntCVveKCxRBb4SFZTJkcLjHp8w5ZStwTNMuCIpMylyciB9GcH/CKhCjfJRwdMek67iluym6R4mBZgHBis7LbwRxIepvDGuLlYZyzHzdH2e2Ni5XbOl14rlWxrn1ytlVJdrUuOffQLn07cP+tqn9cEImUCVbCzBzbJ+bR7xZ8vaA6P6/NUO/EhHFTVGMO8duMZquoX/vJDZJBbZV2t37E6ET2+tK7kPzLcu+oaqf797nc/WTje+iaq+qaoDYeWD+xtICf2XyGt0oYHjJySRga1E62g9nzoc2ZOrOTjOU/fRdtTYMAxaNiExTb6vANjiFdXig7YrSwYZHFIE6D88269ptHesY7Ajhn3dFyRSqUbB/yThaafLFYFRo2EhgV1USPBLA8Q6fL6vrvRTN3uCTRWqufNICKqxhC2tC7NyownfFIbGU4f8pCHCK8IO9pn4e+lfBYiC9bhpgnNp3a+R4U1qJcbGKgZj34kfGnrmXHSf1eJnvsLEtuy9h3gHvU55ONDCVgIT2p1zQaWrsvtrB1BrFYPEXYy9llYWItYbdRrlo2bxg7dxgRQiLlnnhcVxeehmQ4tLPSTdcOESZd9KMWIIDs5dqmZUx0bGlje8g4fqvoTI1t3CDHx0EquyVhDlHmdPnosM7V7qvT0zZ9XKZFmvbpqoW/XuCMUx1hddZ4OauEZv+q99lnR0PYqcdwSxco9QOXbQF/dAC47URWqh5gYpHTJAquLnhwUYVkE/ya7lUjQYeAlYV41MWMEWk/E6Em4fY9GUmqIPlr6yIsPJbUXSlQqBdxYUKgSVUdNiUIDJXui3LnSh81txuK6feEnq7By0qAGNVrJojgCa0GJswalpLIUhJL1FnROMgmrUiQlHvegSkaUstgeu9IQsihIO06GYAqzKFWAkQTvBCLQipNBujXnxkJHTFlg1bTuHlBDzFiltCnzBoRw9xZM1bhRDEM1olhVEzR26Fst1MiuZuUCqyGIpZ7WxKS6RmGkg1isWsgIBWhq7YBZwqsIyaB2g1FGFiKZFm8J1WVkJ1zVaNJdhhqsCBACPUJFFDOmvzRstUpf+c1KxdTNwXoWfaDoKJJeQ1stLphFIA1VXAUlmxvYSuFOkoyGuzdsiW4MTH21pvM23dFNTTsvPpTRQahRIXAtAj4rpZVGp8y8uTt7DkLglBPQuXRkI5VBbERhBNa5dORD6z4U9nqFUVWzjIW1+d0QYdwwPtR8Ko1RzlBpWPP/IPWeRU6XQZITZUoy7pFWogxQEw/fzOi1asYijrqpxFjdiU1VbruNOpiASgeDDzWMV63DmOy4jsmvqhn0PANS+ylqnjLam1nUblIdRUNhpnBPz+DMKXIrZZwxSzdpzE2ObRYQsKjbReIaJjvTvYyekZl7UCZKt4i8Id9Qb/0tPHRcNT1GOSYU8xFurF01W7LpwyLB7N9LTZekNI9r9LFfICMl+K62MVTisq6WaYrn1FkVWHcxiYMKWGg+yiOgj/vuqbl+oqTiXRELbNOoT5+xzFAd94f9OaV+YQ3W6QGcPN+tb9b/0VilMEuzecs5nAPNajOR0KQlkCieR6rnd+N0NBaispZMrTlLKFsyIKwbJ63BLGi5El5Pu9LpsETxaZlEeSuNMUQueLkSK3N1+mM8UB17Zzykb/lkfBCYYMYT+cxjsukDFuE52orNGXyEOcrnmmS0POY4mFPYklFicvWgftYSuv5zh517qL9ic9bnOv5cVdwMj5bTHA0L0UmCGlGl4dgaEzgIEhh4tayYiDCHDpKARUE7lICF+cyudb6E4c9fvltb2MpuoNSZRZisCbg6FXow1bnECTQuiDt6sst2Mi+jNnMIf/pjGBOGlJpfPxHSZgF6+MREDI5mTeOvuy6MTLd/+MMfLlTGdNiivNY07pCsm1Y5WsJpJptSSS791ku23VuYdEWX/K+Y+w/+6EiWHvotcdgitZUiWmkU8PIFUxq/0U8P06p4aSLyQlUp5fXCDoOmUL0zVSNLK5Fs6yr3NzAx17p58shHPtLdFelVRDKj2wMe8ACO6ARC/6Sk2z5y6YE4iIm65CQ1PNPh2UIt0ppXLn1JL1WL1lM4Rihd4FmLEKVolKx4YCFWWF1Gj/zosSXBwsjLRzSQl4nw/1XKHCCW7J6DppSdGtqOBJOc6hCOrcHOLKjWEvjp+U9/ziejAdTiybzoMT/zpW17bnlRRgTUyF4luq/l39H5234aFi2eLKFYgqqZoa0vrRvIrH/Yriz9bbjx39piE8YRtTY52S0sYKwR3c3re2usVHyUVfiHakEB/9ftrpp5yGwkEAOpStFZS7mFZfJTC0WrpgY10lGACRmw3Ihj3tKIN+NvLzFXnDLSC1EzeCtsPxmwV5+w4bZ5+gtgo834XXJHkTKEWJ7KZXHpoVkLSo+bsi6NqAfpMuSUcN6+e19Wn7Qik7GhR6CuoW8qXTJtRNTKOVICqjIMQ3OZn28LFOhqISLWo7lN+drIHRXpLQWoCpoXj09sTFmTj8QveMELtJrhouRbBLhlip4ZXTW1hYLcTe0Qidhfvf0eJYWaMi3HWSYsmsOyzEtD/J3huLicFJqfIXCaCViAmkDFTM1NzcH4aZTWiQzONV/0pcM8MEeY6HV8FeF/lvNgDDFxOzZW9xLZ0GeuNICYGrgfy9Ux45jRjGO1nWF5GLHoNG5bshv5De/zZclyWVtd1TSKUxczwhigMW5bMZu5tKYBULIW62c9tCLoII31mFByX+0DVVZNY6lZzNBd5+EV/vBQtznFxKHcTu8AdqsaE67SzeNG7LHcMeW5PWbJ6qVpzOPmmlJG43KlwHGpQt51vn5qSk3fajMtZ+TVayYQOk0fsDEbDawNZOmTh3BAeU1sMUkxNaoOrlJq6mddXdZTFoslBPQgQtjMQnpLRzB1TNgXkp2rSzjoF7x0GoqEepxqvPXYWqmsaoqHilD0SdDkYu1GGCuuPj8eSMAp1U856r1uGRPMjwkU6FGcYBloKxdj81xneUYXsJy24rUWtQq16Jr73uuKsLA00tLWUp+clcmKA4wGFuPJyjQHdVKD6gvcK3EW4RiLXtPiyoAFhwU61Tf+123dsSImIHx0GQFlda9L5ib2ILHBh3/X09OY8RQeH0rAgr/hBZCcCq1+t7vdTYDW3GCqMN7xMfg8nn3iVvFmTYqSiVkwF6ZvNJFMy0nG1TRKCn/qzOT4yd/Wmf3l8rxpDSU+hPgWU+AImUc9X8R6HHvs0z0Wnk/dQBizW6hx8wwxPE9xBOnZIg/TixK5mhNzZIXGOOEA6Y0stQ3SuM+5UrQIhVWFKvhUESZ1DiSni9NojPOgo1r482FinVRT2lZ9WyUQfOonv1RwwTE33gLCECDcgwy8nEwldq4+IE2v87CAsVJgyGBkEnVVNS1rdBuefM1YYxY7/Uh2j4UDDJHYTempv8GoZ3LUxQu9S0nQR+1aw1HIWBcJuPR6psay24rrjoOPxZZGkYuenGftgifzcCxGwx4koEORIbDk+2lBJrEllyAF4YIvomAaGkxjIg+cCZkkaGgssETTRoYGd+zlbSX7oOSTYJWpRkZqtTZ5j1WoxGNN5YKCOTEM5mSwFsjADU/xDoEAcRYBJtUUrlYp6SesKovWEdnRIrK7iyW9CJTixLnEgBiVsJd1M2nCXkyIegJkqmbZQT7LEQehtrVyyWcJlJfYPj1VlpgQOxEgFWzihHg0sarj/o/iGKpAA7ulAKsQiNFbG04fGLXRtsOC9aoOhQV3VF/PtWBlz4WRBHEfu5RZtYf0RLjEVtSxg1ktsA/KdJmZ8JwFsbxUsjimj5Z11TwKslowDEGKusWquOp3UCtRdtxoxWDQoKeKiHJCob+s7B2tQA5C4HQSMFpy9Q3OgrZGD2MmDoYCUX7jmB4nwVmSscoXyjRiW4gbE0R4j70z0pwjQazJrr1ls5th3JBu0O65Q10kk8ZJA8hy1Yg1uJXYySw5z6iI0kGJip4nANn9Og6zRYXVqqXwzhxktLRQUE1SXZZ6+ahXffq8n24hWDwYw60c3CdYGa2QnptkbabiqtPqkalGE5klXKW8H0To3HJcZN8th5V1b00csAeLFmAZG3uwHiirG9Ps41gt2DNoIiwWAxWeoIb4uEbBc1wN+smtsnJQQQvU0tB61RZClsADIW1ZSQBNRhgqEbqGWbmYny6mUdwTItCcbrl1Mhz0aPpTyYLBAkY0gUpa3KrMT8uDDlStq6C8pmlVoPmR44MKQgHCSmePKItSIQN9h+VYzNg2L/G6oo/3vFozRTc5rN4tafQL66WVRbAWK16mIgJlKVJGbpy0KtNqvQl3krdqZ93OnxcnPdJmKjtTYZa6NskGtIlMP6lttaMvS2MwoU/dqJun3PCMBrKUcgdLWxiXcGCNG+aVjBp6EGNAaWLnJYSp2F9jiuHSbyV5WQeFaj79SKEWwxaN5d0s59rqqhpVeEXXQGllXn4N30H1GQ81Jmk0UA0XsuPQVxmDD80ZSZ/sA0gNU3xPV/UI7bvQKQQNbVE3NFkGW2mvs8YSbmHMP+V6mIPMBRsG0VqxvR4cSsACFHvsjc6YGhe4E4Z+LaH9TFfm0bIJ7SpCz7INXtVR2/plNERKbPcjZEKA7INDYshYICi7qJi2NChz6srPcSveSesnn3GKKjmiAEYlafhsFWq1A0qMTXDBoGZ+nRRnptFJDFtKqSdX9R/my0+mZJl410IafcxNddtHyTE0+MkoaVJiO+WklPrJgk2BQjZ9z9/ygm5MEJx5V6lcOHP76UMrY1x1adMwPYV7Jvu7ZKEzmb69kcteL2cMBGYd26L4kCZvt9CR56C6qlAjeBU0+R7r4lh71V4DHVhvtGKwUcIQJlelNDrDwjk3BSqdDfA2tUUnaPnSG7JZkbv91TnZj9v4EsvlEidcE7MlOzvkAplpeWasJcwPUDJ8cMXtF6gpnA5jFeZZnJHGACEKQA3lumsnlEMxZ6yNXDWUcLlVk9mT5jPKYf+W76IAYDpvSHLjS1yJKDSsliQQ4GO6ripIpbj0pDmv4diq3T3mAME1yovitXyLD4tIU6x9LsxMdpEpizDZxTi0IPlOkmOJSYHqgE4K9FDAeQIl6A+GQg8sUAfURtU9jaQMUtew4KggCIxECRwIIshLZ5bGQnSQ5YAFA1MXARS2rSlLPQEyxyIgRlh9X9xHTMpUXTDNE4rWBVxiUcIxzui29lwUBzbvhomgCd1Q6rrkIAROCYGLRpzhM68158S0WLv9LayNKrowT8asZFCyoFm3Turxgfi52D5jKLPZyqhiMDRZiEUa8frqsRwYmsxNhgLjtuBLDR0km3EEjo0qopyuuuSkIdRawoTLf+CbLSsgpW2PnBMT5XJi44/p1dAEl8StQ8s3QYs1cwlwA9YwVcNyJ9jqAHMDmhqJBPE0PLpiViWBv2HuVoRm7cCBwVxrGuRx0NamGDd+JAbBc/smBdMBVqWAnxY/NjBaKpBWm9WlRFgCmo/LDBOulhWFMdKaFKpljeRuOxmKaVXTSkmub/wJtx2VVq4aq43eY4KzOS5TLHufywGEPauRyciEZSe2NGYcEByo9bjQ52HqC9whNz+s61xiwCBgaAVlJprLH89IDAKG6mjim/cR86b7MWI9LMcUZuuryXSUsPNxV99Bd9JRGhPlNLJ/E73of93ww4QtmdatXugzpp8fMwxkuHAWGLV0maepM2rnlob9m9bSZXWTlBZsFirWSzqIiIYbb+OrcCeJd/u5jgNDtaRB3rLWEss9G/6eIiqgRlut3A1Hf4sZxuBjDayPM2D9XWLH6+yBm6PrWevKu7mjzpm05tHpJjbZ1SeQ2gxM+7JGup1NwEIbqZRbfWzACtwCuBZL1q74YGLQ6MGkdRgP9AujEC/POLAyJVNx+00T6wtHqqpShb3hj2WNxzqvYJMRz+jHbJj0eHXbY13SxKfDjl5ejagqRfjK2BwzUH1mYGBZaQb6FP/LgGy05AAKyVHMtGhysUo3hutEE1VNwfqmyYLLrGjEvAG0vNdJSj+x5Y5xoumvLBvejfDjKD1mYVq8KktlCvCJ7Fv3aqcxwbk9PpSABQoAaQYHhvKC4icL4Ef1rGZWENBi1rpQOY2NT2cwp/I9dM6612q+4TCvW051RksHtmIp5oazlQ1bNBXZAGbiVFYn6wPyzSKshAI6sPFUAEXHcKY178QOSOPyGXD1WE+TOmPcN07xIQ1k6jImpolam6gIN36xVKODfwPyk92PKVcecwJNJ2yRp0qyYI15V0UkXsjuksWWvqS3WJiafY0Ihlq26967+k7KcpWeKmuzALwiMnxvO8R0jHJTi4OKaNNJ3nU/ZSHEaFjrKk2pIbQ+mZWFkoJHoNWggLYEihNpnldN0S7Z69ErDKM2K9JjWY4NWjUQ1N4N8hWq1rYDLCisFO3lCYKJ4a2rUZ+37iw1WBorpbk2UlkJkDTcO8+KOn0fqIVLdvH0lC/kSVUNylBd8viG6IC2EwfR3CYwpoWkj7zkOPBdDVFgW7jRUJiAoz5O/4Y80RPtbngVC5BRLp2oOyAFlEsBoCYCGZuJgarCWGUGylJxNs8ZEFupgAWMDFunLk2MiUZkmkw6QutZB2Ym0UCdVGJP+tChzotYW04ZYcVirIbZsL0/1LDCYC1a2bFlpYCarmp1SD1zvKv0J1MaM6g1Gck1B0/Kzc8QOC8JGHD0DitO46eIoVFRqFHgwHhuwDdadu92oMs4o/vYSMhnMM6YK/V3XXsSZDTgGIssvIzbPDffhjtzioi5YdPoob9PeBqN9U0joYHdus3oceQydCJh/GlitbBWF0+u6fj2WtKBA+xRQTXleI9rVgXZR2AsMugJdBq1+Ku8a4Fyajsu/4R8wwWvydZOGhrPjY20NdjKJTrMkyREFUoTQ5m9mRy20sGQBYtn4OlAPXO0GxWjznWsLdwhqDuQNaydDQcyzdHK0mqqryKmTq1gS51IgTFf7VoHCxgtywy0jvalak2p5avzvqyhexnAQpwx9RtaPZ0nwERPmxnRUKKxvVdcLMQOODyZELbGWItshfKmuFIAIjMPyrAHzVcLHpwFNXq0b4W3OgCfgbFJjVg3hIz/WscUbKXEsKndAjkVrF0Mi+YmCxraOkrz8k5ZRadUKU6mCc5VD296B4p5k+VYY/Af2EmnxMF5Lp91IFMhU3ejACNRWW2EZyfuA5T0UJR85DKFjaV3ss0PFGqe9bF4sJvS5C5MwEvU6IJQUI8+jK6qUOZt8yOTkICF8NacHLXFlnWpvuzmX0syibUyU1cEIbWYLCXxsSHUSsCUDbLVFFaiFW7haBo2udJjl8ZaRd2pB6y+c5b2oCz2oK8VB1WwtOD48TwtpVRBZSmMj4rYN01tARr0jBLyOs8+3SDR5VlvNwqzp7921xEMj9xCpRgxZOwV4LyxdEZLdEMHgDyFeQJrJ34pUxS2A80CkiUzTg2nS3q8F/B5LjqzOp2I8Rj0GM88zeZnjA/MwJpQWXAJUvjGQSms2vpfo9SqWGPxjc0j7IQXplJGEp1dE8vuNpIVWo+TowKGGoaBs3Gpp54xgWOdhQWaubSXj3CSBsKBs6AbWr9NJNNQodITSz1FU3Uic/OfpBnxRHXNIxqaNHOH5nN7T/BIu+gXYw9qyRQwA+rOpoPJdFlpjJ+GFwMdsxEpMFZraFbkWKHMrJyFFujAefOOfqFesptqe1vxmKyOWYKRxKxUzedY3nUojAnEkikxzU0fJqZe/8+Fn/CZAwpYrKy59hjDSywSyppNJ+l1S6FKfcMdY0OwoU2rO+lgknL8SZSBRmiDZVd204mMRk95WeGYuI6lNwq4GcKkLM5MfjqSsW/lwCGL7kSaSVHvYt9smpLmb4Y4F85j53qZVu1RV3HK68DcSEP/ylpPJOiZBlOzo8WHLm1lablmkAVtknL+U38zPymakrAbKKlq0JlPD1qBq8+UzUnub+tOFjSlJ/dvLnnDM6iOHQNP6PRM2Ut/A9m4tpDAGVgqzaQU0sbFsVZTESl9yl81xo3ji6LRq+DORFT/ZA81mfWZ+YGhfBw3Jzqb3lxV0DzjyjPqOJaoUoVCLaQ3v1otmfKtQoSoNDf9XTqyuUEDgQSLBpC7aMWZGg1/RFUt1ikwt0bjuBmaShPPnxmzQHObUkox1e+IhpN+Ol81ak0mBxIYcAkxsmu4vqpNTfOmLj3RSROJ0lmm5YjWF9hWtOUCrQzTvAUTqodHlF7FaSzLFH2kaLTYHITA+U3AZGRvkWWinlVDqJWf1adja02OqI7WBMyJ7rToOGY9Gwqq75jUPFo1mSJNhVxi62nLdNn1L98yEssVt2vAc2qG4pbswHRj/VQOiTmIwzBe3faYbnSwsrSdweBArDOUMXJaLwo3j8Mp4UKWtvUZuNxOsHXLYGjEkMsSXKTYPNgKmOLpKY5vHSkBbsT6FgGx7Y7v2ilV1mBlBUmNUQdzgWWuewB4duI+MIAbo2hLJTHZcdnTabY6MIDzkE0NXAi3Gb23iGJahE8ueNELVic5JLRVccOgJq72VZZLauozzhHOW3a7iWJDIhdOehDk1b4CWHU3vvQ0tFohGJzJqaDwKFk4aWIJlcvymlsii1GauyvkVOd3/rbgpioXGn8KkMx5qJdqmRfssrQjtYUrVAOxSR6sOqq7VqYDU6dwJ6sDqzL2zF3nl4rgkEw+x5JAGTux8+ZlboBO1/aAGH0kFvEZFyqdiz1oF8koyXQ7dtYJtj2wxHUfTv+tZRWtrPGs98hRQUBs7G2Z+rV+YS3K4B1oYvavvt73NJnfVY2NqRpjULsyBsItBZEcXWUnzb86BW+/OcBrGWYxLOJjsdEK9IGliH6hdAYG18q+04k3ObCKcLe5tC17YKW8ZceWsuyh9quyW3ZoIUFtQ4r2laDkO2M8mWurT6myh38FuaylJUODI8p4xgVPKymB9Zt20dmNuhL3pT5QcQprBWECDSeNLswqrNMMOzr4PJcE1IbaJZ1dmGAy6LXwTQ4owA65FQq1gnJDaOTAhrVLy3HJakp7URgEreyMjLqDIKwbbCu7MxswPhguDCxjILXFOlApkR1ukXWmn9CRrFHEC1RTB3EXeTIZyWLE1v0lMK2cZeiTECtPQSJ+oluboroqRQ2lGLE5bnSQZtS5jgWYAEGJMwXXPIEzNDcmW3iLfRh2ahoijUVxteb+grEdK1MPZaihU4yB+EkRnCaRIxbIpA25+q9l/yRN/9QFiDIsSMxsxHMnVDvlOTk49IAFizc0bIIGWdOSacZH79IBbOQzKnn5hZXHSksitvqeWVYjSS8GYfBli0LsXmogtMksJqWLBdivaMzV6rqBu+XWdvZEGN0mKfunuIOPLNIwPv2fIdbOn05TmoiVeEGG6LugBkOnj2ilPmkQXHlbRlc3HJQQEjzpUHtDVMcAYYJxUiBfp+qC1h2ohR6FHjcPTCMOIfMbIJWdZ2g8oqcOQ0/agkZPpQOyrojxvHluopU20tydpoCMP/XSceU0SdApHbgk8brRwRBsoNHPR6twskmOovpY4rH0Pj8eqBE5nYwajucT21jumH1yXNlbmqtjlQ0owt5WS6BpKf6DUcnsbvE0JpvI9FPpqo8/AqNwl+jPopz0IcQHw4VGGYWjRyWLjzG9BIAocVybThIoZZSz7phi5NN5zC7vKN/Eb9pwG4dZ6rlmOIN170OW3WAiwMEPqUIpZqxnKtCtKzfnQ+D8I2DhaC+DNeI4FukUfhrbx7iwuhsNdCJdzwgvMqgDmiwmm7MKkbGOT14R/FGyAceKzSRI1ASm5bgpVWLLQXvixt49SbnJT96dRa17X5wQrq/VsxItuayD+SErowC0ss9cGIJ7ZpVvcJCdjzGOCbTiPBse3SuzArZwp4yxzkTJnZtM5aZ43hdNLELo4D4VdALiJn0b4nqrwlgdfASPxE2kVK7AzVlyKOFW0vaxK1EoSqOAbNHirqwFT7eO0Y/+amFZMimUPRj/OTwTe5DM8prLJBTCtzcyqx2f013l0XthY3bn8cYVMVa2jtGYuL7OK5E9cOEcU9tgvuHyby6/z2gONimE5EzX2rGy8LHi6pR14Ca5JxaBsow0S4oUMEtryHktmJZewOYtfsR6YJGXGzkJuqEnUoaDNRXjYZNamXlw5nkjKyMRLM2yim+mUKs4jvq89InaR/6kgKZUtM+YGIdayo4nHauLreOCj0YJk7vm1oPcPBs1IYotMRIGxoB1H9LYgL7sLuAkxKNBxQR5RKIbYkZqV33T2ALvSr+IND6ntlOoMedY+oWC8Kxlw1hlfdDawLK5TjI8UUhVLo93kpIvJ1gwopDAIkdFSBb8tRKDRdRmHuJpUUpkkDqC9RvafX48MHBZVDMw26N0YQ1hgMKQTa7bjKY/Ml2JKWAwH2Opo+QNjwmhoa5t5B+7j+z0Nwbi0Ks7fc1IwgA4EYY+4yQLcVLtmLpqritU39ETRW2MqCvTkAOmuACxoxoshIY8lzG4XBIMvIyHDlqcKc57+sqCFk5aUnLEvPVfR2bqOIsCVFuAsDImRT1NRnNMeEaj5pOCwOFXMnKhdkME82OKzK8NcpIeUncR9Eoy9UpD5SRB/yRKBNxP0TEBLGazMkJa6VVHC4LJ3hiPjAs6dxEndvA2//DEijyyoAkgTX5kFuO7IBYDEuPXHmxUjxVEEIHT1RnT3JpLprIYhziC+cO7AHxsiTGe8sZ1OSEMNjGWThlLFl49E2G7vB1XOULuM+i9Y8rxmHBTBYHiZ0Y6QwnzmkQ9aaIWAr26rr5tIjRQWkO4MyC2KoAiYCENBQyILVwY3tBv3PTRhSwgTLFiNAzdMCGZDZnUmyDt7OOB9LSywU8FhfrkEq1YadlmGorVbG0gqxC4BR/U4q9jwGIsFx8V7BL1B6pSu8+czAGVVMoYZ6VFgTYM062KrJw1lxUbK2VMx21ctMm7iQEvFzG/avjWRoZOpuXZYGZfw6VWGPWpjKrs00Low8ZA0F8o7GdfZXICdiAYBxfsuUWNB0ga7Eggsx0DQiy8FFfbInZGIaOp0XpC32HzZdtK14JuJijakstP5qRjWmOJ9FkIcgD0u4o51g4ai0v3eytxKS+7HjSPS45Vy3EInGcEOA+8ss0rZbTnmfhYL9YadGVeayMraZ+VV+cnq//aDGjMFBGwsJun2faMNZ/nKOWyDODqWEybaum8IIfn7A+GTKxqR5N5iFle4w8fzIfORiEjkiGlV+oT4UbCejuSSdnHACix70my/mkIsi/M0E0gJ38coDrNbgfUdtfXx+xmnKfGXI7Rz07J+fmFM+piaPWhOW4Is5BJevMI791ncn7hp/bCwcRkgubHasqFxBteKqSobpheMs4DL9HKUFuvJNaiTLtWaz4mPgTQ7kvjgQa1k8Kn7QGcObHOYhUh4sbjMr8fuU24cy0faKNtm4Ov60NnTte6pZEq25rhQ2fdR7+gcy+rJipxR21hcJLZqJ2mIXZhEci0cNCRdUnGtu72+6SU5Z86uNW1z3IyV4WKmMGRycYE7LZGCfagditHkk6vEwn81SOu6wYHQoRpfIC18tEQ9O/1T4saD8TOOOpW6XxawtfZ5Jhl+VirebXZcpq+KghYnhQF2IN6MTxYOsH8QEcQiSgOCwO15nALeZ593RnLP6tZg57IqR66YGbrJEzOE2Uda2eiZa2qMU7tu9wWsoiVuLPoQFNOBE5+iiZ4FYUxR+/Qg5YbzlRrZPCZCFn5k+Saj1ZeHU/SU2Tn7IM7o8xjPD5pd/FI1c3ZPkcmGxNArI3daha+davfJTZkaBPs1LfNOgsCGTFP1VZVTr7hQF5+jr1DBgizpi43FuSYKBO/DmYsqGiFkyIR3B49baFLCDfoyVx6OyYsFoV4J5LVwgguCKIW5mxXzZRi8GYCl9TCGbOjAasC3n7SUCjXHYnq5NLUyC7uUL3IGbEV1r+sW2miFAFOlm1zrJ0pJLhnUpcm35Zrbkn53wq7HF1yA0Ht+Mytp5OGV73at2Njlu4nV905cUYFhUWkd3zyH944d91YpqZVOvI21Fg3LwyXcz2NwqpgWNQQrjJC7auaJ1AvRVhGUJi5ihBVtIJliohZN7DD0RTZTDXEWAUNreFEc0X66rw0NiZoI/OTcXmh14xy+tjwap0nWsEmO9ihc1GJeoK1nXKHA7rpDtavwjT29bQE92aF5Cx63Catk+5u2WwioOaBQBV3b63mCcEO/U4cUx07u3uquptJQvjMSf1dApN9NagzOhc+NTL4aT2tRDqQ3EJyEAIHSMAQ4XPsiulry0u0rUo0WupxBisevulmeV27lWSJ6Wl4NMptOKor3Six7GMQa6UoIEvhIxegEhsV6WDGWeeQVKVM3O6aOLYot8BdTlxZtv3GYdn33lZgpeedWtgs+N5biTWp4WD4NdRbIx2X2K106MQWLZsTk3LZwSixbQ/LVbMgwcF8xB4s5zY04Nb8eA/ovC5aMRakO1S/WBetGBMzm+qb40JlTFDHCJh/9Q5rErcilqHNs5/DM+zhyJGEeqpvPNmkvxvMDSOgLQ+/VkpWpNZdFl3cToPJuYJAgRr6NhnVcWA/x2jnxYFfJlxiJDmW0GeTpK3h1BSw3BaVXsNp4k0mi0ovsWlok8Gk9Tk9BxccTlW1k0YyUttNwMSNUHRjdhMNnemTdexb3+Co2OYglMVZ4plwR22vIM12x5UDR+c1yPrwXf2jhP0CDIsX5961k3MvS48SrmOv3DAlKsjTPrZy8BUNOoLBdpOuHNz5h3wn936FP0UTx+2mrYnwils9Yi4esfMgE6ead+RdR2iIc+OgaN2Px+UZYxLo6U1gshcil+jD4QTB/QT+s+AI7052fhffzL6pQtpZqugmrHS7v9TdGdtS1t3v0lcFa9zEpqe9r37yD704QwuWniriI5yhvgIZuh9t7Y/1tIvApEaxEcNViq3TpPVcSNBpSv+xLuNxXe3EzMNccrvb3TDTCRYAADVjSURBVE5sSLwWLj+1psjO8nA5l8kA5OWfMxU3qZiQvTBdXJc4P9OV6jR9ZixlPG4hdVItLBP1EeQ9NO7FXZpYuESjME4eNTcAcybBnj2qauuN254utUwRPSsAbf2gBz1IIzI2yWwsMgSzT83Hl+jEXXorPJ6pY53X5iYk7fKwsBDDss7QBxmeMHDvu5nLnJ8ZhddV35Y4NjMLDnriw0/6i9ewOvE79zS6q9b8xOx1NGmoUdLgEmWnjDd01rBgUvf4jHWh24+aUjLdzX5ydfcnrBWyUZZXhJBf8Wmd3VuXiPLApO9RzxyHwCEQqCCFULW+bPw3hpvUGPMh6DbXQXTVKGHMsaasGX+e5jScwcF4a+SxSLBUOA1VXllHoQorBHOW+aLWEiuTnfcnOeq1ULHLdVwrnvcVn1QQBzdOTP3sYfLg1SRlfjYByxvcDCPW3psEjzrjeXaAgztMnCYcNo8XnGcQzrPqHFDAgrtoVOIeeFCWs+EefjmQ420ix/WpZnBcBzwxXpZ4gX8J8c0TtgIw4nPSLNdcnTRbC+H5cLTcZeXv8a6FPCS22nNSyGD+BgcZ3QgSDuByuzHLMXPGXjXuPT+NGyOj9zBNivPTwEGal7WolI21Y0i1akETRfOduJoeCOT9SmPTkby2itgu5cAOCAk4UUISrkpPFI+LwrKLF9iLxQOnmyc7nOFTeXiSIyoIwj93z7lQVIkEOuhjP/VqvqVlLnQ2d5gnnJx/4OXi2uqvFJLVqO7qw2Jbr/TiJmYXaogBuWQToMeiRCi8xYPLRzE7JKWU13HLHzVx8mLV3k69TtkHlaZ+To5LwjylEqUUsDCcaXH/3kJ/MSamQrdJrkl2GfuMAw1KjveGaHdC0HMzpO7PlzKT9C18PF/H1S4lvK/2wVhoCdFABmIPWj/iEY/weichM2dMUf4Ejo3ZdCCkpWrcFR+cPQchbCcq0TpYHNsjY0D3ogcVZ05aCgfPPNdLHzrlpPSF86IDsnuxttIFpyw1LECFRRjAOltakFbljhBYu/CEIAVjFqOsnSN6h4qwyU5vGOGhSWnJO26u1onsldB9BB1kp5tWk91O3cquu9lqoQvXBgqmIhCpQ/ElSjibIVaybbefVPZ8h8C+CejXom+M1qQgmlk2fLABC93Twwjire4km7/2Dedg5btVIHou0Oym6DgXHKzCe1LMysHgzG49uX2afQwcTNl6sZj7abYHt4K8RN+aSr8wWe/J6s4nsdZLlmH+KckzKdbw51PVtqoLDpwye1IcrHsNxFYCk/gQCJzxvMA6PTbZ7rIu727nbQrw/gjDkwWWkZpvoNfZZ957FizC3CPlXNkB7ltKd1nt9mGXSnTMN7OFjBxZrNt03c47qsQ3I4fXQQ7XxSVhAjsXrBhMD0bJ2kyliDFXH9OKm6d0N9ittDjneoUog5sDnNi6W9uJ+6C2O3Isx00fdFA0v8jWDDeHJXbjVy3c7OVQ8TDJN+5YhpYcVeNeyuKqu/pFCRYVERMh3NMWgh3Ksgby3Ap/FRAviaGqYAQNCy/nVi5BBNOA/tz+npdoeDGYPRH8uuVbXlw7etKEd2eTBSH07M0stqWJHCkCSTpQ3p4XjSswxK5sVKOPOpqYOd6SVZhJ4mbu4QIxEduuqMFFtEFD00jQqnI+SRCUARwWmqsLtr7V0VXlUqy5SaCZgCIBdh8qWRM4yd6s7N1F56zytFW/cvU3ngxG7TTTOHHyYDWHjWeaw50Q6jFaypSezmtN6rGoEqU4hWq4diGcwUpzOONmIw58ew1HH2xZmuPuieILXpzDGNSCGgr1zm0BKU2gsnQjRAKsFOFmHZiEqLjS671EmkBnYVSlD1ectcBYIXllkQyIq2SKhamgk7BU+lHDdQspRWCi4uxZ39TW3Qp6KJk2CvZdIxarlTWWM/M9CyrIepmHqlUX0Gpqp45eQaJ3qLUoXvMpJWmuyjRHftKUiqMbyDQhkLXoQd251E73ARYEw0I1ATtEVW8iXD+1mGY/MrYdVqHrvslcdynnQ2AHAhNrn0swWDFv1usS2+7BZ54yZ0IgBEIgBEIgBELgJAnstjA+rIDFSfJKWSsJ+EsR7xmyB96TAuW4rkx2iT7JlRWOEarz92MiBVUXGxNsmRHT8Q9wFcO6RNcxyh8Igd3G5QNRPmocIIEjAxYHqHNUCoEQCIEQCIEQCAEEdlsYr95BEKCnjYAtDJ7XcPPfn5K4nV5v+jxfIQjE2ILhxaLu0vtraFtP3ZD3lI279x6lTrTifG331CsEQiAEQiAEQiAEQiAEQuCSRSABi0tWe+1LW08E+JsV/9zh9p19B7bE76ukA5Dr2Rkv+7DV3zs4vDKTRp4UEKfw8pF6B8cB6BgVQiAEQiAEQiAEQiAEQiAEQuC0E8gjIafdAqr+dlh4B4fXUnjs36sKT8O7hW2v8NYSr3gQrPGmA69C8E8TG76YIEYTAhsS2G3n24bCk+wUEsgjIaew0VPlEAiBEAiBEDg/COy2ME7A4vxo/dQiBELgEAnsNi4fYk2i02EQSMDiMNohWoRACIRACIRACGxNYLeF8fT/PrcuNhlCIARCIARCIARCIARCIARCIARCIARC4LgJ5B0Wx0008kIgBEIgBEIgBLYnUP/GKt/5+h9V2yM5Bzm81MlfSivYM5JpiHPQACkyBEIgBELg7Qlkh8Xb88ivEAiBEAiBEDgdBLim/h3pLW95i4MOFpyrqnudkHchv/rVr/aCoXKYz5Uml+hytaO/7oYRTEi3rQtL8Ppt75/2amp/HLZt9qQPgRAIgRAIgWMnkHdYHDvSCAyBEAiB/yWw26N6wRcCIRACIRACIRACIRACIYBAdljEDEIgBEIgBEIgBEIgBEIgBEIgBEIgBA6OQAIWB9ckUSgEQiAEQiAEQiAEQiAEQiAEQiAEQiABi9hACIRACIRACIRACIRACIRACIRACITAwRFIwOLgmiQKhUAIhEAIhEAIhEAIhEAIhEAIhEAIJGARGwiBEAiBEAiBEAiBEAiBEAiBEAiBEDg4AhcsaOTfzhau5lIIhEAIhMBKAv5Z8MyZMysv5WQIhEAIhEAIhEAIhEAIhMCGBJYCFvkj9A0hJlkIhEAIjAREK8QsxjM5DoEQCIEQCIEQCIEQCIEQ2JZAHgnZlljSh0AIhEAIhEAIhEAIhEAIhEAIhEAI7J1AAhZ7R5wCQiAEQiAEQiAEQiAEQiAEQiAEQiAEtiWQgMW2xJI+BEIgBEIgBEIgBEIgBEIgBEIgBEJg7wQSsNg74hQQAiEQAiEQAiEQAiEQAiEQAiEQAiGwLYEELLYllvQhEAIhEAIhEAIhEAIhEAIhEAIhEAJ7J5CAxd4Rp4AQCIEQCIEQCIEQCIEQCIEQCIEQCIFtCSRgsS2xpA+BEAiBEAiBEAiBEAiBEAiBEAiBENg7gQQs9o44BYRACIRACIRACIRACIRACIRACIRACGxLIAGLbYklfQiEQAiEQAiEQAiEQAiEQAiEQAiEwN4JJGCxd8QpIARCIARCIARCIARCIARCIARCIARCYFsCxx+wOHPmzLZKHGN6pZ9bBY63LscobaWo3VhdzPgkWnkr9U5MKyRPoKwji1hOsHx1pTHs9eSh6bPXykZ4CIRACIRACIRACIRACITAsRC44FikTIRwTt761rdOTu7pp7JI7uL++7//2/GlLnWpOr+nQk9GbFfqZIrbvJQ9QZ40JX0Q2NyW3vKWt0is6TevyM4pi8ClL33pnSUcmbFaf6H6y63gqiJOhsaRdZHgBIhtosYkzdzkJgnyMwRCIARCIARCIARCIARC4BwSuPT97ne/dcVv64/xjn71V3/1+77v+wj8oA/6oP/5n/9ZJ/kYzyvFpzxVTtFP//RP/9iP/di7v/u7v8/7vI/zx1jQSYrie//Mz/zMT/7kT/7fiz/7iFxorD/6oz/67u/+7n//93//4A/+4M2LePOb3/z85z//J37iJ97zPd+TdptnPBKg9tKCmrJa8/d///ef8pSn/Nu//dsHfuAHOrOQXV3+/M///Hu/93tf85rXXP3qV9/Wbhckzy/R5E1vetOP//iPv/CFL7zSla50xSte8RgJVHGK+K//+q/nXvwB+T3e4z3mRQDFQp75zGf+v4s/YwLZQfvBH/zBl73sZVe96lXf9V3fdbw6r9G+z9CHzSCmQu///u9/+ctf/tzqM9b3orHj4tGDkuP5sz9ugVrq7KVFQgiEQAiEQAiEQAiEQAicTgLHeTua3/jyl7/8UY961Etf+tK9Oo3VVFwCruP3fM/3fPM3f/Pf/M3fXHDBBXyDX/7lX/6BH/iBV77ylSegwJ4sRr1U5Jd+6ZdUjR+O6j4KUspf/uVfPuEJT0Bs8yLkEkzRvj/0Qz/0V3/1V5tnXK4CsZxYIYAHPvCBYl7EOqMRxVN+/ud/vlzKBQkS/93f/d0P//APS1z7LBYSn+UlZf3Hf/zHz/7szz71qU9V6HERGLVShFooggH8xV/8xbwICTD5lV/5FVGJV73qVZMErr7+9a9/znOeI5zxr//6r36Owk/+uKqjaTTQ3//9359zfYoANYRRBLm+6Zu+iSVfcoeLk2/QlBgCIRACIRACIRACIRACJ0bgOJ1hTtRHf/RHP+ABD7jhDW/I4+o68A34Az7liPZ5By751IGr8wSV2Pm5BBndiH7Ri17k5u1rX/taCSR+h3d4h3d8x3d07GrlWimzr5ZWVUp9u+Tj2PeChJVZFtK3tCqximghftaZkuBYRd7pnd6pKtWKTeoimTP1qexzgc7P6yiZ8+Rf7nKXu8IVrjDKl3hl+pbsYDfIo4aO+1P6E/s7v/M7z3rWs/7sz/7MGT+pQcPLXOYyY9FyuVoaOu5LTmr3SrwyQRXX6eugpI1yxgR19SIcb2+6zitIcQpyPE/QQlpCpezzDlzyGc9MTipipQG0qG6FiZCS838u/lQppeG8uEq5Uv/KOJHsZJdel+qMk5Pzk4x+jsQkLqTzZM60TAfzBHW1sk8S+FlnfHcRdWalHOOV0YPJ/dM//ROB8zQ5EwIhEAIhEAIhEAIhEAIhcG4JHOc7LDgA1772tT/swz7M6r82Ql/kQJw584Y3vEFAwX1pvrEN4a5Kqdq+//M//9NPvp8Dadxmt8eeq1UJpCkJtrj/y7/8i6vv8i7vYod8SVDEG9/4Rmn8JNynUXJXREz+9m//llglcsvJ6Y3orop08FJk5/XR6rKXvawSK4H7rvLyFUlT6Ote9zoPmPiMErogB3KRRiZR0vvIqxZ+jrWQ0u1uVx0oTqGyVAISbBUpDtIoUQLFjaX4STEfB+T79pFAYh8AYWmBzqs4PlLK4kGJd37nd54/WcCH9LxA1ZQ0amBCWjGBmpxiMmpSx9IrDii7DJBfCZkCBLrbT6AmwHCEDBq1SfvHf/xHomhImm0yFNYubGBeqGRkQiQBge/2bu/WAlsrikmgXMK1gjpK4wOIS8T6bsl0UJxCJeuTLcrBP//zP5Om3DKSMa+rzsvOzGiFgAo62cRcJZ9Ve+im+FPJ1UqgxR3QR7IqkRBKUqaw1Mn+VrQPUXpTdSI/++q6A8IVVPsaVKEeDykFZHEVSRqqBQ0lUDQ14NKm5Ps5ljLBJbvEEFFbc4ydaEEfQuijRMVpQSlbH2X5UIlMZCSobVMtrRKAoFHopn3pQNtKQA0m5LxcRgwfNoyVXF1Ei5ILSd/6HUQ+REnZCXIQAiEQAiEQAiEQAiEQAiFwzgkcZ8DC0t8+dhu/P/3TP/12t7sdZ4b/8OIXv/hHf/RH//qv/5oLxGe+/vWv//mf//nv/d7vzYWw5//xj3/8Va5ylQ/5kA+xS8LGbDj8vPOd7/xRH/VR5WPwXtwCfcELXvAP//APBPJwrnWta93xjnf80A/9UO84+NZv/dY//dM/5ag87GEPu/GNbyxjeR1EPeQhD/FUBb9IoZ/0SZ+k0H6Y//d+7/co6ZsvzVN9r/d6r5vf/Oa3utWtuDeKs9X/t3/7t29961v/1m/9ll330vB5PvETP/FOd7pTuWRjmymOGh6s8BoIbzSgKj3JoR5lnOQRScO/etrTnmZXPEdavXh317nOddRCZUl79atf/YhHPOLKV77yR3zER/zIj/yIoIZdKpz8KogTBayd/x4Q8K2aMlKbn09VGkrP27za1a52+9vf/rrXva4SAfFcjAp+5md+5kte8hJPcNzmNrf50i/9UjRaeWrwCala4Q/SPOUhMWmEU0YjwuK4GqIz9sEf//Efa26UtCyGn/qpn/pZn/VZBVmV/+RP/oR6rnIvOZDetEBzavDqWYW3YDzvec+75S1vqflYiDeeEPsbv/EbmhgBubxaRa4uqzxJqF316g3NxJv9yI/8yDvc4Q5ULQ2l4YIq1HtMVAcTdvV5n/d5ImiiKt/xHd/h5F3veteP//iP5zNLTG2UvOhBW9OcVmNxAjdak56aTHVY7E1velPJEJOs9PmDP/gDaV7xildgjsDNbnYzZl8NRyVXPbKhFXjOsFzjGtegLZ1JI/yxj30syV/2ZV/mNRNlJL/5m7/pERiWT8mS3/rIwq70I8/LMEgm/bEf+7GMapKs0/fBr/3ar+kF2oIEb3WhPyUdSwA1UB4b0TcZjHpphdve9raf8AmfIKDwxCc+ETTqsajC5ZsCeiKj+uzP/mzZ7YhxRnPw9sUOPuZjPsZ5B6rTCkwOfvd3f1cWTEhDjAEwMy1VBJjKs5/9bO/mQIZx6h0UVlMK46myjPMZz3gGgxHRYLds/nM/93MFSV2lj0u/8Au/QAfP0bBM2Bnb9a53PTwRG7UikNrf8i3fwvy0u97HKr7kS76kYmoTnfMzBEIgBEIgBEIgBEIgBELgXBF4m0949hrwKLgKXq13zWtek4/NJ+HOPfKRj+TPcBo5GHb7c8l8e278fd/3fXlc/G3utIzcvA/4gA/gKXnTpO+HP/zh3Ce+hEfxBSO4NCRwnsn3Tk1+O39PLkWUs+qgjp1U3Pd///fzSTg8HMU//MM/5Fk5EHGglVgG4dxUgQ968pE4nCIUyuLccnv44bwyWXhHdFC0Y2lo+AVf8AVzSnynn/u5nxOM4PKJRHDDFMGv5gsJmnBT6SNa4dUerqoFDUVqvJrUxocLL7yQ4839po+KiNqQhoNSJKuyVMSbLDhX3Msb3ehGPCv3kMU4HvrQh0ItSuKdlG6S89Yoef/73190hm+m1mrBPwSz7mPPNecTukRtfj4HlXfNp1VlcQ0hA/4zzTmERXjMTiVtJ9iEp5dcYqsgWfiZ9773vTUT71p9eZ6uitqQw0clkOS73/3uRHl9BmgswctHhIG0FPLlUjqophxLRIN8tUOVQF4xCbx3JL/u674OAYmlYUtICi6IYvDDmQpfXXP7qY5eFColv1pKVQBNuwDOoZ2URQHhGzEOjq4quEr/X//1X2ct97jHPaosGSUgRwKxD1dFKCgmIiBBtQWvmI1RWFtrLCe//uu//lM+5VMYm+rQUBytGto3aIILmmN0rassquKpibWXBgLt0Y9+tKKhlmDlx1VbP0T0pFFr3jtnHg3yP/mTP5kC6LFPteDwc9SFJ0RnmA1cFFZT9iO88uEf/uF08xHuEd0AXLxMLMmrTx70oAdpQRVEiYkSqO+ItekCGnGiFX2EadSC1akCwggAQrEv+qIvqquPe9zjvGa1gjsUoA+Z2vfTPu3TWBoF6CaiAbIoj4wVLfrar/1aSJVIGUZliICLJWOlOro2Tb7yK79SFVolxyDToc6g4dNXcxACIRACIRACIRACIRACIXAgBI4zYKFKPBmBCb49l4Dn8OQnP9nNWy6Hm9gcFR4dl8Nz45ycr/7qr+aEOMmt4kHd61734oRwR3l03Co32/mBnG0+J4f5G7/xG+2A4NVIcN/73teddq7RDW5wA9K+6qu+SnpukjuxPBB+iA+X/mu+5mu4MfLysgRN3M//jM/4DJ6V27MUcGv3wQ9+MG+fL+2ePL+Oa+T+vyI4eOXAcI85nxwh4Y8nPelJdh+430vCxBmTRXH8YZ6wSvlbB7opkUAepp0CXEFumGiFG7l2aiDDiaIwb437R21nioN9GWrqvrEoBoXxhAhGbxWls/0O4PDEuP0k8yfFJpSIm9iKzQLeIGgXBv8Tf7WQTO2+4iu+QqG0avesLA+l93u/9/uGb/gGAhVBGj/z277t29xR536LEwmmeAsmaBp0ErPwEyJ+I/jeV0LUT/3UT2HIgbSNwj1tzUfgx33cx2kgfwxBkxIoPuUGOPe4LIQbL0ikLRQtMPSYxzzG7XdxJS4xpOVq0hYf3qnaCVTd7eIPCTxk3q8gDlzaWhpaaRoK20tCN+4r4FpNVEJT0lNiTrK4ABoSsyI+MJ/cbhdVKCy+NSiPV400CiNRI1fl9UJQ37axaBTJGLbQ0n3ucx/tjjP1fDSTRgFHvEO0woYF/O0uUZAQlY80GqjMjHwHXW51B2T6TB1QVTgMWz2C8dMWDT1LUGyeeMyrHVkUDe00EZhgk7x9QGgoRiZ8I+xFvS/+4i8Gn4ZCYOxK5MU2KKExmxQEgESs2DwdVIe5CvPZgiEjSxOYk1cUT4iBzbNSIQa1c6aaY1TGMSx6nCqQj54aCTvq4OyThtCpkViJxrLVyEYS8TsJhDhVmZUKZdLZW3KMJ5KBIMSmY6KqEZmEwQdDobR73vOeuqouQDizFMNiday9e64DEtibYUdQQyfVDeUdzWCifH6GQAiEQAiEQAiEQAiEQAicPIG3+UvHXjZvh4fDURQIcBedO8Gv8KAEB5jfyCfkrfEQeI82Y9sJ794vv4X7x5nhPtFHAo6Tfem+y0v0dIaPS27AOsNTIpZ35IDYqgKZQhU8FjECvhaH0wGBvEqXeD5ua7up7oDfwqvhLfsWceBQlQSSRQe4agIH1FMFDrDtAzzASjD5LrGcNy4l349PVU+g2JAvlMD39riEO/M2R1BVXlpRSTUVWmdIUJaa2iHPlaoYgUsAVrSCVy9aYacAncVxOJNuILs1zZcj33YVTj56Yjf2g2DCw5Sdd00r7h/9nRnV9hM0wQX7EZARU6ADZ08dVcE9beXKXuqNGetYEbe4xS1EB7SsunhMQO14xaIw5CiOPl/4hV/o3r6f/GqQVUp9FVQyKcBL5DDTQb0ow4F3STLH7ck748Or5HaqiCprOGk4xorgpoKsccuWcLCDw34NTCT2CAajAkTbaRShE341pBJTQ0RJxXnvhEzguKp1nLQpQBr6i6kJXrBeplKJGYlGEdKibRmJFhGCYUUCQG71U0N0hbb0V0EmZ7uNKIlQizNzpCvPUFWjcOYB97wJw6YtqiSzk/bA53kpSTFZhI00KHedGTuj36kaBWz2wUo3gYgc7ajVnBfL0GTiVnQW9BGnKFy/+Iu/qGp6kw4olmQziDSsuoJNjtm8FhQQ1Mor9XGVnegL1PCHuHSTS+yD0coiPEFnlAQitS+xOqBG1GSggSBaAT6djRXal92Wzdv8Ig0+CqW/aoqYaBG9zLFGF/uQfcJcelXWss7TB4RJgnkVciYEQiAEQiAEQiAEQiAEQuCECRzzDovWngvEFXFX35ZyjhwfySUneXHusvLr3CDlCHFROJlco9ocwWfgyTjpp2/Hbp7b/G83u297Meyw4L1wV6SUgGflm+Q+cMyTdOubd8T3duzAd5UuMZePn8yJdYuYhu4SEyj8QRlpfIji4PEt5eK4+uaQO+PYpblXUwqogmiFNH6qpl0Pau1mPsmOPQLDK+NxeQpALRzzAzlULU0u7iJWJcFP+nC03D3mbCudX83nhJE+xHI7HfAhbVpRnMRcPlcltg2Bj6oivDsRIqzWxVmUojh5OdUCH3xsd+O5iI55kkqkIR9VsovBvO3LGbWT0imlqwXIsngGRO1QQpgQnqTNKSCrNch00y4lhQTqlW1Qj4RuQZccv62wi1/KSAJVpbQFgKspDbVtXZFMfbmjfhLCh7edoWyJ5jZfaBe4xB0YnliYd5cIfHCJPVXhL3i5tbxfAgnvEgnXFgIc9uZoON8wSuYjvasq4hsB8uVCwE+cS46fFKMDe9BkZcmUkd4ZZgwIk+jilg9UihkIsugLIjukVXE0tE1J3ddlpxK7VZCiK4soAA0LDv9caAAZoUN7ebSaIIv2YlQEygujnRS2MHj0ww4IHdYTPWJqTrqKnm+KPf3pTydclmoODafumoN8CUbd/HSSVUjvI6UwAROyoUMAzmggo8qyk+/8zu+UwLEszkup9cUdqpNqPjQqgaoJrzgvr8Q+AhD17JhLVNJxgFLNSj/Rh2RZnHTgM17NcQiEQAiEQAiEQAiEQAiEwCEQ2EvAgrPBt+S38GN5TX5WVbkHXCYfDmS7iPyocpMqTSd2wAm3n5/XxKHiihDFY/ThxqxjpwiuI+ewXJFJMjJtAfDqAa4+H6Zu5HIFbQ0Y09OQq9NnWqWJtP4pAd3GWlCAQw4Cx8kmC347V1mUwUlRAN6gQl0aJShxlOCSAISacnq5uDhwoet2PXrI+NhCP2ahhnJbW2X5dC26rMkBV40+ttkLJPEGPTIADtr8YdsZxHdaYGckUwIOZwuXhjsqAQfSsbjSt3/7t9sGwj3WHJqMr1t+fgvhT44S+vz8QCnyMhhiBZhaHwcuVUuVJu6ZA9JaKRoBdoikY3EKzwh4XEVDuCcvZmTnDpeekmOhgKiLrR98XVsbOOr2YjAJb164y13uYo+AxIpg24qbOLqlEm2d18Tq2JJdYm/OQ9QnxwOXfMYzdWyLhypoWcXVmaqgrRaNYp7LGXUfCY+J2Z7HW7ws1tYVShJuwwIzYFoykk9VYS+4hPbgEhcTHClcGkIIgDSBA+8x6aKdwQQ6PMeyKgGZmkYVSvk6ST0HgOgjcpEsIDXmdWxDBw0lwMHHQ0MTqjoUmY2O5q2Sg1HaeD7HIRACIRACIRACIRACIRACh09gLwEL/gOHlovIA+FXNwXOg9uhbsxyXzk25bmt8yi4Je7uek8Bv8tzDZ444PfyiDyKby9Ay5wfELhSJoEcP2+X9GoGN41thre1nlPKd7WzYPSjSsJ4Zl5Kn5GYs0QyJ5BbW+dVjQMmisFD82A/z1BB3vxnGwK3UBovd+AJt5CVBxT2zIXH7z2H70a0wI39JmgACy//2esG7ZzvwIcDmtixAvtKgetOSi+XR07c63anXUzHhn+eqqCDPREiF4I7Y15VVjst25yxQoDC9BGmEaDx0gpbEihvG4K6CznRdiJnc8KshbvrfzqEDEDujDT3k/L1DBGV6l66BHTzk4tbxuaMXTNu6XOzvUpD2EICO0E0kLqMtXPsjFzay0MH9kRAIYhjMwIgdmrU/gjZfSYZq1wxFJeY+niVYvYpqAUHezxfx5UeurlMLc4J17gd6ZBGQZMo20qZc2nOaCbPenjjJn30As9oiFVpI/EvLzEhh3Df3n+h6YUqVF/dnRTxEdqghkADOYJZQlpjmwoM6aFsoMMHrZX0Uo6jQVdB0dpXAt/eo8HkyqSd0RByidmxHw0tquKtK77HBI41Speodl3oDgcKlasIOJj8XHlmh1KSJQRCIARCIARCIARCIARCYBMCewlYKJiXVZ65u+K8FD/LBxAdsH+bI8SZ5y+tU5GfwFGRmBts7zpHnYsuMY+6tsGXI9HZeSmTM32pDyTg43G9PCbgbRGc1brkqXu+pas+nXjbA/ec1YtzTm1yuHk057ELLnjJAkfUE/teBlkRDfXiBvNdF0rkgEHEJ/SGQm4zgd6YaEO+u9w8Xred1YVTzQMHlhw/beLwLUYg41b621hRr/D06gpBHO8p8LZIQRyF0pPjqlKjQMW5FS+uQb2qhSCUkIracR01t2NKevchZ7jUk9hNcq7sQpWrCAm0ZvufdVKTMQAShGnqjrpktkgIiwhjwV5igWUhnrzgxBIiAUcXNJsRnJHSUyH1QlCX7IBgA5OCFCejhyNsLvBOkM/5nM/xMAJHXfN56aYNF1x98kcak2Oa0BYWls8qBFPQ85NiHgViD/xtaZzhjcNYAAVW0J4HLNDjxvPYAfRXLNrCGRrWJhHHk9I3/KkWtoF4JMf7JiuAotVoiAbdfBzovzb10MozI3oNDnDBqJXt9JFAo4vd1CYOWWhof4RkHsyZqyGBIshhz/T30ZpCIc6TRgdGC5d4R5s0JoJ0MHozK8tRkK1GmrIT2H/kXbPUFsYS9ZgXeuSZAkgHn0pc9jD+lObi6/+boDp4JziyiCQIgRAIgRAIgRAIgRAIgRDYmcBZ3Y1cLpVnwlvjCXN4+DacMXsK+IE8T+9H4J+Ub7BOCJeA9+KbEy4WwP/nuvjLAB6Uk6RxJNrZ86RA7WZfJ63OS+/ut/vAPB/eDgfJxnh/6EAaT2zbjQldFrEUqP9N4JXx3MhUCn+Pl6VE7pktAAI0akF/tVAX2blkLWTlAUSq6d2B3nApuyK8PoD7aqcGgUrxBkcl4iNaYe8JwvXcwUppK0/SjQTREH9gwY0HgVa8WUxoLiayspngEizQslqHJrKLeogmUIxAGXnjIKsv19r2BHsuNNAyZFEtZQmR1CMVpW25iyJcwgRq54kAxTEnzr/9Dt/1Xd+lFHYimXJtD3HGt8blG9syQKBwg1pU1IDLzTf2rg1hL63DPue1Y12Utw0HbW+XxKGA2FmgII6xslaSbIUFfbz2QvTEv8OwMdK0Wj3ZJGIipsNghAPA8XIWIRXN500Z/pekonKjcOoJTtkQpHQvjPDeDfqwBFVDgJwx8ebHCoKLKIppFy+JYD+2AglGsFvNVDyFrvRTf88Bly1OQi30kVHcxHYVYSkWqH3F+4R4bBpSX2GIlVqhyrRENPzjiYqLMhgKVMfLU0ljtDe5yU0kYCeiGNoXN0xssPKMkhIFmyigIAlU3AEISpeAEGovN8o6MkxOZdWOwUiDBqPyzyNqoVCVZeH+a0YzueqMov1xCcOggJ/rxOZ8CIRACIRACIRACIRACITAsRDYyw6Lch7cv/Vvphb3/iCTi+jeMk+eY+8POOzt5wxIxlvgSY41cb5O8gfcSuXdiSnwUd215uQ7cFPXrn6+Ci/UzXN3dLnK/BZuqv8pKJkT74XAcj/cVOe+8nke9rCHecMCR134wD1borhJ7ta6oz6XUGdImIgd1XbMr+Pw05On6g42B8x+e64UJbmCXDV+kYKk4Y/x7aVRC+lrw/9KDkr0EfWwb8KDDP54RRaPKvjvT28f8BZPQuwv4N3Zx8GX9v8I7lfzpkhTa3knSq78ybvmDfLK/EmqY34sR522HkiZPw9CQjn/auFPWCVQipa1EcBOEA8X8M9FWJzh2mkaP0FWRzfJkfEaUc8RyEI9bd368HIxAdnbOjjw7vw7LkuQjFgbbfxPB3/SGyUEHWD0gkZBMf8lwbTKbBxAzXlGlZHww/2Lh10eXRBW7v8LoGh072ig8zxKRTfBEb66/930ag+vunTG7gbK297CwVZ9nzne0lZiZgaFBmJp6q5FwORXK522WlOh7NB+DZWVQBaeMOUFRAgpJl2E4IJa8Nt9/I+sl0rqBcy15MjbDPvASXJ8xqt1klgHIGg4MR17l4QeBE10Hw1EMd1Nn2JvpGkR0QROu/CKoAn3XmuCKSKjr3moxD+Dag7PiWgLLSIeZCsKm1dKK1MHzohZCFVoWUULi7AQGfU4wQgy/T+OgBQjvPe97+3dnAJhTJooJo0bY/CfNXbHCCRpVjqLaukOojn+ukUIj+ZlA93WylXTxjjRx09g/UsrIQxV9f1XkSDIk5/8ZGAB14hEGSWYgQNNT3/xQXE9NPzL8rb7mOYK5EwIhEAIhEAIhEAIhEAIhMAygUvzH9alWHmndF1i5zkVXCAuh9vIHGBnRBy4mvwr/oA74dx1PjyHpG5T83h5CJxDPiFfSHoOBj9EHIEjyifhGHD2nOGQu5Hr2FMVXAW53AIVueC88Ss4P+4/c7fcM+fnkMMb5MNwM+q+rtL95HHxMTg/VYq7qa7yZnnp3FcyOTDK5e2rOP05vVJKQz6PTunEcnGdVER9XBWCee5zn6umfDy7A5TF7eTweOqkbuD7VhG1qH0i6svt5NL7SW1VUBCHlnPIhZaXZEXQh3DBDgBVhARKIuMqd04cpyILFONEkaPuwPr3TQmkR1t1lCKjn6Xtym9leY8Dz03F5eJ5kumMYJNnOjTZmJ1Kfro9ztUUNOG+Vukqpb7+5lMCZlAeprYAmduMvAdM3J+XkQ5U5UbatsC/VeviKZfWYRLSc1NlcQY0AQJstQgnmZtNZkFmMB5gUWUnSZORkQiEES5UgR4N6ePdmeUPV93l4jN7QweZ/hmUazq2ZqVxRuzA8yDEQiHuoImrTb/8y79cLfjG2o4laB3mJ71aawL0cGD8yPP5SYCUdw2RBBr3vve9rx0oKqhqWlB9Nah7+ySI4vkTVgecee0rPWkKxYH+6uKkq8olEB9/FSykQk5ZiEvduPLSUHYZWaymdNVJBelEtGI5Ij5U1YlA82FaAhD+hpbCmLtKWw2Ng7pga0sUDUWdqiDSZEeeBAaPjz01DEZzqBdurYwDiVUZScEFUScbOmShoYCm1tFkZPrQwTigajTXgpJR9V73updAhtanDK0kcECUBLTyyJXgneeSlEIC6/INiM7uQLnsEzEZdWelO9mKOSZWoeyBetKwRppLz9LUl20oizIIaFMdhEBaqTLzBrZptMzxQOL6OaExpslxCIRACIRACIRACIRACITAMoGL3Jh1KSqIsO7q/Lz0NuR71J9f59Y0n8SqnU/FteAF8RB4d+Ui8gRkd5XP4Py4ppfeSWcqjePKzj2Q3U/n+br8Q6L4Es5wS/zkXPF2/CShs5eSzjtwUlmukiCGYh8BZ74CEC7hIJmfJFBMGp/KXnq2hDpZ36S57+3eLAfPmzVVmatMk1KVWMkKAr/Ih86CNSWfsyoUwp8staXkOLXwUqN0rpNVNVqVWD8dcOA5UTxbdfHd6SsxgarcMhcOChrflZLakXcnVCF9Qxjzlm7OYIikvOorV5fujHI1unbhCvK3q5Wpqu6qLEHpP8qvXLAAQpqfdabqWxgRpqRyyVSok32VwFKYW85m6F/lVhGVnanUgyTCK5zhyjtWrY+raLVDmD6CCwSWztIUga6vM+SXAtWIXRxtmSuePmR2iZVeRQBnxnWVnAI1L6KKhpQ0JoShND6jDnXGdyszXq2To/xuPsYDuEsMUsxC9IEtlTTlditIMCmiJMjF89fQiugKdsqJHCahFpBqPhUfNVSWIgDB3CUJaDJJoDVdlYaGIjJzm5e+jWolh1GxahEqqb4S5+mr+gRWvTrB2FVHgX0sZeFisX0yByEQAiEQAiEQAiEQAiEQAlsROLaAhQU9R0LAwgsa3PZ0R50bU6rwCnwcW/f7bKWfxJXd6r98Bmc4A04SVS6Bnz6O6+eR8iWW3TeBnaU1PDL7mECuCli4PevfUsvNJrN168RS+rjUtfCTDvOUnWWTAw4VIVKOddkk4zxNYaGVS7RqPecp+4ws5WSurEXp5pJPZWnhLWF+UJS6XSYJqkTfZK7TcF4uIRXVsjvDn5WwTIZqL8M6CV0oUa3zkYk7Vx800nXaVoIymM61cLCyagvply8VzNFcSx/aruM/EVgSnJR+Qz7zQicyAS/mBK5UoxqlSlyZYCJw+Sd9fMg5e1FjQSXTmQQsRiw5DoEQCIEQCIEQCIEQCIGtCBzPOyw4GF6m4C8JPXbuvqiHNcbVP//HZyu1xsTz7ISP3tFFrsZw73fMu/JY4jF7pdlZQ9Lcbi2Bdbyy0Hktdi5xlD+vyHh1q+PCspXAhfoqei5qkyovp1kuseo7L5d9eojg0Y9+tNeg2PPvTyWY6HJBLWoubXOqRyKtBJsLPBtl5qXMYW6rz1zCvJTJmSOzaJflpgHhGDnQx2eiZH6GQAiEQAiEQAiEQAiEQAgcAoHjCVhcfJPyjOcpvEHAo/XepOCG9iFU7wR08LCA50HqEfcTKC5F7ECAfYpZiCt5rMPLUAUs6mGEHUQlSwiEQAiEQAiEQAiEQAiEQAiEwMkQOM5HQupRcGEL9z9Pz01LlfVaAc/ke3XFybRZStmBgGiF15QIW9TbIpbv4e8gP1lCYCSQR0JGGjkOgRAIgRAIgRAIgRAIgd0IHFvAojZZUOK0uYKntuK7Gdy5ylWbLMo+T0807VzRTrkJWMQGQiAEQiAEQiAEQiAEQuDsCRzPIyH0uOhB8FP5KPiprfjZG99JStBMx/jig5PUPGWFQAiEQAiEQAiEQAiEQAiEwOkkcNFfQuQTAiEQAiEQAiEQAiEQAiEQAiEQAiEQAgdFIAGLg2qOKBMCIRACIRACIRACIRACIRACIRACIXARgQQsYgchEAIhEAIhEAIhEAIhEAIhEAIhEAIHRyABi4NrkigUAiEQAiEQAiEQAiEQAiEQAiEQAiGQgEVsIARCIARCIARCIARCIARCIARCIARC4OAIJGBxcE0ShUIgBEIgBEIgBEIgBEIgBEIgBEIgBBKwiA2EQAiEQAiEQAiEQAiEQAiEQAiEQAgcHIEELA6uSaJQCITAJZ3AmTNnLulViP4hEAIhEAIhEAIhEAIhcM4JXLCgwWUuc5mFq7kUAiEQAiGwTODNb37zcoJcDYEQCIEQCIEQCIEQCIEQWEdgKWBxqUtl/8U6bjkfAiEQAiEQAiEQAiEQAiEQAiEQAiGwRwIJSewRbkSHQAiEQAiEQAiEQAiEQAiEQAiEQAjsRiABi924JVcIhEAIhEAIhEAIhEAIhEAIhEAIhMAeCSRgsUe4ER0CIRACIRACIRACIRACIRACIRACIbAbgQQsduOWXCEQAiEQAiEQAiEQAiEQAiEQAiEQAnskkIDFHuFGdAiEQAiEQAiEQAiEQAiEQAiEQAiEwG4EErDYjVtyhUAIhEAIhEAIhEAIhEAIhEAIhEAI7JFAAhZ7hBvRIRACIRACIRACIRACIRACIRACIRACuxG4YCHb6173uoWruRQCIRACIRACIRACIRACIRACIRACIRACeyKQHRZ7AhuxIRACIRACIRACIRACIRACIRACIRACuxNIwGJ3dskZAiEQAiEQAiEQAiEQAiEQAiEQAiGwJwIJWOwJbMSGQAiEQAiEQAiEQAiEQAiEQAiEQAjsTiABi93ZJWcIhEAIhEAIhEAIhEAIhEAIhEAIhMCeCCRgsSewERsCIRACIRACIRACIRACIRACIRACIbA7gQQsdmeXnCEQAiEQAiEQAiEQAiEQAiEQAiEQAnsikIDFnsBGbAiEQAiEQAiEQAiEQAiEQAiEQAiEwO4EErDYnV1yhkAIhEAIhEAIhEAIhEAIhEAIhEAI7IlAAhZ7AhuxIRACIRACIRACIRACIRACIRACIRACuxNIwGJ3dskZAiEQAiEQAiEQAiEQAiEQAiEQAiGwJwIJWOwJbMSGQAiEQAiEQAiEQAiEQAiEQAiEQAjsTiABi93ZJWcIhEAIhEAIhEAIhEAIhEAIhEAIhMCeCCRgsSewERsCIRACIRACIRACIRACIRACIRACIbA7gQQsdmeXnCEQAiEQAiEQAiEQAiEQAiEQAiEQAnsikIDFnsBGbAiEQAiEQAiEQAiEQAiEQAiEQAiEwO4EErDYnV1yhkAIhEAIhEAIhEAIhEAIhEAIhEAI7IlAAhZ7AhuxIRACIRACIRACIRACIRACIRACIRACuxNIwGJ3dskZAiEQAiEQAiEQAiEQAiEQAiEQAiGwJwIJWOwJbMSGQAiEQAiEQAiEQAiEQAiEQAiEQAjsTiABi93ZJWcIhEAIhEAIhEAIhEAIhEAIhEAIhMCeCCRgsSewERsCIRACIRACIRACIRACIRACIRACIbA7gQQsdmeXnCEQAiEQAiEQAiEQAiEQAiEQAiEQAnsikIDFnsBGbAiEQAiEQAiEQAiEQAiEQAiEQAiEwO4EErDYnV1yhkAIhEAIhEAIhEAIhEAIhEAIhEAI7IlAAhZ7AhuxIRACIRACIRACIRACIRACIRACIRACuxNIwGJ3dskZAiEQAiEQAiEQAiEQAiEQAiEQAiGwJwIJWOwJbMSGQAiEQAiEQAiEQAiEQAiEQAiEQAjsTiABi93ZJWcIhEAIhEAIhEAIhEAIhEAIhEAIhMCeCCRgsSewERsCIRACIRACIRACIRACIRACIRACIbA7gQQsdmeXnCEQAiEQAiEQAiEQAiEQAiEQAiEQAnsikIDFnsBGbAiEQAiEQAiEQAiEQAiEQAiEQAiEwO4E/j8SPywxRJ2fBgAAAABJRU5ErkJggg==" alt="image.png"></p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[2]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">transformers</span> <span class="k">import</span> <span class="n">BertTokenizer</span><span class="p">,</span> <span class="n">TFBertForSequenceClassification</span>
<span class="kn">from</span> <span class="nn">transformers</span> <span class="k">import</span> <span class="n">InputExample</span><span class="p">,</span> <span class="n">InputFeatures</span>

<span class="n">model</span> <span class="o">=</span> <span class="n">TFBertForSequenceClassification</span><span class="o">.</span><span class="n">from_pretrained</span><span class="p">(</span><span class="s2">&quot;bert-base-uncased&quot;</span><span class="p">)</span>
<span class="n">tokenizer</span> <span class="o">=</span> <span class="n">BertTokenizer</span><span class="o">.</span><span class="n">from_pretrained</span><span class="p">(</span><span class="s2">&quot;bert-base-uncased&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Initial-Imports">Initial Imports<a class="anchor-link" href="#Initial-Imports">&#182;</a></h2><p>We will first have two imports: TensorFlow and Pandas.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">tensorflow</span> <span class="k">as</span> <span class="nn">tf</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Get-the-Data-from-the-Stanford-Repo">Get the Data from the Stanford Repo<a class="anchor-link" href="#Get-the-Data-from-the-Stanford-Repo">&#182;</a></h2><p>Then, we can download the dataset from Stanford’s relevant directory with tf.keras.utils.get_file function, as shown below:</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">URL</span> <span class="o">=</span> <span class="s2">&quot;https://ai.stanford.edu/~amaas/data/sentiment/aclImdb_v1.tar.gz&quot;</span>

<span class="n">dataset</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">keras</span><span class="o">.</span><span class="n">utils</span><span class="o">.</span><span class="n">get_file</span><span class="p">(</span><span class="n">fname</span><span class="o">=</span><span class="s2">&quot;aclImdb_v1.tar.gz&quot;</span><span class="p">,</span> 
                                  <span class="n">origin</span><span class="o">=</span><span class="n">URL</span><span class="p">,</span>
                                  <span class="n">untar</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span>
                                  <span class="n">cache_dir</span><span class="o">=</span><span class="s1">&#39;.&#39;</span><span class="p">,</span>
                                  <span class="n">cache_subdir</span><span class="o">=</span><span class="s1">&#39;&#39;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Remove-Unlabeled-Reviews">Remove Unlabeled Reviews<a class="anchor-link" href="#Remove-Unlabeled-Reviews">&#182;</a></h2><p>To remove the unlabeled reviews, we need the following operations. The comments below explain each operation:</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># The shutil module offers a number of high-level </span>
<span class="c1"># operations on files and collections of files.</span>

<span class="kn">import</span> <span class="nn">os</span>
<span class="kn">import</span> <span class="nn">shutil</span>

<span class="c1"># Create main directory path (&quot;/aclImdb&quot;)</span>
<span class="n">main_dir</span> <span class="o">=</span> <span class="n">os</span><span class="o">.</span><span class="n">path</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">os</span><span class="o">.</span><span class="n">path</span><span class="o">.</span><span class="n">dirname</span><span class="p">(</span><span class="n">dataset</span><span class="p">),</span> <span class="s1">&#39;aclImdb&#39;</span><span class="p">)</span>
<span class="c1"># Create sub directory path (&quot;/aclImdb/train&quot;)</span>
<span class="n">train_dir</span> <span class="o">=</span> <span class="n">os</span><span class="o">.</span><span class="n">path</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">main_dir</span><span class="p">,</span> <span class="s1">&#39;train&#39;</span><span class="p">)</span>
<span class="c1"># Remove unsup folder since this is a supervised learning task</span>
<span class="n">remove_dir</span> <span class="o">=</span> <span class="n">os</span><span class="o">.</span><span class="n">path</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">train_dir</span><span class="p">,</span> <span class="s1">&#39;unsup&#39;</span><span class="p">)</span>
<span class="n">shutil</span><span class="o">.</span><span class="n">rmtree</span><span class="p">(</span><span class="n">remove_dir</span><span class="p">)</span>
<span class="c1"># View the final train folder</span>

<span class="nb">print</span><span class="p">(</span><span class="n">os</span><span class="o">.</span><span class="n">listdir</span><span class="p">(</span><span class="n">train_dir</span><span class="p">))</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Train-and-Test-Split">Train and Test Split<a class="anchor-link" href="#Train-and-Test-Split">&#182;</a></h2><p>Now that we have our data cleaned and prepared, we can create text_dataset_from_directory with the following lines. I want to process the entire data in a single batch. That’s why I selected a very large batch size:</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># We create a training dataset and a validation </span>
<span class="c1"># dataset from our &quot;aclImdb/train&quot; directory with a 80/20 split.</span>
<span class="n">train</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">keras</span><span class="o">.</span><span class="n">preprocessing</span><span class="o">.</span><span class="n">text_dataset_from_directory</span><span class="p">(</span>
    <span class="s1">&#39;aclImdb/train&#39;</span><span class="p">,</span> <span class="n">batch_size</span><span class="o">=</span><span class="mi">30000</span><span class="p">,</span> <span class="n">validation_split</span><span class="o">=</span><span class="mf">0.2</span><span class="p">,</span> 
    <span class="n">subset</span><span class="o">=</span><span class="s1">&#39;training&#39;</span><span class="p">,</span> <span class="n">seed</span><span class="o">=</span><span class="mi">123</span><span class="p">)</span>
<span class="n">test</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">keras</span><span class="o">.</span><span class="n">preprocessing</span><span class="o">.</span><span class="n">text_dataset_from_directory</span><span class="p">(</span>
    <span class="s1">&#39;aclImdb/train&#39;</span><span class="p">,</span> <span class="n">batch_size</span><span class="o">=</span><span class="mi">30000</span><span class="p">,</span> <span class="n">validation_split</span><span class="o">=</span><span class="mf">0.2</span><span class="p">,</span> 
    <span class="n">subset</span><span class="o">=</span><span class="s1">&#39;validation&#39;</span><span class="p">,</span> <span class="n">seed</span><span class="o">=</span><span class="mi">123</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><img src="data:image/png;base64, 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Be8oQa94HyVcDUpfJ5o+b7vtttkPf/jD7GMf+1h25513DgpavB2OAcdABRioRaIL0WJxBrbeeuvskEMOSTZ10003DQwAEieY3joBZktg3xU2DM9333033KP+ve99L1hRp/rEhoL72RdddNFUdAjjesItt9wyWGTHiXbaaafSO7mVVt/fMneKO/PMM7MVV1xRP5PPyy67LDvwwAPHxXEVLX2DYS+DXtteVm6n4SyWjP0qgCtOW8EgW8i3anuV8VXivcp21VnW448/nt16662hiq222qovVxZX3R9Lk+171fWUlQftBBAKODgGHAPDhYFaGN3hQtHk6Q1S0JNPPnlcg9lIiOnEndBGG22UTZkyJVtwwQXHpf3tb3+bbbbZZtnPfvazIs7mP+2008I94QcffHA21VRTFWn08pOf/CTbcMMN9XPcc7vttstOOeWUbPXVVx8XR8B3v/vd7Gtf+1oyjnvKKRtml3vhY+i17XF5vfxGaitgc7DMMssU99jPPPPMiqrsefPNNxdlgYfPfvazxe9Reuk33gcBt8xp5iWw1lprTUpGdxDw6G1wDDgGhhMDI2OMhuPzK664Ivwtu+yyw/k1/9YrbjqCEb3lllsybjpCWn733XdnHG8Ldt555+BHU7/1POmkkwomd/nllw9XhJL/qquuKnQ9zz333BCuPHqig7r33nvrZ8axOeoHMM3f+MY3ivBddtmlYLyLwPzl17/+dQOTe/bZZ4e8LORf/vKXQ1J0UcsY4V7abtvR6zsSKdoMIDnfZ599ssUWWyww5zDo00wzTVtVsBlhzO64445tpR/1RFXhfdTxOBH9n2j6zKkjc+2ss86aiO57nY4Bx0CNGBgZRpf72hdeeOHwN91009WI0okreuqpp86QaHFt5zbbbJPNOeechdN39KRhBNFBA5COWqktYUiEL774Yl6DVIiyYJoBHMhTpuD73/++XovnI488kr344ovhN0z1rrvuGvRr0QneYIMNAu6V2EogFXbNNdfoNTvooIOyFVZYIegT8+323XffIu7+++/PXnjhheI3L722vaGwHn+g0yxYfPHF9drxE4k7Y3b22WfvOO8oZqgK76OIu4nu80TT509+8pNhrmFL4OAYcAwMFwYGXnUBo6JLLrkke/bZZzPeMWbCwA3JGBJHjJTKjKtgxt58881xXwyJrgx9xkXmAei7PfPMM8E6HiMFdE6RiMJgwVAtsMAC2cYbb5zNM888qewhjJt7kMhxlI9B1bzzzpstssgiwQjpnnvuyTAS+/CHP5ytu+66pWV0GvH+97+/qZHTBz7wgWyllVbKzjnnnFA0BoPWCPC2224rqqRd0047bfGb43DlIxDcHnrooQ3SyauvvrpID36sagN9BhcC9HDXW289/QweCS699NLi9/rrr1+883LGGWc0/IYptkZWvba9ofAufpx33nmFlPq1114rSnjwwQeDqkYRkL+svPLKwbjPhvGOERXjLgakXUsssUQcXPlvxvZ1110XpPBI4v/yl7+EsQ6zveaaazZ8z1TlfF/GAPMU6TweH9CrZo4ut9xyGcxE1VAF3mnTfffdl917772h75wasElkztLvVqom0IWHH3444IfNIPqeSAfZcL700kvZjDPOGAw5UQmaZZZZekbBK6+8kl1++eVFOXZeXXTRRYE+FpH5C5stvmEKum07YwMjy7vuuisYHv/qV78KtBGjVeji5z73ufDdU3UqbCLp83PPPRfarrboibEtm/IygJZjtAZssskmQY3r9ttvD2OHTT6M8qqrrtpwepYqi1MyNvsPPfRQiEbVCNsF5sv1118fwljfmtkjpMr1MMeAY2A8Bgaa0W2mrwkzil5ama4pXUUiieQyBiS6zRjdG2+8MSzY5CMdzK6FRx99NLvwwguDPumSSy5po8L7q6++mu2www4FESMQppLjf4xlYIQgcEhXq2R0xzUkESAXV0QhRbEgoktY3K8jjzyyYOSUh4WOI3kBzKzAGrvBQO2///6KCk/qgiGQERWLt6TBeHewUneYP/R6LbBAW0a317bbsrt5Z6xJD9rmp538WUC6DkMQA0ymZfYV/8UvfrF2RhfGFnz+4he/ULXhqbF+7bXXZt/85jfD5qwhQf4DlQFUVkiTAhZuxg/MRdXQK94x9EOtxm7iaCOqJzDtnILwB9NRBjC00pFl84aqCZtjAScnbGL4s5tBxXf6ZBNBv1OgExkbt99++5Uyut22nRMXy2yrPuicxgFjAjpYJoiYKPpMW2E0U55MYDSbMbrkE+5ZG1CjYmMkoP+sSagroZufAsbAXnvt1RAF/YLGoe514oknhrgZZpjBGd0GLPkPx0B3GBhYRheCYXUxkRAiYUFSyrH1TTfdFAgMkoUywIUTVvjAyy+/nNzBl+VV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GIb33HPPzVZeeeVsscUWayganbq99967CNtjjz0yjjNhDK+66qpsv/32C3G77LJLkODDQFtAZ9AyuWeffXa27LLLBt1Y2nHhhReGo2zSwOzWCc8880xR/D777JMtvvjixe92X2Bc6St6tg7tYeCpp54qEh511FEDef1s0UB/acDAqI73UVxbGj68/3AMDDgGRobR5b72hRdeeMA/R7XNQ68WHel2Ab3Yiy++OCSHuUUFQlI0HMhvs802GYwwgIpEzOg+8sgjhS4rEsldd921kPpusMEGQdcUiS9w8803Z+utt154179rrrlGr9lBBx2UrbDCCuE3327fffcNjC4B999/f4Ye5+yzz16kr/rFGuqgH9wNoAft0BkG0AsHmKt8d4fJg4FRHe+juLZMnlHpLXUMZNnAM7osfJdcckn27LPPZrwjHYR54+gaiSNMyHvf+97kt4QZw6AoBqSEzaS6t956a4ZEDyM5JJLonHKUDYMFM8gR9sYbb5zNM888cdHFb6zFp0yZksHYYVA177zzZossskgwiLvnnnuCwRjGYOuuu26RZ6JfbrvttqIJtEtMLoGoNJxzzjlFPLg99NBDs2mmmaYIu/rqq4t38IN3AgF9FpNLGHq4ltFFGnzppZcqebb++usX77ycccYZDb9hinfbbbeGsF5+8I0wHBM8+OCDes2QLNu+gJfNN9+8iNcLR8F33XWXfhZPDPhg9PsBSN5/9KMfhTGH+gnMB4Y9HMtKBaCsHb3MtbIyW4VrrindL37xi/CKQSUqLhboR5n+Lrhn84REGFox22yzBePH5ZZbLtzyZcuJ39Gr/M53vhOs/FFTwUgL3WzGKDj805/+FHC35pprZiuttFIpvYnLLfsNbTjrrLNC9JxzzpmtuuqqZUkDzXn44YdDPGo7duP62muvhW+N0d5LL72U/epXvwonONAl/jiOr3Oz0Ot4f/nllzNoBrim7dDypZZaqqUOP8h48cUXM2gKxq6MFW52Q3effjNO+E52zgrB1113Xfb888/rZ6GSxfyPxxvryo477liktS/dri0q4/XXX8+gYYxXDLeho/PNN19YIzgtSwF5UO0CWMO4wQ6azbrEGsX85uQJ1bOyNTFVroc5BoYdAwPN6DbT12SBRF8UZpLFKQVIJNHrjGG66aZryujeeOONgQCTD4YYZtcChJljdNqXslx+9dVX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" alt="image.png"></p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>As you can see, we have 20,000 reviews for training and 5,000 for validation.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Convert-to-Pandas-to-View-and-Process">Convert to Pandas to View and Process<a class="anchor-link" href="#Convert-to-Pandas-to-View-and-Process">&#182;</a></h2><p>Now we have our basic train and test datasets, I want to prepare them for our BERT model. To make it more comprehensible, I will create a pandas dataframe from our TensorFlow dataset object. The following code converts our train Dataset object to train pandas dataframe:</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">train</span><span class="o">.</span><span class="n">take</span><span class="p">(</span><span class="mi">1</span><span class="p">):</span>
  <span class="n">train_feat</span> <span class="o">=</span> <span class="n">i</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">numpy</span><span class="p">()</span>
  <span class="n">train_lab</span> <span class="o">=</span> <span class="n">i</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">numpy</span><span class="p">()</span>

<span class="n">train</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">([</span><span class="n">train_feat</span><span class="p">,</span> <span class="n">train_lab</span><span class="p">])</span><span class="o">.</span><span class="n">T</span>
<span class="n">train</span><span class="o">.</span><span class="n">columns</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;DATA_COLUMN&#39;</span><span class="p">,</span> <span class="s1">&#39;LABEL_COLUMN&#39;</span><span class="p">]</span>
<span class="n">train</span><span class="p">[</span><span class="s1">&#39;DATA_COLUMN&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">train</span><span class="p">[</span><span class="s1">&#39;DATA_COLUMN&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">decode</span><span class="p">(</span><span class="s2">&quot;utf-8&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Here-is-the-first-5-row-of-our-dataset:">Here is the first 5 row of our dataset:<a class="anchor-link" href="#Here-is-the-first-5-row-of-our-dataset:">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">train</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><img src="data:image/png;base64, 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BFocATFuLd5AKp4QEAJCQAgIASEgBISAEBACQkCMm/qAEBACQkAICAEhIASEgBAQAkKgxREQ49biDaTiCQEhIASEgBAQAkJACAgBISAExLipDwgBISAEhIAQEAJCQAgIASEgBFocATFuLd5AKp4QEAJCQAgIASEgBISAEBACQkCMm/qAEBACQkAICAEhIASEgBAQAkKgxREQ49biDaTiCQEhIASEgBAQAkJACAgBISAExLipDwgBISAEhIAQEAJCQAgIASEgBFocga4tXj4VTwgIASEgBIRAzRD46KOP3B9//JGZ3uijj+4mmWQSx7VSeuedd9zQoUPdp59+6sYbbzw39dRTu4knnrhNMp988on77bff2riXcphhhhncyCOPXBDs999/dx9//LF3e/vttx1hpplmGjfmmGMWhKvHwz///OMee+wx9/7777vPPvvMjTHGGG6eeeZxc889d2a988rw119/uUceecR98MEH7vPPP3ddu3Z1k08+uZtxxhndoosu2qbOYTrffvut++6771Knaaed1o066qjpc97NN998477//vvUu1i89957z1FXaLTRRvP4WsRff/3Vt7c9c51ppplcly5dQqc297QZbWc0wQQTFGAW1musscZyU0wxhQVtc/3qq6/cjz/+6N3Jl/wbRf/++69799130+zGGWccN9lkk6XPldxU05cN/6+//tqBGXmPP/74aba015RTTlm0DxWbD9KEht8wrrt165Y6h3EZm4y/RtLPP//sHn74YT8HfPnll76fMAbnnHPOiuaAH374wafD3EV/Gnfccf0YJK3ZZ5+9aJWqxaDceH/++af78MMP0zIUGysEYu5m7i1GzNPM1yHRT8J5Mywf8zj55hHlo5xQqfGal0Yl7l2SCgytJILCCgEhIASEgBDoqAisttpq7o033ihafBaAG220kdtggw2KLpotEZiO7t2726O/Lrnkku6KK64ocONhnXXWcS+99FIb91IODzzwgIPBCKl///7ugAMOCJ3880477VTgVuuH66+/3p155pnuiy++yEx6+umnd3369PELyMwAiSPM0EUXXeTOOecc98svv2QGox322GMPt/HGG2f6H3fcce6SSy5J/W699VbPOKYOOTfHHHOMu+yyy1Lf22+/Pbes4WJ85plndgMHDkzj3Xfffa5nz57pMzc33HCDW3DBBQvc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lnNqoXXESuIqbOdCQKqSnas9VRshIASEgBAQAkJACAgBISAEOiECYtw6YaOqSkJACAgBISAEhIAQEAJCQAh0LgSkKtm52lO1EQJCQAgIASHQBgHOrmR9MLtNwAwHvo2GKXKREBAC1SPw4Ycfpuc4K02F82u1tOpYaf4K3zoIiHFrnbZQSYSAEBACQkAICAEhIASEgBAQApkISFUyExY5CgEhIASEgBAQAkJACAgBISAEWgcBMW6t0xYqiRAQAkJACAgBISAEhIAQEAJCIBMBMW6ZsMhRCAgBISAEhIAQEAJCQAgIASHQOgiIcWudtlBJhIAQEAJCQAgIASEgBISAEBACmQiIccuERY5CQAgIASEgBISAEBACQkAICIHWQUCMW+u0hUoiBISAEBACQkAICAEhIASEgBDIRECMWyYschQCQkAICAEhIASEgBAQAkJACLQOAmLcWqctVBIhIASEgBAQAkJACAgBISAEhEAmAmLcMmGRoxAQAkJACAgBISAEhIAQEAJCoHUQEOPWOm2hkggBISAEhIAQEAJCQAgIASEgBDIREOOWCYschYAQEAJCQAgIASEgBISAEBACrYNA12qLMmjQoGqjKp4QEAJCQAgIASEgBISAEBACQkAIJAh07969LBwkcSsLJgUSAkJACAgBISAEhIAQEAJCQAg0D4EuQxNqXvbKWQgIASEgBISAEBACQkAICAEhIARKISCJWymE5C8EhIAQEAJCQAgIASEgBISAEGgyAmLcmtwAyl4ICAEhIASEgBAQAkJACAgBIVAKATFupRCSvxAQAkJACAgBISAEhIAQEAJCoMkIiHFrcgMoeyEgBISAEBACQkAICAEhIASEQCkExLiVQkj+QkAICAEhIASEgBAQAkJACAiBJiMgxq3JDaDshYAQEAJCQAgIASEgBISAEBACpRAQ41YKIfkLASEgBISAEBACQkAICAEhIASajIAYtyY3gLIXAkJACAgBISAEhIAQEAJCQAiUQkCMWymE5C8EhIAQEAJCQAgIASEgBISAEGgyAmLcmtwAyl4ICAEhIASEgBAQAkJACAgBIVAKATFupRCSvxAQAkJACAgBISAEhIAQEAJCoMkIiHFrcgMoeyEgBISAEBACQkAICAEhIASEQCkExLiVQkj+QkAICAEhIASEgBAQAkJACAiBJiMgxq3JDaDshYAQEAJCQAgIASEgBISAEBACpRAQ41YKIfkLASEgBISAEBACQkAICAEhIASajIAYtyY3gLIfhsA///zjvv/++04Jx6+//up+++23Tlm3jlKp7777ztHHREKgngh8/fXX9UxeaQsBISAEhMAIjkBTGbcffvjB3Xzzza53797u2GOPdVdccYV78cUXO32TsIB89NFH3VVXXeVOPvlkd/XVV7uXXnrJ/fHHH52+7ssuu6ybe+653aBBg9K6wtgstdRSbsEFF3T9+/dP3TvSzbvvvuvrRd2+/fbbtOj057nmmsstssgi7o033kjddVMeAjDzb7/9tgPfcoi+RHh+f/31l49y5ZVXuoUWWsgtv/zyI8QYKwenRoX58ccffVu89957JbMcOnRo2natvNHBnM04P/TQQwvqtNtuu7lFF13UHXDAAQXuHenhm2++SeexctqsFnXLw7MWaSsNISAEhEC9Efj000/9u+uzzz6rd1Y+/a4NySUjkwsvvNCdeOKJGT7OLbnkkp6hmWyyyTL9O7Ljrbfe6k466ST3xRdfZFaDl/+ee+7pRh555Ez/ju4IU/PLL7+433//Pa3K66+/nuJx3333ufXXXz/16yg3MAnUC/r777/TYj/22GP+Hr+nnnrKzTbbbKlfq9389NNP7quvvnKjjDKKm3baaVuiePfcc487+OCDfVkeeOCBkuW65ppr3HHHHefDP/nkk26SSSZx9957r3/+6KOP3DvvvOPmnHPOlqjbiFAINmKsPS655BK33HLL5Vb7559/diuvvLL3h9leYoklcsOW6/Hhhx96Br5bt25u3HHHLTda0XBDhgzxY53xYvTnn3+6u+66yz9SZ+b4Ll26mHfulbnigw8+8P7TTTed69q1aa9kXwbKkzWP5VagDI8vv/zSgdk444zjJp100jYxsvBsE6gTOJTCoRNUUVUQAiMUAsyXZ599tuvTp4+v92KLLeb69etXdwyaInFjhy2PaaPGjzzyiNt4440dE11nIiSLe++9d8qkzDzzzG6VVVbxEhmrJ52gZ8+ejp3qEYXmm28+t84663gctttuu05V7bXWWssxmNmMsEVpq1bw9ttvdyuttJJbY401WqaIjA+jAQMG2G3u9cYbb/R+MAgwbdCOO+7oGeYNN9zQzTHHHN5Nf41HYI899iiQRjeiBPRl+jR9u5406qijegnc9NNP74455piy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LrQPql6hWk+ptIiHcQwIs+nhbnCpuFn+1ZYjK632uv3888+O9oOZYzFig7a96ZaKz1ClLciPRYYteIrFYwHP+TjUammHvM9CxGmwoEcFh82TvHwIw3kXygIWIyqhlog6KwuuUN20FB70I9qmEeO4VFmy/FuxfaudB3jXmGq6MbphnatNN0yjvfeMVcrIZx/yxilzAGeZqAMq3JUQ7wzyYLw2i5iHKAPzSq3nzWrmxzwc6t0f8nBgzFGPrPdlMT/qQd8ZkefhvLaUuxDobAg0lXHrbGCqPkJACAgBISAEhIAQEAJCQAgIgXog0BRVyXpURGkKASEgBISAEBACQkAICAEhIAQ6KwJi3Dpry6peQkAICAEhIASEgBAQAkJACHQaBMS4dZqmVEWEgBAQAkJACAgBISAEhIAQ6KwIiHHrrC2regkBISAEhIAQEAJCQAgIASHQaRAQ49ZpmlIVEQJCQAgIASEgBISAEBACQqCzIiDGrbO2rOolBISAEBACQkAICAEhIASEQKdBQIxbp2lKVUQICAEhIASEgBAQAkJACAiBzoqAGLfO2rKqlxAQAkJACAgBISAEhIAQEAKdBgExbp2mKVURISAEhIAQEAJCQAgIASEgBDorAmLcOmvLql5CQAgIASEgBISAEBACQkAIdBoExLh1mqZURYSAEBACQkAICAEhIASEgBDorAiIceusLat6CQEhIASEgBAQAkJACAgBIdBpEBDj1mmaUhURAkJACAgBISAEhIAQEAJCoLMiIMats7as6iUEhIAQEAJCQAgIASEgBIRAp0FAjFunaUpVRAgIASEgBISAEBACQkAICIHOikDXaiv22S//VhtV8YSAEBACQkAICAEhIASEgBAQAkIgQWCKscqTpZUXSpAKASEgBISAEBACQkAICAEhIASEQNMQEOPWNOiVsRAQAkJACAgBISAEhIAQEAJCoDwExLiVh5NCCQEhIASEgBAQAkJACAgBISAEmoaAGLemQa+MhYAQEAJCQAgIASEgBISAEBAC5SEgxq08nBRKCAgBISAEhIAQEAJCQAgIASHQNATEuDUNemUsBISAEBACQkAICAEhIASEgBAoDwExbuXhpFBCQAgIASEgBISAEBACQkAICIGmISDGrWnQK2MhIASEgBAQAkJACAgBISAEhEB5CIhxKw8nhRICQkAICAEhIASEgBAQAkJACDQNATFuTYNeGQsBISAEhIAQEAJCQAgIASEgBMpDQIxbeTgplBAQAkJACAgBISAEhIAQEAJCoGkIiHFrGvTKWAgIASEgBISAEBACQkAICAEhUB4CYtzKw0mhhIAQEAJCQAgIASEgBISAEBACTUNAjFvToFfGQkAICAEhIASEgBAQAkJACAiB8hAQ41YeTgolBISAEBACQkAICAEhIASEgBBoGgJi3JoGvTLuzAj89uuv7vfff2toFf/++2/377//FOT5w3fftXErCKAHISAE2o3AP//843784Yd2pxMnoPEbI6JnISAEhMCIjUBLMW5//vmne++dt9PfF599OmK3TpW1H/LTjx7DTz76sMoUFA0EHn7gfrf8IvO6DVdfsSJAXnv5Rdd9kXnc6ksv5t55642K4lYa+N9//3WXnNvHbdFjDbfUfLO5JeaZ1X36ycc+mf7XXOVWXXoRt8FqK7g///gjTbraeqUJ1OmG8c74/+Lzz4rmAEM86J4B7rILzvF1v3fAHe7nn4cUjdNZPLffdH3fJwfcfktnqVKHrwebND1WWsatsuRC7o6b+9esPnnjt2YZKKGaI/Ddt9/48cl748MP3qt5+kpQCAiB1kOg3LVLrUretVYJtTedd99+y/U6cJ+Che4CCy/qzrns6vYmPcLFv+PmG12fU453E0w4kbvroSdHuPqXW+EhQ35y3379tevataubappp20T744/f3a+//uLc11+18Svm8PQTj3tv4r7wzNNupllmKxa8XX7n9z7VXXnJhWkaY445lht5pGH7MQ8Pute7f5Ywch+8966bZfY5/HO19UozqfENkkKYsEvPO8unXGzcP/PEY+6IA/Z233/3bUEpqPehx57ouq+0aoF7Kz5889WXCaP5sxt77LHdxN0mraiI1Jt+9XvCLIhaA4G333zdffXlF74wjwwe5NZYd/20YPRt20BjjmGuKZfyxm+58RWu8QggefXvjCTrv//6u/EFUI5CQAg0DIFK1i61LFT5b5Fa5hqkhWrX9Vf1db1PPj5w1a0QqD8C9911hzv5mCMci/77n3qxZhmuvPqa7qnHHvaLtGVXWKlm6WYlBJMOLb70sm7vgw4vYEA337an++7bb93sc83tZp5t9qzoTXdDOnhkwoi9+tILJcvy+isvud233zINt8oaa7uRk4XwA/fc7RdLh+6zuzv9vEvc/5ZaJg3TijdnnnScu3/gXW75lVdzx57WpxWLqDJVgMCc88zn6Ivvv/uO23jLbQpifvj+e27zdVfzblfdfJebceZZCvyLPXSE8Vus/PITAkJACHRWBCpZu9Qag6Yybuw8H5lI2Z57WlKhWjes0mseApNNMWVDJMVIX0zy1GPjzQqYNmq/8P+WcFfedEfzgCiR88A7bnW9Dto3DTXFVFM7pINZNHToUHfSUYenXtfecY+bdroZ/PNOe+zjtlx/LY/Fib0OdTcMGORGHXXUNKxuhEA9ERh55JHdkSeeVvMsWn381rzCSlAICAEh0AEQqGTtUo/qNPWM25OPPVLAtM0+1zz1qKPSrAIBzk59+83XjgVzpcQh/Xob5kAl5ZtEhTE2xlFpWasJj8EA8m8vcTaG84jV0m+//acul6XqWW26YTzqacxh6G73P3z/fcH5OXMvdeUsiDFtqJLCiCE1zCM2d958/VXvvdMe+6ZMGw6oG+6+30HeD5W1QYk0qz1Enavp++DEuGk0+bGQbIJV0icZ17QdarOV0F9//eXYcKtk3NlcUkn5KilTGJZ60XaV5OXxa9JcEpa92vtazre1bitUiRjr1bxHqsGDfsl7gfPyldAviepyNXMxfefrZDyUyo/3YSNxqKTuCisEhED5CFS6dik/5fJDNlXiFhZz130PdOtttJk36hC6676xCDz+8INejcvUz8h93Q03dT1339tdeNYZbvB9A906G2zsn8OSoSZ07hknu+eeejLV8Z9+xpncwost4Xbeez83+uhj+OBvvf6a22vHYepEp59/iZttjrnCZEqGefO1V93F5/Z2nCWBUHNccrnubvGllnUrJ+pK5RC7JajmGkPCmYTVll7UR126+wruoF7HtUmGBe7Zp53kHrr/3vQ8y6JLLOU223p7L9kKI3z84Qduxy028k5X3Xynm3CiiVNvjIRY+cEM4izioosv6RgDE0/SLQ2bd2MY/vH7f4u5a3o0AABAAElEQVTubTdc1402+ug+yi33PewlTncnBiz6nHKCm3ra6dwFV16Xl1zqfvP117iLzj7Tt8khRx/vzjjxWPfEIw/59gTnbXbezW2y5bbur7/+dP0uv8RdfelFaVujLrbdzrtXrKaIatnOe+7nRh1ttLQcWTe0O0Q5Ntxia38f/q20+lrJWb8LvLraG6+94lZZc53QO/f+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PBq6ceADLjSpPALBpKoKASEgBIRACyCQxbi1QLFUBCEgBIRAVQiUy7i13dapKjtF6ugIcHgbFRHUbjicffE5vd3c8y+QPH+SqvNRxx4bbyamraM3tsovBISAEBACQkAICAEh0OEQKE8u1+GqpQJXigCqhpdff0t6xgV9f6x82Rks0uNczv6JgQiREBACQkAICAEhIASEgBAQAo1FQKqSjcW7Q+SGSeSPEsMPSN9GG310bwBhyqmn9h+v7RAVUCGFgBAQAkKgUyPApzd+GTLETTjRRAWWUDt1pVU5ISAEOi0C5apKinHrtF1AFRMCQkAICAEhIASEgBAQAkKg1REol3GTqmSrt6TKJwSEgBAQAkJACAgBISAEhMAIj4AYtxG+CwgAISAEhIAQEAJCQAgIASEgBFodATFurd5CKp8QEAJCQAgIASEgBISAEBACIzwCYtxG+C4gAISAEBACQkAICAEhIASEgBBodQTEuLV6C6l8QkAICAEhIASEgBAQAkJACIzwCIhxG+G7gAAQAkJACAgBISAEhIAQEAJCoNUREOPW6i2k8gkBISAEhIAQEAJCQAgIASEwwiMgxm2E7wICQAgIASEgBISAEBACQkAICIFWR0CMW6u3kMonBISAEBACQkAICAEhIASEwAiPgBi3Eb4LCAAhIASEgBAQAkJACAgBISAEWh0BMW6t3kIqnxAQAkJACAgBISAEhIAQEAIjPAJdhiY0wqMgAISAEBACQkAICAEhIASEgBAQAi2MgCRuLdw4KpoQEAJCQAgIASEgBISAEBACQgAExLipHwgBISAEhIAQEAJCQAgIASEgBFocATFuLd5AKp4QEAJCQAgIASEgBISAEBACQkCMm/qAEBACQkAICAEhIASEgBAQAkKgxREQ49biDaTiCQEhIASEgBAQAkJACAgBISAExLipDwgBISAEhIAQEAJCQAgIASEgBFocATFuLd5AKp4QEAJCQAgIASEgBISAEBACQkCMm/qAEBACQkAICAEhIASEgBAQAkKgxREQ49biDaTiCQEhIASEgBAQAkJACAgBISAExLipDwgBISAEhIAQEAJCQAgIASEgBFocATFuLd5AKp4QEAJCQAgIASEgBISAEBACQkCMm/qAEBACQkAICAEhIASEgBAQAkKgxREQ49biDaTiCQEhIASEgBAQAkJACAgBISAExLipDwgBISAEhIAQEAJCQAgIASEgBFocATFuLd5AKp4QEAJCQAgIASEgBISAEBACQkCMm/pAisDXX3+d3uumMgS+++47988//1QWSaGFQJ0Q+OWXX9xvv/1Wp9SVrBAQAu1BQO/a9qCnuEJgxEagqYzbv//+69577z136623uuOPP95dcMEF7tFHH3UsgptFP/74o3v77bfdhx9+2KwipPn279/fzT333G6DDTZI3ep1s9tuu7lFF13UHXDAAfXKomHpnnzyyR63Qw89tCF5XnnllW6hhRZyyy+/vPvjjz8akqcyaSwC33zzje9TjEfmrFamZ5991pd1kUUW8XNZvcvayHnK6rLsssv6Og4aNMic6nJdb731fD4333xzXdLvSIk2el7tSNhUUtbO9K6tpN4KKwQ6KwKffvqpf9d+9tlnDali14bkkpHJK6+84rbZZhv37bffZvg6x+S25557upFHHjnTv16OLEKOO+44N9FEE7mnn366XtmUle7vv//u2DmvNyP7559/urvuusuXifqfdNJJrkuXLmkZYWL/+usv161bNzfuuOOm7uXc/PTTT+6rr75yo4wyipt22mnLidLuMEOGDPG4kXcj6N577/XZfPTRR+6dd95xc845ZyOyVR4NRODvv//2fYosuW8EVTvu2PyCmDuYw2aeeea6FrdR81RYCd4b1I+860mWz6+//lrPbGqSNv3ygw8+8GlNN910rmvXyl7vX375pWPuHGeccdykk07apkyNnlfbFKATOJR613aCKqoKQmCEQYA59+yzz3Z9+vTxdV5sscVcv3796l7/pkjcBg8e7NZaa61cpo1aA8auu+7asEVS3ZFu4QxGHXVUh3Rq+umnd8ccc0wB00ax11hjDbfSSiu522+/veJaEIe4pNFZaccdd3SzzTab23DDDd0cc8zRWaupejUYgWrH3dprr+14gSy99NJ+7DW42MquSQggCWau5VeNVPjYY4/1cbmK6oNAqXdtfXJVqkJACNQaATbqN9poo5Rpq3X6xdKrbEuuWEpl+sGhbrvttgWhUTGbf/753fvvv+9uvPHG1O+ee+5xzz33nEPlR1RfBLbbbjvHT1Q5AksssUQqsaw8tmIIgdoigGS7Ebt+tS21UhMCIwYCeteOGO2sWnZeBDjetffee6cVnGaaaRyMXKOo4RK3F198saBue+21l7vooovc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ATNuc9IQLoYRMAJGwAgYASNgBIyAETACRqAOATNudcj4vhEwAkbAsqjhDQAAPv1JREFUCBgBI2AEjIARMAJGYE4QWHvcclx44YXjRnU8I2AEjIARMAJGwAgYASNgBIyAEViNwDrrrNMIB2vcGsHkQEbACBgBI2AEjIARMAJGwAgYgdkhYMZtdtg7ZyNgBIyAETACRsAIGAEjYASMQCMEzLg1gsmBjIARMAJGwAgYASNgBIyAETACs0PAjNvssHfORsAIGAEjYASMgBEwAkbACBiBRgiYcWsEkwMZASNgBIyAETACRsAIGAEjYARmh4AZt9lh75yNgBEwAkbACBgBI2AEjIARMAKNEDDj1ggmBzICRsAIGAEjYASMgBEwAkbACMwOATNus8PeORsBI2AEjIARMAJGwAgYASNgBBohYMatEUwOZASMgBEwAkbACBgBI2AEjIARmB0CZtxmh71zNgJGwAgYASNgBIyAETACRsAINELAjFsjmBzICBgBI2AEjIARMAJGwAgYASMwOwTMuM0Oe+dsBIyAETACRsAIGAEjYASMgBFohIAZt0YwOZARMAJGwAgYASNgBIyAETACRmB2CJhxmx32ztkIGAEjYASMgBEwAkbACBgBI9AIATNujWByICNgBIyAETACRsAIGAEjYASMwOwQMOM2O+yd8zJG4LzzzlvGtXPVjEA/CFx44YXVP/7xj34ycy5zh8B///vf6t///vfclWvSAnl+mBRBxzcCKxeBtWdZ9f/85z/VGWecUf34xz+uzj777Ora1752tcUWW1Sbb755dYUrXGGWRZso73POOae64IILRqZBHTfaaKOR4RYpwB/+8Idqxx13TEV+73vfW13vetdbpOJ3UtZnPvOZ1Sc+8YnqAQ94QPXiF7+4kzTnJRHe03/+85/V1a9+9Wr99dcfFIv3mEVWG9pkk02qy13uctU89ZmLLrqoOuuss1I1rnrVq1b8mhB1BwNo3XXXra55zWs2ieYwQxD43ve+Vz3iEY+ornjFK1bvete7qhvc4AZDQjd7VNd/m8V2qL4QYPx85zvfWX3rW99KWb7sZS+rdtppp76yn2o+y3l+mCpwTtwIzCkCv/nNbyqEjMxVG2644dRLOTPG7TOf+Uz11Kc+tbaCBxxwQPXIRz6yWmuttWrDzOuDVatWVaeccsrI4t30pjetYG6WEyEd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DgLsueNzNXi1xKNpk+8aTqckTtUIGAEjsNgINN3jZsZtsdvZpTcCRsAIGAEjYASMgBEwAkZggRFoyrjZVHKBG9lFNwJGwAgYASNgBIyAETACRmBlIGDGbWW0s2tpBIyAETACRsAIGAEjYASMwAIjYMZtgRvPRTcCRsAIGAEjYASMgBEwAkZgZSBgxm1ltLNraQSMgBEwAkbACBgBI2AEjMACI2DGbYEbz0U3AkbACBgBI2AEjIARMAJGYGUgYMZtZbSza2kEjIARMAJGwAgYASNgBIzAAiNgxm2BG89FNwJGwAgYASNgBIyAETACRmBlIGDGbWW0s2tpBIyAETACRsAIGAEjYASMwAIjYMZtgRvPRTcCRsAIGAEjYASMgBEwAkZgZSBgxm1ltLNraQSMgBEwAkbACBgBI2AEjMACI2DGbYEbz0U3AkbACBgBI2AEjIARMAJGYGUgsNbFq2llVNW1NAJGwAgYASNgBIyAETACRsAILCYC1rgtZru51EbACBgBI2AEjIARMAJGwAisIATMuK2gxnZVjYARMAJGwAgYASNgBIyAEVhMBMy4LWa7udRGwAgYASNgBIyAETACRsAIrCAEzLitoMZ2VY2AETACRsAIGAEjYASMgBFYTATMuC1mu7nURsAIGAEjYASMgBEwAkbACKwgBMy4raDGdlWNgBEwAkbACBgBI2AEjIARWEwEzLgtZru51EbACBgBI2AEjIARMAJGwAisIATMuK2gxnZVjYARMAJGwAgYASNgBIyAEVhMBMy4LWa7udRGwAgYASNgBIyAETACRsAIrCAEzLitoMZ2VY2AETACRsAIGAEjYASMgBFYTATMuC1mu7nURsAIGAEjYASMgBEwAkbACKwgBMy4raDGdlWNgBEwAkbACBgBI2AEjIARWEwEzLgtZru51EbACBgBI2AEjIARMAJGwAisIATMuK2gxnZVjYARMAJGwAgYASNgBIyAEVhMBMy4LWa7udRGwAgYASNgBIyAETACRsAIrCAEzLitoMZ2VecbgYsuuqi6+OKLWxfywgsvrP7+97+3jrcSIpx//vnVf/7zn4Wq6r///e81yryI9Vgo0FdIYZv0I94X+mBT8vjTFCmHMwJGwAhMjsBcMG4sOn/605+u8RtnETs5JE5hXAR+97vfVV/72teq008/fdwk5iLegx/84OpmN7tZ9cEP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" alt="image.png"></p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>I will do the same operations for the test dataset with the following lines:</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[9]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">j</span> <span class="ow">in</span> <span class="n">test</span><span class="o">.</span><span class="n">take</span><span class="p">(</span><span class="mi">1</span><span class="p">):</span>
  <span class="n">test_feat</span> <span class="o">=</span> <span class="n">j</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">numpy</span><span class="p">()</span>
  <span class="n">test_lab</span> <span class="o">=</span> <span class="n">j</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">numpy</span><span class="p">()</span>

<span class="n">test</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">([</span><span class="n">test_feat</span><span class="p">,</span> <span class="n">test_lab</span><span class="p">])</span><span class="o">.</span><span class="n">T</span>
<span class="n">test</span><span class="o">.</span><span class="n">columns</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;DATA_COLUMN&#39;</span><span class="p">,</span> <span class="s1">&#39;LABEL_COLUMN&#39;</span><span class="p">]</span>
<span class="n">test</span><span class="p">[</span><span class="s1">&#39;DATA_COLUMN&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">test</span><span class="p">[</span><span class="s1">&#39;DATA_COLUMN&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">str</span><span class="o">.</span><span class="n">decode</span><span class="p">(</span><span class="s2">&quot;utf-8&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="First-5-rows-of-test-dataset:">First 5 rows of test dataset:<a class="anchor-link" href="#First-5-rows-of-test-dataset:">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">test</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><img src="data:image/png;base64, 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dD0iIgogICAgICAgICAgICB4bWxuczpleGlmPSJodHRwOi8vbnMuYWRvYmUuY29tL2V4aWYvMS4wLyIKICAgICAgICAgICAgeG1sbnM6dGlmZj0iaHR0cDovL25zLmFkb2JlLmNvbS90aWZmLzEuMC8iPgogICAgICAgICA8ZXhpZjpVc2VyQ29tbWVudD5TY3JlZW5zaG90PC9leGlmOlVzZXJDb21tZW50PgogICAgICAgICA8ZXhpZjpQaXhlbFhEaW1lbnNpb24+ODYwPC9leGlmOlBpeGVsWERpbWVuc2lvbj4KICAgICAgICAgPGV4aWY6UGl4ZWxZRGltZW5zaW9uPjMyODwvZXhpZjpQaXhlbFlEaW1lbnNpb24+CiAgICAgICAgIDx0aWZmOlJlc29sdXRpb25Vbml0PjI8L3RpZmY6UmVzb2x1dGlvblVuaXQ+CiAgICAgICAgIDx0aWZmOlhSZXNvbHV0aW9uPjE0NC8xPC90aWZmOlhSZXNvbHV0aW9uPgogICAgICAgICA8dGlmZjpZUmVzb2x1dGlvbj4xNDQvMTwvdGlmZjpZUmVzb2x1dGlvbj4KICAgICAgICAgPHRpZmY6T3JpZW50YXRpb24+MTwvdGlmZjpPcmllbnRhdGlvbj4KICAgICAgPC9yZGY6RGVzY3JpcHRpb24+CiAgIDwvcmRmOlJERj4KPC94OnhtcG1ldGE+CkdQ0SUAAEAASURBVHgB7J0FuBw1F4ZTKG7F3d3doUBxdyilyI+UFqcUKcWdAoUWdygOxd1KcdfiXtzd9d837Zlm587s7szu3r13+5377B3LZJJ3MpmcnJNMh/8K4iQiIAIiIAIiIAIiIAIiIAIiIAI1JzBWzWNUhCIgAiIgAiIgAiIgAiIgAiIgAp6AFC4VBBEQAREQAREQAREQAREQARGoEwEpXHUCq2hFQAREQAREQAREQAREQAREQAqXyoAIiIAIiIAIiIAIiIAIiIAI1ImAFK46gVW0IiACIiACIiACIiACIiACIiCFS2VABERABERABERABERABERABOpEQApXncAqWhEQAREQAREQAREQAREQARGQwqUyIAIiIAIiIAIiIAIiIAIiIAJ1IiCFq05gFa0IiIAIiIAIiIAIiIAIiIAISOFSGRABERABERABERABERABERCBOhGQwlUnsIpWBERABERABERABERABERABKRwqQyIgAiIgAiIgAiIgAiIgAiIQJ0ISOGqE1hFKwIiIAIiIAIiIAIiIAIiIAJSuFQGREAEREAEREAEREAEREAERKBOBKRw1QmsohUBERABERABERABERABERABKVwqAyIgAiIgAiIgAiIgAiIgAiJQJwJSuOoEVtGKgAiIgAiIgAiIgAiIgAiIgBQulQEREAEREAEREAEREAEREAERqBMBKVx1AqtoRUAEREAEREAEREAEREAEREAKl8qACIiACIiACIiACIiACIiACNSJgBSuOoFVtCIgAiIgAiIgAiIgAiIgAiIghUtlQAREQAREQAREQAREQAREQATqRKBjneJVtCIgAiIgAiJQcwIffvih++OPPxLjHX/88d3UU0/tWGaVd955x/3333/uk08+cZNNNpmbeeaZ3VRTTdUimo8//tj99ttvLfaX2zHHHHO4scceuyjY77//7j766CO/7+2333aEmWWWWdyEE05YFK4eG//88497/PHH3fvvv+8+/fRTN8EEE7hFFlnELbzwwon5TkvDX3/95R599FH3wQcfuM8++8x17NjRTT/99G7OOed0yy67bIs8h/F888037ttvv412zTrrrG7ccceNttNWvv76a/fdd99Fh0ud99577znyiow33nier53466+/+vtt2yznmmsu16FDh3BXi3XuGffOZPLJJy9iFuZrookmcjPMMIMFbbH88ssv3Q8//OD3c12u31ry77//unfffTe63CSTTOKmm266aDvLSp6ybPy/+uorBzOu3alTp+iy3K8ZZ5yxZBkqVR9EEY1a4bmeZpppot3huTybPH+tKT///LN75JFHfB3wxRdf+HLCM7jgggtmqgO+//57Hw91F+Vp0kkn9c8gcc0///wls5SXQaXn/fnnn27EiBFRGko9KwSi7qbuLSXU09TXoVBOwnozTB/1ONdNE9JHOpFyz2taHJXs71BI+H+VBFQYERABERABEWg0gfXWW8+98cYbJZNBw23rrbd2W265ZcnGrkWCstClSxfb9MuVVlrJDR48uGgfG5tssol7+eWXW+wvt+PBBx90KAahDBkyxB144IHhLr/ds2fPon213rjuuuvc6aef7j7//PPEqGeffXY3aNAg3/BLDFDYiRJzwQUXuLPOOsv98ssvicG4D3vvvbfr2rVr4vHjjjvOXXTRRdGxW265xSt80Y6UlWOOOcZdcskl0dHbbrstNa1hI3ruued299xzT3Te/fff73r06BFts3L99de7JZdcsmhfuIGyvcwyyxTleaeddnKHHnpoFCyeL64TpiMKWFg5+OCDHffDBMU7rpjbsVovUVrDvK6++ur+nua5Tp6ynMQ/6dqksXv37m7jjTducbiS+sBO2mqrrdyJJ55omy5+Lsp5awgdRqeddpo7//zzUy+3yiqruAEDBpRUFFDUTzrpJHfNNdekxoPS1a9fP7f00ksnhsnLYO2113aUVZM0dq+88orbaKONLJgr96yg8Dz99NO+Ayg6KbbywgsvuM0337xo77nnnuvWWmutaF+YL577m2++OTXOFVZYIaoLl1tuOXfVVVdF8dRyRS6FtaSpuERABERABBpOAEVi4MCBDqUpbGCnJezOO+9scQirDT3v9RQaAXG56aab4rtqto2SdNhhh/lGfpqyxcWwem244Ybu3nvvTbw2ChaKSv/+/YsUj3hgrnHIIYd4JfLvv/+OH26T20n3JEwoinOaghmGC9f33HPPVKtsGK49rydxq1VZfu6559x+++3njj/++PaMyKcdJbdbt24llS0CPvTQQ27TTTdtYckxACg4KKCllC3C0jlE51O9lAhLT62WPFso4qUka7lCMUQxbbRI4Wr0HdD1RUAEREAE6kagV69e3t2m1AVuuOGGxMNJylpe68NYYxW/bnEhwqUvLjQOylnw4udUuk2j68orr2wRnB7gxRdfvMV+LG133XVXi/1YcFA84jLffPMVuezZcawf5513nm226SV8SrmMhtaoSjPC/Tz55JMrDd7uwtWyLK+55pqO30ILLdSCw4UXXhi54LY4WMGOvM9uBVFXHARrExaauGDFw7IcCm5xKF2hSx7Hcd+kXuN4XIgHK1FcsMBiOWoPgpU5TXg2sypcxIW3wn333ZcWbavsL34DtMoldREREAEREAERqA0BfPn50YjBzYyGSFx69+6dapV4/fXXvUUnfg7buLjFBeXBrmlL3H9CoUfejtkyPi4hzXpEPHfffXcYXU3WGdtxxBFHFMW12mqrecUJxRKl88UXX3TsCwX3PcZpmaAkxnvVcdXCIoilcNiwYb6HGve0UE499dSi8ULhsba2ntbDzhi1hx9+OFdyL774Ys8m18lt/KRalWWUAhRzfrfe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w5K14IILZv7OG814pn9n3NR3333nXS55Buk0QClqLWHsJOPuvvrqK29NQ0HKYlVurXQ26jpSuBpFXtcVAREQAREQgQoJ4FaY1/2FRtfw4cMrvJKCiYAIJBE45JBDiia9SAqTto9xWOFse2nhtL95CcilsHnvrXImAiIgAiIgAiIgAiIgAiLQYAJSuBp8A3R5ERABERABERABERABERCB5iUgl8LmvbfKmQiIgAiIQJMQYGxG0oeKK8ke37ZiSmqJCIhAfgIjRoyIxilmjYXxWbWcJTDr9RW+8QSkcDX+HigFIiACIiACIiACIiACIiACTUpALoVNemOVLREQAREQAREQAREQAREQgcYTkMLV+HugFIiACIiACIiACIiACIiACDQpASlcTXpjlS0REAEREAEREAEREAEREIHGE5DC1fh7oBSIgAiIgAiIgAiIgAiIgAg0KQEpXE16Y5UtERABERABERABERABERCBxhOQwtX4e6AUiIAIiIAIiIAIiIAIiIAINCkBKVxNemOVLREQAREQAREQAREQAREQgcYTkMLV+HugFIiACIiACIiACIiACIiACDQpASlcTXpjlS0REAEREAEREAEREAEREIHGE5DC1fh7oBSIgAiIgAiIgAiIgAiIgAg0KQEpXE16Y5UtERABERABERABERABERCBxhPoWC4JQ4cOLRdEx0VABERABERABERABERABERgjCTQpUuXkvmWhaskHh0UAREQAREQAREQAREQAREQgfwEOvxXkFKnf/rLv6UO65gIiIAIiIAIiIAIiIAIiIAIjLEEZpiotA2r9NExFpsyLgIiIAIiIAIiIAIiIAIiIALVE5DCVT1DxSACIiACIiACIiACIiACIiACiQSkcCVi0U4REAEREAEREAEREAEREAERqJ6AFK7qGSoGERABERABERABERABERABEUgkIIUrEYt2ioAIiIAIiIAIiIAIiIAIiED1BKRwVc9QMYiACIiACIiACIiACIiACIhAIgEpXIlYtFMEREAEREAEREAEREAEREAEqicghat6hopBBERABERABERABERABERABBIJSOFKxKKdIiACIiACIiACIiACIiACIlA9ASlc1TNUDCIgAiIgAiIgAiIgAiIgAiKQSEAKVyIW7RQBERABERABERABERABERCB6glI4aqeoWIQAREQAREQAREQAREQAREQgUQCUrgSsWinCIiACIiACIiACIiACIiACFRPQApX9QwVgwiIgAiIgAiIgAiIgAiIgAgkEpDClYhFO0VABERABERABERABERABESgegJSuKpnqBjaKYHffv3V/f77b+009Uq2CIiACIiACIiACIhAeyDQKgrXjz987+667WZ34VkD3cD+x7khV13uXhv+UnvgUzaNI95/1733ztvu559/Khu2PQX45KMPfb64d7WUs0/r71ZfZlF34lGH1jLa1Li+/eZrfz2uOeKD96JwlL8uyyzi1u+8nHvnrTei/c28ksaimfM8puftkQcf8OV/q/XXbPMoWrtuaPNAGpDAXbpt4csL72uJCIiACDQbATrZh957l7vkvLPcRWcPcvfddXurtd871hvmFZdc4M469aTEyyyz/Iru0OP6u6mnmTbxeHvY2XXDtX0yDz/+ZLfuRpu2hyRXlMZdt93SffftN27XPfd1O/Xcs+icn3760X3z1VeuY8eObqZZZi06Vm7jl59/dr/++ov7+ccfywWtyfF//vnHX4/I/v7r7yjOZ558wq+TlheffcbNNc980bH2vPLxhyPc33//7aacemo3ySSTFmUljUVRoBpvlEpPjS+l6BII/PHH7yPL/1dfJhzNv6se97W164a03PP8kD+E+o16bkwR6nzqxN8L1n+JCIiACDQTgWeffNwdfuB+vm0b5mvCCSdy/Y490XVZa91wd83X62rhOvv0k1OVLXLy9BOPuZ7bd3Vff/lFzTOmCKsjMPGoxvp4443fIqL777zdbbPR2m6HLTZqcay97Fh7/Q3dEksv61D6V11jrfaS7LLp5J5wb7hHbUHaWnraApNmSEMz39cR77/nnyGeI9YlIiACIiAC7ZvA66+87PbaZftI2Vpng43d+pts7lC26GTq13sv98QjD9U1k3VTuF5+4Tl3+YXnFSV+3vkXdOtsuEnRvk8//sidftJxRfu00XgCE044oU/E+BO0VLgan7rqUzDdDDO6sy650g284DI3VTu2sFZPQjGIgAiIgAiIgAiIQHMS+O+//9xJRx0WZe6a2+91R5x4qjv02JPctYX1yaeY0h878ch+7s8//4zC1XqlbgrX2aedXJTWHnvt5y69/hZ3xAmnuFseeLTo2AP33Oneev21on1j0sZvv/0Wad2V5psJH3768YdKgxeF++brrxzu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IAIiIAIiIAIiMGYQkMI1Ztxn5VIEREAEREAEREAEREAERKABBKRwNQC6LikCIiACIiACIiACIiACIjBmEJDCNWbcZ+VSBERABERABERABERABESgAQSkcDUAui4pAiIgAiIgAiIgAiIgAiIwZhCQwjVm3GflUgREQAREQAREQAREQAREoAEEpHA1ALouKQIiIAIiIAIiIAIiIAIiMGYQkMI1Ztxn5VIEREAEREAEREAEREAERKABBDqWu2anDr+XC6LjIiACIiACIiACIiACIiACIjCGEpiwZL5l4SqJRwdFQAREQAREQAREQAREQAREID8BKVz52elMERABERABERABERABERABEShJQApXSTw6KAIiIAIiIAIiIAIiIAIiIAL5CUjhys9OZ4qACIiACIiACIiACIiACIhASQJSuEri0UEREAEREAEREAEREAEREAERyE9ACld+djpTBERABERABERABERABERABEoSkMJVEo8OioAIiIAIiIAIiIAIiIAIiEB+AlK48rPTmSIgAiIgAiIgAiIgAiIgAiJQkoAUrpJ4dFAEREAEREAEREAEREAEREAE8hOQwpWfnc4UAREQAREQAREQAREQAREQgZIEpHCVxKODIiACIiACIiACIiACIiACIpCfgBSu/Ox0pgiIgAiIgAiIgAiIgAiIgAiUJCCFqyQeHRQBERABERABERABERABERCB/ASkcOVnpzNFQAREQAREQAREQAREQAREoCQBKVwl8eigCIiACIiACIiACIiACIiACOQnIIUrP7umPfPrr79u2rzVImP//POP+/7772sRleIQAREQgTZD4Ntvv3X//vtvm0lPPRPy66+/ut9//72el1DcIiACIhARaIjC9eeff7p33nkn+n366adRgrQyksB7770X8QlZlVr/448/InzdunVzyyyzjLv11lujfZWs9O7d262yyiquX79+lQQf48Lwkl5zzTXdiiuu6G666aYG4rFeAABAAElEQVS65v/BBx/093D99dfPfJ0BAwb4c4888sjM545pJ1TDOS+rX375xT/f77//ft4oxtjz8tZtYyywCjN+9dVXu5VXXtmtu+66LnyXVHh6YrC2eq+GDx/ull56ade5c2f31ltvJaZdO0VABJqPAJ0s9957rzv33HPd2Wef7e688073008/tUpGO7bKVYKLvP322+7AAw8squSo+C699NIg1Ji9ystuww03zAzhqquucosuuqg/75tvvnE06n777beK40ERvueee3z4m2++2R177LGuQ4cOFZ8/JgR888033RdffOGzSkN90003rVu2qRi4h3mE8/i1VkWSJ41t5ZxqOKfl4cMPP3R///23m3rqqd0kk0zSItgDDzzg+vbt6/e/9NJLrmPHVq+KW6SpVjsoc1999ZXP0yyzzJI52nLs8tRtmRMRnPDll1+6n3/+2U088cRummmmCY7UZ7Vc/utzVecok8jHH3/s6PCbf/75q75U3nvFswMHhDJU6+fjySef9HFTRz777LNunnnm8dv6JwIi0LwEeO4POOAAhyU/lIkmmsi3d9daa61wd83XW83ChZvC4MGD3SabbFKkbNU8R00QYV4lZ6yxqrud4447rleGZ5ttNnfYYYdJ2UooS4sssohXhhdYYAG3ww47JITQLhFwbosttvDlhN6zJBlvvPGi3bVuTEYRN2iFPNNhBIM8Uo5dnjirOeekk07y+WHZGtKo/O+8885e8dhss83cfPPN1xpZTb0Gll/KEL96WIHxGqCjd/nll3drrLFGajp0QAREoDkIvPLKK446zpQt6hb0EZQtOl72228/98gjj9Q1s63SrUoPIVatZ555pq6ZaZbIUXxeffXVFtnp37+/u+yyy7wVC2tWPQQlQopEOtmxxx7bnXjiiekBdEQEKiAw/vjj+1BU9hIRaAsEUD7q7SbdFvJJGmaYYQZ51bSVm6F0iECdCfz333/uqKOOiq5y++23u9lnn91v77PPPm7zzTf3itgRRxzh7r77bkcbvB5SnUmkwhQ9/vjjRcrWQgstVOGZClZLArgM/vjjj1VHSeFlYg0mj6iVEJf1PCTF+d1332UeV9DoAeC4IdWCd5wHcdYy3kZyYvKR9jJwnXJPOaxFes3CZcv4PQ63a8kITwOeXfKSVXB1xkWsLUqeuo3xmLV8jspxwU0OfnnYl4ubMlJqIp9a5pVy8MMPP5RLUurxPPcqNbIKD/B+wRWca2eRap6XLNdRWBEQgfoRwNjz2muv+QugYJmyxQ7cxPv06eOPUUfYsBq/o8b/WsXCFaZ5//33d127dvXm/HC/1utH4LHHHnMXXXSRe+qpp/xFcBlcaaWVHBNkxBt8xxxzjB9QiMa/7777FiXqhRdecOecc4578cUXo7FF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88/ebY4GaJLykSUuC0vDFSsajy0VSKVKrp0fXzaSEw198gKb+CDWeDrbyjbjFBlgS9mvpFzhBmUf0rWGfpa8VMsIVyzSTMM3dDWzNHD/cWWihx3FqpR1kbLH+CDuF5NAxBuqFme4JH7eIczMaY3r8Hip9WrZpcVNvDZehvohS7oYHwoH8lNJ/sM0MKMoZYEZICuZjKcW+a8mr5Z2eoUph3w3LN7JQhjq2XXXXdcHx4qaNGmRxZVnCW+4UdeVG6eaJ/7wnGqfF8o7dbMpmmHcpY4RDsaV1ClhnFoXARHIToDn3D6Tgws3MxNmrc+TrlpuBmopXEnUtE8EREAEmoAAVi1zg8Pllska7MWCdRELHe51CGGxykhEICTA2FMrI/QQm/UeZY7p9I8//njvqokFMM+EQOG1Gr2u56XRd0DXF4H2S0AKV/u9d0q5CIiACFRFgF51xmLZmBusbMzYxIeaw1nwunbt6sfiVHUxndyUBEILFhlEseJDoky8Y5OPsJ8xXllmduWctiZ6XtraHVF6RKD9EJDC1X7ulVIqAiIgAjUngAswYwAZH5cklUwAkXSe9o05BN577z3Xt29fr2TFc824JSZWYVbPZhA9L81wF5UHEWh9AlK4Wp+5rigCIiACbY4A1gj81rF2MVaECU5mnnnmiidxaXMZUoJalQAuhMxMSxlizB/jLilD8Rk6WzVRdbyYnpc6wlXUItCEBKRwNeFNVZZEQAREQAREQAREQAREQATaBoFyCpfmY28b90mpEAEREAEREAEREAEREAERaEICUria8KYqSyIgAiIgAiIgAiIgAiIgAm2DgBSutnEflAoREAEREAEREAEREAEREIEmJCCFqwlvqrIkAiIgAiIgAiIgAiIgAiLQNghI4Wob90GpEAEREAEREAEREAEREAERaEICUria8KYqSyIgAiIgAiIgAiIgAiIgAm2DgBSutnEflAoREAEREAEREAEREAEREIEmJCCFqwlvqrIkAiIgAiIgAiIgAiIgAiLQNghI4Wob90GpEAEREAEREAEREAEREAERaEICUria8KYqSyIgAiIgAiIgAiIgAiIgAm2DgBSutnEflAoREAEREAEREAEREAEREIEmJNDhv4I0Yb6UJREQAREQAREQAREQAREQARFoOAFZuBp+C5QAERABERABERABERABERCBZiUghatZ76zyJQIiIAIiIAIiIAIiIAIi0HACUrgafguUABEQAREQAREQAREQAREQgWYlIIWrWe+s8iUCIiACIiACIiACIiACItBwAlK4Gn4LlAAREAEREAEREAEREAEREIFmJSCFq1nvrPIlAiIgAiIgAiIgAiIgAiLQcAJSuBp+C5QAERABERABERABERABERCBZiUghatZ76zyJQIiIAIiIAIiIAIiIAIi0HACUrgafguUABEQAREQAREQAREQAREQgWYlIIWrWe+s8iUCIiACIiACIiACIiACItBwAlK4Gn4LlAAREAEREAEREAEREAEREIFmJSCFq1nvrPIlAiIgAiIgAiIgAiIgAiLQcAJSuBp+C5QAERABERABERABERABERCBZiUghatZ76zyJQIiIAIiIAIiIAIiIAIi0HACUrgafguUABEQAREQAREQAREQAREQgWYlIIWrWe+s8iUCOQj8+uuv7rfffstxpk4ZEwh8++237p9//mm6rJKn7777runyVa8MffXVV/WKWvGKgAiIQFMSaBWF699//3Xvvfeeu+WWW9zxxx/vzjvvPPfYY485Xt5jgvAif/vttzP9PvvsswjN/fff7xZeeGG3+uqrR/vG9JUhQ4Z4JltuuWVmFAcffLA/9+STT858bns4IW95eemll9xCCy3klllmGffGG2+0h6xWnMb+/fv7e96vX7+Kz2nWgHnLx+WXX+6WWmopXw/98ccfdcNDY5760upAOgCs/vzvv/9qfl06GVZeeWW35JJLOuqVUDbffHNfbm666aZwd7tc/+WXXzzHd999N0q/cYVBpbLnnnu6ZZdd1h144IGVnlKXcHqm64JVkYpAUxPgfXLXXXe5M8880w0cONDddttt7qeffmqVPHes91VeeeUV97///c998803iZei8t5nn33c2GOPnXi8GXYOHjzY39gseencubO79NJL/Sm///6742X55ZdfZomiqcMakzxK+88//+x5wrRR8sUXX/iHfJJJJnHTTjttpmT8/fff7oMPPvDnzDbbbK5jx+LH2NhkLS+PP/64jxMuTz/9tJtvvvkypastB6ZCJV8//vhjW05mlLYRI0a4v/76y00zzTRu0kknjfZXskIeuffjjDOOm3XWWVuckrd83HfffT6uDz/80L3zzjtuwQUXbBF3LXaccsop7vrrr3fLLbecu+qqq9xTTz3ldtppJx/1k08+6ZmE16mGFfG8/vrr7vPPP/dRooxuscUWUfS8tyg3WRSS6OScK+XuX85o3b333uv2339/f/pbb73lKAdrr7223z7rrLPcuuuuWzbqP//80915550+HMrpSSed5Dp06FD2vDwBytWRrf1Ml0tPnjzqHBEQgdYjQBsHfSOuj0w00USODpxK6sBqUltXC9ewYcPcRhtt1CJzYYLRMvfYYw9HI7JZJY8ySWNJ0rwEjj32WLfWWms5llkFazHn8mO9VsKzSiN3pZVWihpitYpb8WQjsMEGG/j7S+9bVuEcygZx1FJ22203r4RvtdVWboEFFqhl1EVxTTDBBH57vPHG88vxxx8/Om77oh2FlWpYEc9iiy3mNtlkE2/d3XnnncOoG7Jer/sXsqOTJtwOGZfK9LjjjuuwEs8+++zumGOOqZuyRRqqqSNL5SHvsbaWnrz50HkiMCYSePnll1337t0jfYQ6n841lC061dBD0FnqKcVd4zW8EgqU9UpatLjELb744u799993N9xwg+32PW/PP/+8d2WKdjbRClY8fqHgZogLC4Krzoorrhge1roItDqBGWec0VsUWv3CumC7IEAdZdaNeibYFC5ehEioDITrtUoDHWIDBgyoVXRtNp4417BTL1S+ymUApbQtKKbl0qnjIiACIgABXNEPPfTQCAaeDHPMMYffxupPpx1Wr0MOOcQrXXQs1UPqZuFiPEgo++67r7vgggvc7rvv7hg7c8IJJ4SH665ZFl2sSTayDmBnYDiuRrUa9E4hZrxFlvhQxL/++utMd4D4cefIch27AP66pDHP2A/GqWRNax4mltZ6L7OWl3Lp+eGHHzJPsEGlVmtrNp0XeSb6sHuV9VzKYR5X1nI8G328VuUD9zvKRl4xpcqUANsmvlq9CCkz/PJINfVRnuuVO6fSeiqJp8Vtx2y7Fsu8z2U112a8eNY6u9ryWk16da4IiED9CeCKzvAmpE+fPpGyxTZDOvr27cuqdy2vZ6di3RQuJsUIZbvttgs3W7i7vPjii0XHtZFMAL/7I4880q2wwgp+APvcc8/tdtxxRz8JSfIZzhe0XXfd1REWlzFcaFCAmcQkjzz33HP+mosssogfPE28uKOlDSyngXL++ee79dZbz80zzzzekskkIOXS/eabb/qeVOJffvnlffoZD1jJhA70YHA9xpkwwJu0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AkbACBgBI2AEjIARMALdIWCBqztsnbMRMAJGwAgYASNgBIyAETACM46ABa4ZHwBuvhEwAkbACBgBI2AEjIARMALdIWCBqztsnbMRMAJGwAgYASNgBIyAETACM46ABa4ZHwBuvhEwAkbACBgBI2AEjIARMALdIbD8oKxvuOGGQUl83wgYASNgBIyAETACRsAIGAEjMJMIrLjiin3bbQtXX3h80wgYASNgBIyAETACRsAIGAEj0B4BC1ztsfOTRsAIGAEjYASMgBEwAkbACBiBvghY4OoLj28aASNgBIyAETACRsAIGAEjYATaI2CBqz12ftIIGAEjYASMgBEwAkbACBgBI9AXAQtcfeHxTSNgBIyAETACRsAIGAEjYASMQHsELHC1x85PGgEjYASMgBEwAkbACBgBI2AE+iJggasvPL5pBIyAETACRsAIGAEjYASMgBFoj4AFrvbY+UkjYASMgBEwAkbACBgBI2AEjEBfBCxw9YXHN42AETACRsAIGAEjYASMgBEwAu0RsMDVHjs/aQSMgBEwAkbACBgBI2AEjIAR6IuABa6+8PimETACRsAIGAEjYASMgBEwAkagPQIWuNpj5yeNgBEwAkbACBgBI2AEjIARMAJ9EbDA1Rce3zQCRsAIGAEjYASMgBEwAkbACLRHwAJXe+z8pBEwAkbACBgBI2AEjIARMAJGoC8CFrj6wuObRsAIGAEjYASMgBEwAkbACBiB9ghY4GqPnZ80AhONwG9/+9uJrl/Xlbvuuuuq//znP10XMyf/f/zjH9WNN94459pi1GNOBfzDCLREgPfnX//6V8unh3ts1uer4dByaiNgBKYNgbEIXP/+97+rK664ovrsZz9bHXXUUdWnPvWp6jvf+U7117/+ddrwmrr6/vrXv65+9KMfVddcc828uv/85z9P9/74xz/Ou7csX/jyl79cPexhD6ue/OQnL7PNfMUrXlFtsskm1f777z/VbWzbVyeddFL1qEc9qtpss82qv//9751i8Kc//al69atfXT32sY+tHvzgB1ePe9zjeuXV1eMd73hHGoMHH3xwL61PRo8A8965555bnXzyydVFF11U0VemwQicfvrp1XOf+9zq/ve/f/XABz6wOu200wY/tIAUkzJf/e53v0vvJevDT3/60wW0yI8aASMwiQj87W9/q770pS9V733ve5M88vnPf766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UprBdrvJRsAIGAEjYASMgBEwAkbACBiBzhGwhatziF2AETACRsAIGAEjYASMgBEwArOKgAWuWe15t9sIGAEjYASMgBEwAkbACBiBzhGwwNU5xC7ACBgBI2AEjIARMAJGwAgYgVlFwALXrPa8220EjIARMAJGwAgYASNgBIxA5whY4OocYhdgBIyAETACRsAIGAEjYASMwKwiYIFrVnve7TYCRsAIGAEjYASMgBEwAkagcwQscHUOsQswAkbACBgBI2AEjIARMAJGYFYRsMA1qz3vdhsBI2AEjIARMAJGwAgYASPQOQIWuDqH2AUYASNgBIyAETACRsAIGAEjMKsIWOCa1Z53u42AETACRsAIGAEjYASMgBHoHAELXJ1D7AKMgBEwAkbACBgBI2AEjIARmFUELHDNas+73UbACBgBI2AEjIARMAJGwAh0joAFrs4hdgFGwAgYASNgBIyAETACRsAIzCoCFrhmtefdbiNgBIyAETACRsAIGAEjYAQ6R8ACV+cQuwAjYASMgBEwAkbACBgBI2AEZhUBC1yz2vMdt/vaa6/tuARnPywC7pNhEXP6aUfghhtuqP76179OezM6rf91111X/fvf/+60jFFmTl1///vfjzJL52UEjIAR6ByBsQpcLHxXXHHFvL8bb7yx84b2K+CPf/xjdeGFF1bHHXdcdfjhh1df/OIXqyuvvLJa7Hr1q/M47j396U+v7n//+1ef/OQnhypu9913rzbccMNqn332Geo5J+4OgWnok1e96lVpvL31rW/tDogpyfnMM89MWDzucY+bkhp3V822WFx66aXV/e53v+phD3tY9f3vf7+7Ck5xzh/+8Ier9ddfv2Kc/f3vf5/4liBAP+pRj6oe+tCHVqeeeurE19cVNAJGYPIRuPrqq5Nc8stf/rLTyi7fae5Z5m984xurj3zkI9nVqvr2t79d3epWt5p3vesLaMpg7t7//vcXi2KxPuqoo6rVV1+9eH/aLyJU/vOf/6xWXXXVaqWVVprXnN/97nfVX/7yl4pFrin94x//qD7/+c+n5CyIb37zm6vllluu6eNO1wEC09Inf/7zn9N4Y8zNOv3tb39LWFxzzTVTAcVvfvOb6vrrr69uc5vbVHe6052GqvOf/vSninbe7GY3q+52t7vNe7YtFv/3f/+X8mI8ff3rX6/uda97zct71i+cccYZCYKr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YO+U9v4QqCQKW+yhIipUaZ/auOrocoyAETACRsAIGAEjYASMQAkBuxSWUPG1iUSA/VxYuXAvJEwywRyIBpkHJ5nIyg+oFEE72BOGD3/8NtKAx3zbCBgBI2AEjIARMAJGYMIRsMA14R3k6hkBI2AEjIARMAJGwAgYASMwvQjYpXB6+841NwJGwAgYASNgBIyAETACRmDCEbDANeEd5OoZASNgBIyAETACRsAIGAEjML0IWOCa3r5zzY2AETACRsAIGAEjYASMgBGYcAQscE14B7l6RsAIGAEjYASMgBEwAkbACEwvAha4prfvXHMjYASMgBEwAkbACBgBI2AEJhwBC1wT3kGunhEwAkbACBgBI2AEjIARMALTi4AFruntO9fcCBgBI2AEjIARMAJGwAgYgQlHwALXhHeQq2cEjIARMAJGwAgYASNgBIzA9CJggWt6+841NwJGwAgYASNgBIyAETACRmDCEbDANeEd5OoZASNgBIyAETACRsAIGAEjML0IWOCa3r5zzY2AETACRsAIGAEjYASMgBGYcAQscE14B7l6RsAIGAEjYASMgBEwAkbACEwvAha4prfvXHMjYASMgBEwAkbACBgBI2AEJhwBC1wT3kGunhEwAkbACBgBI2AEjIARMALTi4AFruntO9fcCBgBI2AEjIARMAJGwAgYgQlHwALXhHeQq2cEjIARMAJGwAgYASNgBIzA9CJggWt6+841NwJGwAgYASNgBIyAETACRmDCEbDANeEd5OoZASNgBIyAETACRsAIGAEjML0IWOCa3r5zzY2AETACRsAIGAEjYASMgBGYcAT+HzFRpSGfUjK0AAAAAElFTkSuQmCC" alt="image.png"></p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Creating-Input-Sequences">Creating Input Sequences<a class="anchor-link" href="#Creating-Input-Sequences">&#182;</a></h2><p>We have two pandas Dataframe objects waiting for us to convert them into suitable objects for the BERT model. We will take advantage of the InputExample function that helps us to create sequences from our dataset. The InputExample function can be called as follows:</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">InputExample</span><span class="p">(</span><span class="n">guid</span><span class="o">=</span><span class="kc">None</span><span class="p">,</span>
             <span class="n">text_a</span> <span class="o">=</span> <span class="s2">&quot;Hello, world&quot;</span><span class="p">,</span>
             <span class="n">text_b</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
             <span class="n">label</span> <span class="o">=</span> <span class="mi">1</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Now-we-will-create-two-main-functions:">Now we will create two main functions:<a class="anchor-link" href="#Now-we-will-create-two-main-functions:">&#182;</a></h2><p>1 — convert_data_to_examples: This will accept our train and test datasets and convert each row into an InputExample object.</p>
<p>2 — convert_examples_to_tf_dataset: This function will tokenize the InputExample objects, then create the required input format with the tokenized objects, finally, create an input dataset that we can feed to the model.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="k">def</span> <span class="nf">convert_data_to_examples</span><span class="p">(</span><span class="n">train</span><span class="p">,</span> <span class="n">test</span><span class="p">,</span> <span class="n">DATA_COLUMN</span><span class="p">,</span> <span class="n">LABEL_COLUMN</span><span class="p">):</span> 
  <span class="n">train_InputExamples</span> <span class="o">=</span> <span class="n">train</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="k">lambda</span> <span class="n">x</span><span class="p">:</span> <span class="n">InputExample</span><span class="p">(</span><span class="n">guid</span><span class="o">=</span><span class="kc">None</span><span class="p">,</span> <span class="c1"># Globally unique ID for bookkeeping, unused in this case</span>
                                                          <span class="n">text_a</span> <span class="o">=</span> <span class="n">x</span><span class="p">[</span><span class="n">DATA_COLUMN</span><span class="p">],</span> 
                                                          <span class="n">text_b</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
                                                          <span class="n">label</span> <span class="o">=</span> <span class="n">x</span><span class="p">[</span><span class="n">LABEL_COLUMN</span><span class="p">]),</span> <span class="n">axis</span> <span class="o">=</span> <span class="mi">1</span><span class="p">)</span>

  <span class="n">validation_InputExamples</span> <span class="o">=</span> <span class="n">test</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="k">lambda</span> <span class="n">x</span><span class="p">:</span> <span class="n">InputExample</span><span class="p">(</span><span class="n">guid</span><span class="o">=</span><span class="kc">None</span><span class="p">,</span> <span class="c1"># Globally unique ID for bookkeeping, unused in this case</span>
                                                          <span class="n">text_a</span> <span class="o">=</span> <span class="n">x</span><span class="p">[</span><span class="n">DATA_COLUMN</span><span class="p">],</span> 
                                                          <span class="n">text_b</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
                                                          <span class="n">label</span> <span class="o">=</span> <span class="n">x</span><span class="p">[</span><span class="n">LABEL_COLUMN</span><span class="p">]),</span> <span class="n">axis</span> <span class="o">=</span> <span class="mi">1</span><span class="p">)</span>
  
  <span class="k">return</span> <span class="n">train_InputExamples</span><span class="p">,</span> <span class="n">validation_InputExamples</span>

  <span class="n">train_InputExamples</span><span class="p">,</span> <span class="n">validation_InputExamples</span> <span class="o">=</span> <span class="n">convert_data_to_examples</span><span class="p">(</span><span class="n">train</span><span class="p">,</span> 
                                                                           <span class="n">test</span><span class="p">,</span> 
                                                                           <span class="s1">&#39;DATA_COLUMN&#39;</span><span class="p">,</span> 
                                                                           <span class="s1">&#39;LABEL_COLUMN&#39;</span><span class="p">)</span>
  
<span class="k">def</span> <span class="nf">convert_examples_to_tf_dataset</span><span class="p">(</span><span class="n">examples</span><span class="p">,</span> <span class="n">tokenizer</span><span class="p">,</span> <span class="n">max_length</span><span class="o">=</span><span class="mi">128</span><span class="p">):</span>
    <span class="n">features</span> <span class="o">=</span> <span class="p">[]</span> <span class="c1"># -&gt; will hold InputFeatures to be converted later</span>

    <span class="k">for</span> <span class="n">e</span> <span class="ow">in</span> <span class="n">examples</span><span class="p">:</span>
        <span class="c1"># Documentation is really strong for this method, so please take a look at it</span>
        <span class="n">input_dict</span> <span class="o">=</span> <span class="n">tokenizer</span><span class="o">.</span><span class="n">encode_plus</span><span class="p">(</span>
            <span class="n">e</span><span class="o">.</span><span class="n">text_a</span><span class="p">,</span>
            <span class="n">add_special_tokens</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span>
            <span class="n">max_length</span><span class="o">=</span><span class="n">max_length</span><span class="p">,</span> <span class="c1"># truncates if len(s) &gt; max_length</span>
            <span class="n">return_token_type_ids</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span>
            <span class="n">return_attention_mask</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span>
            <span class="n">pad_to_max_length</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="c1"># pads to the right by default # CHECK THIS for pad_to_max_length</span>
            <span class="n">truncation</span><span class="o">=</span><span class="kc">True</span>
        <span class="p">)</span>

        <span class="n">input_ids</span><span class="p">,</span> <span class="n">token_type_ids</span><span class="p">,</span> <span class="n">attention_mask</span> <span class="o">=</span> <span class="p">(</span><span class="n">input_dict</span><span class="p">[</span><span class="s2">&quot;input_ids&quot;</span><span class="p">],</span>
            <span class="n">input_dict</span><span class="p">[</span><span class="s2">&quot;token_type_ids&quot;</span><span class="p">],</span> <span class="n">input_dict</span><span class="p">[</span><span class="s1">&#39;attention_mask&#39;</span><span class="p">])</span>

        <span class="n">features</span><span class="o">.</span><span class="n">append</span><span class="p">(</span>
            <span class="n">InputFeatures</span><span class="p">(</span>
                <span class="n">input_ids</span><span class="o">=</span><span class="n">input_ids</span><span class="p">,</span> <span class="n">attention_mask</span><span class="o">=</span><span class="n">attention_mask</span><span class="p">,</span> <span class="n">token_type_ids</span><span class="o">=</span><span class="n">token_type_ids</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="n">e</span><span class="o">.</span><span class="n">label</span>
            <span class="p">)</span>
        <span class="p">)</span>

    <span class="k">def</span> <span class="nf">gen</span><span class="p">():</span>
        <span class="k">for</span> <span class="n">f</span> <span class="ow">in</span> <span class="n">features</span><span class="p">:</span>
            <span class="k">yield</span> <span class="p">(</span>
                <span class="p">{</span>
                    <span class="s2">&quot;input_ids&quot;</span><span class="p">:</span> <span class="n">f</span><span class="o">.</span><span class="n">input_ids</span><span class="p">,</span>
                    <span class="s2">&quot;attention_mask&quot;</span><span class="p">:</span> <span class="n">f</span><span class="o">.</span><span class="n">attention_mask</span><span class="p">,</span>
                    <span class="s2">&quot;token_type_ids&quot;</span><span class="p">:</span> <span class="n">f</span><span class="o">.</span><span class="n">token_type_ids</span><span class="p">,</span>
                <span class="p">},</span>
                <span class="n">f</span><span class="o">.</span><span class="n">label</span><span class="p">,</span>
            <span class="p">)</span>

    <span class="k">return</span> <span class="n">tf</span><span class="o">.</span><span class="n">data</span><span class="o">.</span><span class="n">Dataset</span><span class="o">.</span><span class="n">from_generator</span><span class="p">(</span>
        <span class="n">gen</span><span class="p">,</span>
        <span class="p">({</span><span class="s2">&quot;input_ids&quot;</span><span class="p">:</span> <span class="n">tf</span><span class="o">.</span><span class="n">int32</span><span class="p">,</span> <span class="s2">&quot;attention_mask&quot;</span><span class="p">:</span> <span class="n">tf</span><span class="o">.</span><span class="n">int32</span><span class="p">,</span> <span class="s2">&quot;token_type_ids&quot;</span><span class="p">:</span> <span class="n">tf</span><span class="o">.</span><span class="n">int32</span><span class="p">},</span> <span class="n">tf</span><span class="o">.</span><span class="n">int64</span><span class="p">),</span>
        <span class="p">(</span>
            <span class="p">{</span>
                <span class="s2">&quot;input_ids&quot;</span><span class="p">:</span> <span class="n">tf</span><span class="o">.</span><span class="n">TensorShape</span><span class="p">([</span><span class="kc">None</span><span class="p">]),</span>
                <span class="s2">&quot;attention_mask&quot;</span><span class="p">:</span> <span class="n">tf</span><span class="o">.</span><span class="n">TensorShape</span><span class="p">([</span><span class="kc">None</span><span class="p">]),</span>
                <span class="s2">&quot;token_type_ids&quot;</span><span class="p">:</span> <span class="n">tf</span><span class="o">.</span><span class="n">TensorShape</span><span class="p">([</span><span class="kc">None</span><span class="p">]),</span>
            <span class="p">},</span>
            <span class="n">tf</span><span class="o">.</span><span class="n">TensorShape</span><span class="p">([]),</span>
        <span class="p">),</span>
    <span class="p">)</span>


<span class="n">DATA_COLUMN</span> <span class="o">=</span> <span class="s1">&#39;DATA_COLUMN&#39;</span>
<span class="n">LABEL_COLUMN</span> <span class="o">=</span> <span class="s1">&#39;LABEL_COLUMN&#39;</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="We-can-call-the-functions-we-created-above-with-the-following-lines:">We can call the functions we created above with the following lines:<a class="anchor-link" href="#We-can-call-the-functions-we-created-above-with-the-following-lines:">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[13]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">train_InputExamples</span><span class="p">,</span> <span class="n">validation_InputExamples</span> <span class="o">=</span> <span class="n">convert_data_to_examples</span><span class="p">(</span><span class="n">train</span><span class="p">,</span> <span class="n">test</span><span class="p">,</span> <span class="n">DATA_COLUMN</span><span class="p">,</span> <span class="n">LABEL_COLUMN</span><span class="p">)</span>

<span class="n">train_data</span> <span class="o">=</span> <span class="n">convert_examples_to_tf_dataset</span><span class="p">(</span><span class="nb">list</span><span class="p">(</span><span class="n">train_InputExamples</span><span class="p">),</span> <span class="n">tokenizer</span><span class="p">)</span>
<span class="n">train_data</span> <span class="o">=</span> <span class="n">train_data</span><span class="o">.</span><span class="n">shuffle</span><span class="p">(</span><span class="mi">100</span><span class="p">)</span><span class="o">.</span><span class="n">batch</span><span class="p">(</span><span class="mi">32</span><span class="p">)</span><span class="o">.</span><span class="n">repeat</span><span class="p">(</span><span class="mi">2</span><span class="p">)</span>

<span class="n">validation_data</span> <span class="o">=</span> <span class="n">convert_examples_to_tf_dataset</span><span class="p">(</span><span class="nb">list</span><span class="p">(</span><span class="n">validation_InputExamples</span><span class="p">),</span> <span class="n">tokenizer</span><span class="p">)</span>
<span class="n">validation_data</span> <span class="o">=</span> <span class="n">validation_data</span><span class="o">.</span><span class="n">batch</span><span class="p">(</span><span class="mi">32</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Our dataset containing processed input sequences are ready to be fed to the model.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Configuring-the-BERT-model-and-Fine-tuning">Configuring the BERT model and Fine-tuning<a class="anchor-link" href="#Configuring-the-BERT-model-and-Fine-tuning">&#182;</a></h2><p>We will use Adam as our optimizer, CategoricalCrossentropy as our loss function, and SparseCategoricalAccuracy as our accuracy metric. Fine-tuning the model for 2 epochs will give us around 88% accuracy, which is great.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[14]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">model</span><span class="o">.</span><span class="n">compile</span><span class="p">(</span><span class="n">optimizer</span><span class="o">=</span><span class="n">tf</span><span class="o">.</span><span class="n">keras</span><span class="o">.</span><span class="n">optimizers</span><span class="o">.</span><span class="n">Adam</span><span class="p">(</span><span class="n">learning_rate</span><span class="o">=</span> <span class="mf">0.00003</span><span class="p">,</span> <span class="n">epsilon</span><span class="o">=</span><span class="mf">0.00000001</span><span class="p">,</span> <span class="n">clipnorm</span><span class="o">=</span><span class="mf">1.0</span><span class="p">),</span> 
              <span class="n">loss</span><span class="o">=</span><span class="n">tf</span><span class="o">.</span><span class="n">keras</span><span class="o">.</span><span class="n">losses</span><span class="o">.</span><span class="n">SparseCategoricalCrossentropy</span><span class="p">(</span><span class="n">from_logits</span><span class="o">=</span><span class="kc">True</span><span class="p">),</span> 
              <span class="n">metrics</span><span class="o">=</span><span class="p">[</span><span class="n">tf</span><span class="o">.</span><span class="n">keras</span><span class="o">.</span><span class="n">metrics</span><span class="o">.</span><span class="n">SparseCategoricalAccuracy</span><span class="p">(</span><span class="s1">&#39;accuracy&#39;</span><span class="p">)])</span>

<span class="n">model</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">train_data</span><span class="p">,</span> <span class="n">epochs</span><span class="o">=</span><span class="mi">2</span><span class="p">,</span> <span class="n">validation_data</span><span class="o">=</span><span class="n">validation_data</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>After our training is completed, we can move onto making sentiment predictions.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Making-Predictions">Making Predictions<a class="anchor-link" href="#Making-Predictions">&#182;</a></h2><p>I created a list of two reviews I created. The first one is a positive review, while the second one is clearly negative.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[36]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">pred_sentences</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;This was an awesome movie. I watch it twice my time watching this beautiful movie if I have known it was this good&#39;</span><span class="p">,</span>
                  <span class="s1">&#39;One of the worst movies of all time. I cannot believe I wasted two hours of my life for this movie&#39;</span><span class="p">,</span>
                  <span class="s1">&#39;It is easily one of the most tragic, beautifully written and directed shows of all time and for me at least is at the top of the list of my favourite shows it is tied with Breaking Bad.&#39;</span><span class="p">,</span>
                  <span class="s1">&#39;Too many monsters.&#39;</span><span class="p">,</span>
                  <span class="s1">&#39;Amazing movie! But I will never recommend it to other people&#39;</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>We need to tokenize our reviews with our pre-trained BERT tokenizer. We will then feed these tokenized sequences to our model and run a final softmax layer to get the predictions. We can then use the argmax function to determine whether our sentiment prediction for the review is positive or negative. Finally, we will print out the results with a simple for loop. The following lines do all of these said operations:</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[37]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">tf_batch</span> <span class="o">=</span> <span class="n">tokenizer</span><span class="p">(</span><span class="n">pred_sentences</span><span class="p">,</span> <span class="n">max_length</span><span class="o">=</span><span class="mi">128</span><span class="p">,</span> <span class="n">padding</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">truncation</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">return_tensors</span><span class="o">=</span><span class="s1">&#39;tf&#39;</span><span class="p">)</span>
<span class="n">tf_outputs</span> <span class="o">=</span> <span class="n">model</span><span class="p">(</span><span class="n">tf_batch</span><span class="p">)</span>
<span class="n">tf_predictions</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">nn</span><span class="o">.</span><span class="n">softmax</span><span class="p">(</span><span class="n">tf_outputs</span><span class="p">[</span><span class="mi">0</span><span class="p">],</span> <span class="n">axis</span><span class="o">=-</span><span class="mi">1</span><span class="p">)</span>
<span class="n">labels</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;Negative&#39;</span><span class="p">,</span><span class="s1">&#39;Positive&#39;</span><span class="p">]</span>
<span class="n">label</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">argmax</span><span class="p">(</span><span class="n">tf_predictions</span><span class="p">,</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="n">label</span> <span class="o">=</span> <span class="n">label</span><span class="o">.</span><span class="n">numpy</span><span class="p">()</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="nb">range</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">pred_sentences</span><span class="p">)):</span>
  <span class="nb">print</span><span class="p">(</span><span class="n">pred_sentences</span><span class="p">[</span><span class="n">i</span><span class="p">],</span> <span class="s2">&quot;: </span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">,</span> <span class="n">labels</span><span class="p">[</span><span class="n">label</span><span class="p">[</span><span class="n">i</span><span class="p">]])</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Result">Result<a class="anchor-link" href="#Result">&#182;</a></h2><p>The model achieved ~88% classification accuracy on the validation set with a transformers network with a pre-trained BERT model on the sentiment analysis of the IMDB reviews dataset. The prediction lines with a more obvious positive or negative tone is captured correct and while the model prediction could not catch some ironic sentences using "but".</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Reference:">Reference:<a class="anchor-link" href="#Reference:">&#182;</a></h2><ol>
<li>Canvas: Text Preprocessing and Representation Learning.html</li>
<li><a href="https://towardsdatascience.com/sentiment-analysis-in-10-minutes-with-bert-and-hugging-face-294e8a04b671">https://towardsdatascience.com/sentiment-analysis-in-10-minutes-with-bert-and-hugging-face-294e8a04b671</a> </li>
<li><a href="https://keras.io/getting_started/faq/#how-can-i-save-a-keras-model">https://keras.io/getting_started/faq/#how-can-i-save-a-keras-model</a></li>
<li><a href="https://towardsdatascience.com/mastering-word-embeddings-in-10-minutes-with-tensorflow-41e25da6aa54">https://towardsdatascience.com/mastering-word-embeddings-in-10-minutes-with-tensorflow-41e25da6aa54</a></li>
<li><a href="https://towardsdatascience.com/mastering-word-embeddings-in-10-minutes-with-imdb-reviews-c345f83e054e">https://towardsdatascience.com/mastering-word-embeddings-in-10-minutes-with-imdb-reviews-c345f83e054e</a></li>
</ol>

</div>
</div>
</div>
    </div>
  </div>
</body>

 


</html>