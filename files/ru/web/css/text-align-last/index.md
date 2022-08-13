---
title: text-align-last
slug: Web/CSS/text-align-last
translation_of: Web/CSS/text-align-last
---
<div>{{CSSRef}}</div>

<div>{{SeeCompatTable}}</div>

<h2 id="Кратко">Кратко</h2>

<p><code>text-align-last</code> CSS-свойство описывает как выравнивается последняя строка в блоке или строка, идущая сразу перед принудительным разрывом строки.</p>

<div>{{cssinfo}}</div>

<h2 id="Синтаксис">Синтаксис</h2>

<p><a href="/en-US/docs/CSS/Value_definition_syntax">Formal syntax</a>: {{csssyntax("text-align-last")}}</p>

<pre>text-align-last: auto
text-align-last: start
text-align-last: end
text-align-last: left
text-align-last: right
text-align-last: center
text-align-last: justify

text-align-last: inherit
</pre>

<h3 id="Значения">Значения</h3>

<dl>
 <dt><code>auto</code></dt>
 <dd>Затронутая строка выравнивается в зависимости от значения  {{cssxref("text-align")}}, за исключением {{cssxref("text-align")}} со значением <code>justify</code>, в этом случае эффект такой же как установить <code>text-align-last</code> равным <code>left</code>.</dd>
 <dt><code>start</code></dt>
 <dd>Подобно <code>left</code> если направление слева направо, и <code>right</code> если направление справа налево.</dd>
 <dt><code>end</code></dt>
 <dd>Подобно <code>right</code> если направление слева направо, и <code>left</code> если направление справа налево.</dd>
 <dt><code>left</code></dt>
 <dd>Линейное содержимое выравнивается по левому краю линейного блока.</dd>
 <dt><code>right</code></dt>
 <dd>Линейное содержимое выравнивается по правому краю линейного блока.</dd>
 <dt><code>center</code></dt>
 <dd>Линейное содержимое центрируется внутри линейного блока.</dd>
 <dt><code>justify</code></dt>
 <dd>Текст выравнивается по ширине. Тексту следует выстраивать свои левые и правые границы по левым и правым границам содержимого параграфа.</dd>
</dl>

<h2 id="Примеры">Примеры</h2>

<pre class="brush:css">div {
  text-align: justify;
  -moz-text-align-last: center;
  text-align-last: center;
}
</pre>

<h2 id="Спецификации">Спецификации</h2>

{{Specifications}}

<h2 id="Совместимость_браузера">Совместимость браузера</h2>

<p>{{Compat}}</p>

<h2 id="Смотрите_также">Смотрите также</h2>

<ul>
 <li>{{cssxref("text-align")}}</li>
</ul>