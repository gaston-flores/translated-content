---
title: URLSearchParams.sort()
slug: Web/API/URLSearchParams/sort
---
<p>{{APIRef("URL API")}}{{SeeCompatTable}}</p>

<p><code><strong>URLSearchParams.sort()</strong></code> 方法对包含在此对象中的所有键/值对进行排序，并返回 undefined。排序顺序是根据键的 Unicode 代码点。该方法使用稳定的排序算法 (即，将保留具有相等键的键/值对之间的相对顺序)。</p>

<h2 id="Syntax">Syntax</h2>

<pre class="syntaxbox">searchParams.sort();</pre>

<h3 id="Return_value">Return value</h3>

<p>Returns <code>undefined</code>.</p>

<h2 id="Example">Example</h2>

<pre class="brush: js; highlight:[5]">// Create a test URLSearchParams object
var searchParams = new URLSearchParams("c=4&amp;a=2&amp;b=3&amp;a=1");

// Sort the key/value pairs
searchParams.sort();

// Display the sorted query string
console.log(searchParams.toString());
</pre>

<p>The result is:</p>

<pre>a=2&amp;a=1&amp;b=3&amp;c=4</pre>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

{{Compat("api.URLSearchParams.sort")}}