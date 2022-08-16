---
title: GlobalEventHandlers.onpointerout
slug: Web/API/Element/pointerout_event
---
<div>{{ApiRef("HTML DOM")}}</div>

<p>一个{{domxref("GlobalEventHandlers","global event handler")}} 用于处理 {{event("pointerout")}} 事件。</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">var <var>outHandler</var> = <var>targetElement</var>.onpointerout;
</pre>

<h3 id="返回值">返回值</h3>

<dl>
 <dt><code>outHandler</code></dt>
 <dd>元素<code>targetElement</code>的指针输出事件处理程序。</dd>
</dl>

<h2 id="例子">例子</h2>

<p>这个例子展示了两种方式来使用 onpointerout 设置元素的 pointerout 事件处理程序。</p>

<pre class="brush: js">&lt;html&gt;
&lt;script&gt;
function outHandler(ev) {
 // Process the pointerout event
}
function init() {
 var el=document.getElementById("target1");
 el.onpointerout = outHandler;
}
&lt;/script&gt;
&lt;body onload="init();"&gt;
&lt;div id="target1"&gt; Touch me ... &lt;/div&gt;
&lt;div id="target2" onpointerout="outHandler(event)"&gt; Touch me ... &lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>



<p>{{Compat("api.GlobalEventHandlers.onpointerout")}}</p>

<h2 id="相关链接">相关链接</h2>

<ul>
 <li>{{event("pointerout")}}</li>
</ul>