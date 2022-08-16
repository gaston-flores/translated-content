---
title: Animation.effect
slug: Web/API/Animation/effect
---
<p>{{ SeeCompatTable() }} {{ APIRef("Web Animations API") }}</p>

<p>Animation.effect 属性可以获取或设置动画的目标效果。 目标效果可以是{{domxref("KeyframeEffect")}}对象或 null。</p>

<h2 id="语法">语法</h2>

<div class="syntaxbox">
<pre class="brush: js">// Get an Animation object's target effect
var effect = animation.effect;

// Set an Animation's target effect
animation.effect = new KeyframeEffect({ opacity: [ 1, 0 ] }, 300);
</pre>
</div>

<h3 id="值">值</h3>

<p>{{domxref("KeyframeEffect")}} 对象或 null。</p>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器支持">浏览器支持</h2>

{{Compat("api.Animation.effect")}}

<h2 id="相关内容">相关内容</h2>

<ul>
 <li><a href="/en-US/docs/Web/API/KeyframeEffect">KeyframeEffect</a></li>
 <li><a href="/en-US/docs/Web/API/Web_Animations_API">Web Animations API</a></li>
 <li>{{domxref("Animation")}}</li>
</ul>