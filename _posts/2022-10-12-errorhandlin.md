---
keywords: fastai
title: Title
nb_path: _notebooks/2022-10-12-errorhandlin.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-10-12-errorhandlin.ipynb
-->

<div class="container" id="notebook-container">
        
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">menu</span> <span class="o">=</span> <span class="p">{</span>
    <span class="s2">&quot;chicken tikka masala&quot;</span> <span class="p">:</span> <span class="mf">49.99</span><span class="p">,</span>
    <span class="s2">&quot;extra naan&quot;</span> <span class="p">:</span> <span class="mf">19.99</span><span class="p">,</span>
    <span class="s2">&quot;mango lassi&quot;</span> <span class="p">:</span> <span class="mf">69.99</span><span class="p">,</span>
    <span class="s2">&quot;burger&quot;</span> <span class="p">:</span> <span class="mf">1.99</span>
<span class="p">}</span>

<span class="n">total</span> <span class="o">=</span> <span class="mi">0</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Menu&quot;</span><span class="p">)</span>
<span class="k">for</span> <span class="n">k</span><span class="p">,</span><span class="n">v</span> <span class="ow">in</span> <span class="n">menu</span><span class="o">.</span><span class="n">items</span><span class="p">():</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">k</span> <span class="o">+</span> <span class="s2">&quot;  $&quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">v</span><span class="p">))</span>

<span class="n">item</span> <span class="o">=</span> <span class="s2">&quot;&quot;</span>

<span class="n">item</span> <span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;Welcome to the restaurant beta my name is cody smith how can i help you&quot;</span><span class="p">)</span>

<span class="k">if</span> <span class="nb">str</span><span class="p">(</span><span class="n">item</span><span class="p">)</span> <span class="o">==</span> <span class="s2">&quot;chicken tikka masala&quot;</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">item</span><span class="p">)</span> <span class="o">+</span> <span class="s2">&quot; is &quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">menu</span><span class="p">[</span><span class="n">item</span><span class="p">]))</span>
    <span class="n">total</span> <span class="o">+=</span> <span class="nb">str</span><span class="p">(</span><span class="n">menu</span><span class="p">[</span><span class="n">item</span><span class="p">])</span>
<span class="k">elif</span> <span class="nb">str</span><span class="p">(</span><span class="n">item</span><span class="p">)</span> <span class="o">==</span> <span class="s2">&quot;extra naan&quot;</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">item</span><span class="p">)</span> <span class="o">+</span> <span class="s2">&quot; is &quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">menu</span><span class="p">[</span><span class="n">item</span><span class="p">]))</span>
<span class="k">elif</span> <span class="nb">str</span><span class="p">(</span><span class="n">item</span><span class="p">)</span> <span class="o">==</span> <span class="s2">&quot;Done&quot;</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Thank you, your total is &quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">total</span><span class="p">))</span>
<span class="k">else</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Beta please learn to spell you must have A+ in english&quot;</span><span class="p">)</span>
    
    
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Menu
chicken tikka masala  $49.99
extra naan  $19.99
mango lassi  $69.99
burger  $1.99
chicken tikka masala is 49.99
</pre>
</div>
</div>

<div class="output_area">

<div class="output_subarea output_text output_error">
<pre>
<span class="ansi-red-fg">---------------------------------------------------------------------------</span>
<span class="ansi-red-fg">TypeError</span>                                 Traceback (most recent call last)
<span class="ansi-green-intense-fg ansi-bold">/home/paaraspurohit/vscode/apcompsciportfolio/_notebooks/2022-10-12-errorhandlin.ipynb Cell 1</span> in <span class="ansi-cyan-fg">&lt;cell line: 18&gt;</span><span class="ansi-blue-fg">()</span>
<span class="ansi-green-intense-fg ansi-bold">     &lt;a href=&#39;vscode-notebook-cell://wsl%2Bubuntu/home/paaraspurohit/vscode/apcompsciportfolio/_notebooks/2022-10-12-errorhandlin.ipynb#W0sdnNjb2RlLXJlbW90ZQ%3D%3D?line=17&#39;&gt;18&lt;/a&gt;</span> if str(item) == &#34;chicken tikka masala&#34;:
<span class="ansi-green-intense-fg ansi-bold">     &lt;a href=&#39;vscode-notebook-cell://wsl%2Bubuntu/home/paaraspurohit/vscode/apcompsciportfolio/_notebooks/2022-10-12-errorhandlin.ipynb#W0sdnNjb2RlLXJlbW90ZQ%3D%3D?line=18&#39;&gt;19&lt;/a&gt;</span>     print(str(item) + &#34; is &#34; + str(menu[item]))
<span class="ansi-green-fg">---&gt; &lt;a href=&#39;vscode-notebook-cell://wsl%2Bubuntu/home/paaraspurohit/vscode/apcompsciportfolio/_notebooks/2022-10-12-errorhandlin.ipynb#W0sdnNjb2RlLXJlbW90ZQ%3D%3D?line=19&#39;&gt;20&lt;/a&gt;</span>     total += str(menu[item])
<span class="ansi-green-intense-fg ansi-bold">     &lt;a href=&#39;vscode-notebook-cell://wsl%2Bubuntu/home/paaraspurohit/vscode/apcompsciportfolio/_notebooks/2022-10-12-errorhandlin.ipynb#W0sdnNjb2RlLXJlbW90ZQ%3D%3D?line=20&#39;&gt;21&lt;/a&gt;</span> elif str(item) == &#34;extra naan&#34;:
<span class="ansi-green-intense-fg ansi-bold">     &lt;a href=&#39;vscode-notebook-cell://wsl%2Bubuntu/home/paaraspurohit/vscode/apcompsciportfolio/_notebooks/2022-10-12-errorhandlin.ipynb#W0sdnNjb2RlLXJlbW90ZQ%3D%3D?line=21&#39;&gt;22&lt;/a&gt;</span>     print(str(item) + &#34; is &#34; + str(menu[item]))

<span class="ansi-red-fg">TypeError</span>: unsupported operand type(s) for +=: &#39;int&#39; and &#39;str&#39;</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

</div>
 
