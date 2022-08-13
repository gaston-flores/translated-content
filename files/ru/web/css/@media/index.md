---
title: '@media'
slug: Web/CSS/@media
translation_of: Web/CSS/@media
---
<p>{{CSSRef}}</p>

<h2 id="Описание">Описание</h2>

<p>At-правило <code>@media</code> в <a href="/ru/docs/Web/CSS">CSS</a> связывает набор операторов, ограниченных фигурными скобками, в CSS блок, применяется при соблюдении условия одного или нескольких <a href="/ru/docs/Web/CSS/Media_Queries/Using_media_queries">медиавыражений</a>.</p>

<div class="blockIndicator note">
<p>В JavaScript, at-правило <code>@media</code> может быть получено с помощью {{domxref("CSSMediaRule")}}, интерфейса объектной модели CSS.</p>
</div>

<h2 id="Syntax">Синтаксис</h2>

<p>At-правило <code>@media</code> можно разместить не только на верхнем уровне CSS, но и внутри любого фрагмента <a href="/ru/docs/Web/CSS/At-rule#Conditional_group_rules">условной группы-правил</a>.</p>

<pre class="brush: css"><code>/* На верхнем уровне кода */
@media screen and (min-width: 900px) {
  article {
    padding: 1rem 3rem;
  }
}

/* Вложено в другое условное at-правило */
@supports (display: flex) {
  @media screen and (min-width: 900px) {
    article {
      display: flex;
    }
  }
}</code></pre>

<p>Для рассмотрения синтаксиса медиавыражений, см. <a href="/ru/docs/Web/CSS/Media_Queries/Using_media_queries#Syntax">Использование медиавыражений</a>.</p>

<h3 id="Формальный_синтаксис">Формальный синтаксис</h3>

{{csssyntax}}

<p>A <code>&lt;media-query&gt;</code> is composed of a optional media type and/or a number of media features.</p>

<h2 id="Media_types">Типы</h2>

<dl>
 <dt>all</dt>
 <dd>Подходит для всех устройств.</dd>
 <dt>print</dt>
 <dd>Intended for paged material and for documents viewed on screen in print preview mode. Please consult the section on <a href="/en/CSS/Paged_Media" title="https://developer.mozilla.org/en/CSS/Paged_Media">paged media</a>, and the <a href="/en/CSS/Getting_Started/Media" title="https://developer.mozilla.org/en/CSS/Getting_Started/Media">media section of the Getting Started tutorial</a> for information about formatting issues that are specific to paged media.</dd>
 <dt>screen</dt>
 <dd>Предназначен в первую очередь для цветных компьютерных экранов.</dd>
 <dt>speech</dt>
 <dd>Предназначен для синтезаторов речи.</dd>
</dl>

<div class="note"><strong>Примечание:</strong> CSS2.1 и Media Queries 3 определили несколько дополнительных значений (<code>tty</code>, <code>tv</code>, <code>projection</code>, <code>handheld</code>, <code>braille</code>, <code>embossed</code>, <code>aural</code>), но они устарели в <a href="http://dev.w3.org/csswg/mediaqueries/#media-types">Media Queries 4</a> и не рекомендуется к использованию.</div>

<h2 id="Media_features">Media Features</h2>

<p>Each <em>media feature</em> tests for one specific feature of the browser or device.</p>

<table>
 <thead>
  <tr>
   <th>Имя</th>
   <th>Summary</th>
   <th>Notes</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/width"><code>width</code></a></td>
   <td>Viewport width</td>
   <td></td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/height"><code>height</code></a></td>
   <td>Viewport height</td>
   <td></td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/aspect-ratio"><code>aspect-ratio</code></a></td>
   <td>Width-to-height aspect ratio of the viewport</td>
   <td></td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/orientation"><code>orientation</code></a></td>
   <td>Orientation of the viewport</td>
   <td></td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/resolution"><code>resolution</code></a></td>
   <td>Pixel density of the output device</td>
   <td></td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/scan"><code>scan</code></a></td>
   <td>Scanning process of the output device</td>
   <td></td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/grid"><code>grid</code></a></td>
   <td>Is the device a grid or bitmap?</td>
   <td></td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/update-frequency"><code>update-frequency</code></a></td>
   <td>How quickly (if at all) can the output device modify the appearance of the content</td>
   <td>Added in Media Queries Level 4</td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/overflow-block"><code>overflow-block</code></a></td>
   <td>How does the output device handle content that overflows the viewport along the block axis?</td>
   <td>Added in Media Queries Level 4</td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/overflow-inline"><code>overflow-inline</code></a></td>
   <td>Can content that overflows the viewport along the inline axis be scrolled?</td>
   <td>Added in Media Queries Level 4</td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/color"><code>color</code></a></td>
   <td>Number of bits per color component of the output device, or zero if the device isn't color.</td>
   <td></td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/color-index"><code>color-index</code></a></td>
   <td>Number of entries in the output device's color lookup table, or zero if the device does not use such a table.</td>
   <td></td>
  </tr>
  <tr>
   <td><code><a href="/en-US/docs/Web/CSS/@media/display-mode">display-mode</a></code></td>
   <td>The display mode of the application, as specified in the web app manifest's <a href="/en-US/docs/Web/Manifest#display">display member</a>.</td>
   <td>Defined in the <a href="http://w3c.github.io/manifest/#the-display-mode-media-feature">Web App Manifest spec</a>.</td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/monochrome"><code>monochrome</code></a></td>
   <td>Bits per pixel in the output device's monochrome frame buffer, or 0 if the device is not monochrome.</td>
   <td></td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/inverted-colors"><code>inverted-colors</code></a></td>
   <td>Is the user agent or underlying OS inverting colors?</td>
   <td>Added in Media Queries Level 4</td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/pointer"><code>pointer</code></a></td>
   <td>Is the primary input mechanism a pointing device, and if so, how accurate is it?</td>
   <td>Added in Media Queries Level 4</td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/hover"><code>hover</code></a></td>
   <td>Does the primary input mechanism allow the user to hover over elements?</td>
   <td>Added in Media Queries Level 4</td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/any-pointer"><code>any-pointer</code></a></td>
   <td>Is any available input mechanism a pointing device, and if so, how accurate is it?</td>
   <td>Added in Media Queries Level 4</td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/any-hover"><code>any-hover</code></a></td>
   <td>Does any available input mechanism allow the user to hover over elements?</td>
   <td>Added in Media Queries Level 4</td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/light-level"><code>light-level</code></a></td>
   <td>Current ambient light level</td>
   <td>Added in Media Queries Level 4</td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/scripting"><code>scripting</code></a></td>
   <td>Is scripting (e.g. JavaScript) available?</td>
   <td>Added in Media Queries Level 4</td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/device-width"><code>device-width</code></a> {{obsolete_inline}}</td>
   <td>Width of the rendering surface of the output device</td>
   <td>Deprecated in Media Queries Level 4</td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/device-height"><code>device-height</code></a> {{obsolete_inline}}</td>
   <td>Height of the rendering surface of the output device</td>
   <td>Deprecated in Media Queries Level 4</td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/device-aspect-ratio"><code>device-aspect-ratio</code></a> {{obsolete_inline}}</td>
   <td>Width-to-height aspect ratio of the output device</td>
   <td>Deprecated in Media Queries Level 4</td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/-webkit-device-pixel-ratio"><code>-webkit-device-pixel-ratio</code></a> {{non-standard_inline}}</td>
   <td>Number of physical device pixels per CSS pixel</td>
   <td>Nonstandard; WebKit/Blink-specific. If possible, use the <a href="/en-US/docs/Web/CSS/@media/resolution"><code>resolution</code></a> media feature instead.</td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/-webkit-transform-3d"><code>-webkit-transform-3d</code></a> {{non-standard_inline}}</td>
   <td>Are CSS 3D {{cssxref("transform")}}s supported?</td>
   <td>Nonstandard; WebKit/Blink-specific</td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/-webkit-transform-2d"><code>-webkit-transform-2d</code></a> {{non-standard_inline}}</td>
   <td>Are CSS 2D {{cssxref("transform")}}s supported?</td>
   <td>Nonstandard; WebKit-specific</td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/-webkit-transition"><code>-webkit-transition</code></a> {{non-standard_inline}}</td>
   <td>Are CSS {{cssxref("transition")}}s supported?</td>
   <td>Nonstandard; WebKit-specific</td>
  </tr>
  <tr>
   <td><a href="/en-US/docs/Web/CSS/@media/-webkit-animation"><code>-webkit-animation</code></a> {{non-standard_inline}}</td>
   <td>Are CSS {{cssxref("animation")}}s supported?</td>
   <td>Nonstandard; WebKit-specific</td>
  </tr>
 </tbody>
</table>

<h2 id="Examples">Примеры</h2>

<pre class="brush: css">@media print {
  body { font-size: 10pt }
}
@media screen {
  body { font-size: 13px }
}
@media screen, print {
  body { line-height: 1.2 }
}
@media only screen
  and (min-device-width: 320px)
  and (max-device-width: 480px)
  and (-webkit-min-device-pixel-ratio: 2) {
    body { line-height: 1.4 }
}
</pre>

<h2 id="Спецификации">Спецификации</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Совместимость с браузерами</h2>

<p>{{Compat}}</p>

<h2 id="Смотрите_также">Смотрите также</h2>

<ul>
 <li><a class="internal" href="/en/CSS/Media_queries" title="En/CSS/Media queries">Media queries</a></li>
 <li>The CSSOM {{ domxref("CSSMediaRule") }} associated with this at-rule.</li>
</ul>