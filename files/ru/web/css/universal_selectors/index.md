---
title: Универсальные селекторы
slug: Web/CSS/Universal_selectors
translation_of: Web/CSS/Universal_selectors
---
<p>{{CSSRef("Selectors")}}</p>

<h2 id="Краткое_описание">Краткое описание</h2>

<p>Звёздочка (*) - универсальный селектор для CSS. Соответствует любому тегу. Убирая звёздочки с простых селекторов имеет тот же эффект. Например, <em>* .warning</em> и <em>.warning</em> считаются равными.</p>

<p>В CSS 3, звёздочка (<code>*</code>) может использоваться в комбинации с пространством имён</p>

<ul>
 <li><code>ns|*</code> - вхождения всех элементов в пространстве имён ns</li>
 <li><code>*|*</code> - находит все элементы</li>
 <li><code>|*</code> - ищет все элементы без объявленного пространства имён</li>
</ul>

<h2 id="Example">Пример</h2>

<pre class="brush: css">*[lang^=en]{color:green;}
*.warning {color:red;}
*#maincontent {border: 1px solid blue;}
</pre>

<pre class="brush: html">&lt;p class="warning"&gt;
  &lt;span lang="en-us"&gt;Зелёный span&lt;/span&gt; в красном параграфе.
&lt;/p&gt;
&lt;p id="maincontent" lang="en-gb"&gt;
  &lt;span class="warning"&gt;Красный span&lt;/span&gt; в зелёном параграфе.
&lt;/p&gt;</pre>

<p>{{ EmbedLiveSample('Example', 250, 100) }}</p>

<h2 id="Спецификации">Спецификации</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Поддержка браузерами</h2>

<p>{{Compat}}</p>