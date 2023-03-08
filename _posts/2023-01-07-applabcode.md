---
keywords: fastai
title: Coding with AppLab
toc: true
categories: [reflections]
permalink: /coding-with-applab
tags: [reflections]
nb_path: _notebooks/2022-9-7-applabcode.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-9-7-applabcode.ipynb
-->

<div class="container" id="notebook-container">
        
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<!--
![applab](https://studio.code.org/projects/applab/-wS4YvDlyFkUal5cBF6qgYpt_3DpgaagloLN9MA1FQ0)

<iframe width="392" height="620" style="border: 0px;" src="https://studio.code.org/projects/applab/-wS4YvDlyFkUal5cBF6qgYpt_3DpgaagloLN9MA1FQ0/embed"></iframe>
-->

<p><a href= "https://studio.code.org/projects/applab/-wS4YvDlyFkUal5cBF6qgYpt_3DpgaagloLN9MA1FQ0" target="_blank" >This</a> is a project done by Paaras Purohit (me) and AJ Ruiz. This is our first app coded with AppLab, and we created a very simple quiz. The language used was JavaScript, a language mainly used for programming HTML behavior. It is famous for having a large amount of libraries, as well.</p>
<h1 id="APCSP-Create-Performance-Task-Requirements-Met:">APCSP Create Performance Task Requirements Met:<a class="anchor-link" href="#APCSP-Create-Performance-Task-Requirements-Met:"> </a></h1><ul>
<li><p>Program Purpose and Function - The purpose was to create a simple quiz that implemented the CPT Requirements</p>
</li>
<li><p>Data Abstraction - I used different screens that looked at stored values of "right" or "wrong," and output the correct message for the user's answer, whether it was wrong or right.</p>
</li>
<li><p>Managing Complexity - Since this was a quiz, complexity was not always needed, but the code is efficient and does not take too long to run, despite its length.</p>
</li>
<li><p>Procedural Abstraction - The code written for the quiz, I believe, can defintely be applied to other relevant situations.</p>
</li>
<li><p>Algorithm Implementation - Using if-else statements and checking what is being inputted when, I was able to create simple algorithms that completed the task.</p>
</li>
<li><p>Testing - There was some syntax error here and there, but no major errors to report.</p>
</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Hack-II---Creating-a-New-App">Hack II - Creating a New App<a class="anchor-link" href="#Hack-II---Creating-a-New-App"> </a></h3><p>Below is a financing app, which lets you sign in and deposit/withdraw money.</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">account</span> <span class="o">=</span> <span class="p">{</span>
    <span class="s2">&quot;Username&quot;</span><span class="p">:[],</span>
    <span class="s2">&quot;Password&quot;</span><span class="p">:[],</span>
    <span class="s2">&quot;Amount&quot;</span><span class="p">:</span><span class="mi">0</span><span class="p">,</span>
<span class="p">}</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Hello, please create an account &gt;&gt;&quot;</span><span class="p">)</span>
<span class="n">account</span><span class="p">[</span><span class="s2">&quot;Username&quot;</span><span class="p">]</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="nb">input</span><span class="p">(</span><span class="s2">&quot;Enter Username &gt;&gt;&quot;</span><span class="p">))</span>
<span class="n">account</span><span class="p">[</span><span class="s2">&quot;Password&quot;</span><span class="p">]</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="nb">input</span><span class="p">(</span><span class="s2">&quot;Enter Password &gt;&gt;&quot;</span><span class="p">))</span>

<span class="k">def</span> <span class="nf">deposit_or_withdraw</span><span class="p">():</span>
    <span class="n">action</span> <span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;Hello, &quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">account</span><span class="p">[</span><span class="s2">&quot;Username&quot;</span><span class="p">])</span> <span class="o">+</span> <span class="s2">&quot;, would you like to deposit or withdraw today?&quot;</span><span class="p">)</span>
    <span class="k">if</span> <span class="n">action</span> <span class="o">==</span> <span class="s2">&quot;deposit&quot;</span><span class="p">:</span>
        <span class="n">deposit</span><span class="p">()</span>
    <span class="k">elif</span> <span class="n">action</span> <span class="o">==</span> <span class="s2">&quot;withdraw&quot;</span><span class="p">:</span>
        <span class="n">withdraw</span><span class="p">()</span>
    <span class="k">elif</span> <span class="n">action</span> <span class="o">==</span> <span class="s2">&quot;exit&quot;</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">()</span>
    <span class="k">else</span><span class="p">:</span>
        <span class="n">deposit_or_withdraw</span><span class="p">()</span>
        
<span class="k">def</span> <span class="nf">deposit</span><span class="p">():</span>
    <span class="n">amount</span> <span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;Amount you would like to deposit?&quot;</span><span class="p">)</span>
    <span class="n">account</span><span class="p">[</span><span class="s2">&quot;Amount&quot;</span><span class="p">]</span> <span class="o">+=</span> <span class="nb">int</span><span class="p">(</span><span class="n">amount</span><span class="p">)</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Successfully deposited. Your balance is now &quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">account</span><span class="p">[</span><span class="s2">&quot;Amount&quot;</span><span class="p">]))</span>
    <span class="n">deposit_or_withdraw</span><span class="p">()</span>

<span class="k">def</span> <span class="nf">withdraw</span><span class="p">():</span>
    <span class="n">amount</span> <span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;Amount you would like to withdraw?&quot;</span><span class="p">)</span>
    <span class="k">if</span> <span class="nb">int</span><span class="p">(</span><span class="n">amount</span><span class="p">)</span> <span class="o">&gt;</span> <span class="n">account</span><span class="p">[</span><span class="s2">&quot;Amount&quot;</span><span class="p">]:</span>
        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;You do not have enough money.&quot;</span><span class="p">)</span>
        <span class="n">deposit_or_withdraw</span><span class="p">()</span>
    <span class="k">else</span><span class="p">:</span>
        <span class="n">account</span><span class="p">[</span><span class="s2">&quot;Amount&quot;</span><span class="p">]</span> <span class="o">-=</span> <span class="nb">int</span><span class="p">(</span><span class="n">amount</span><span class="p">)</span>
        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Successfully withdrawn. Your balance is now &quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">account</span><span class="p">[</span><span class="s2">&quot;Amount&quot;</span><span class="p">]))</span>
        <span class="n">deposit_or_withdraw</span><span class="p">()</span>
        
<span class="n">deposit_or_withdraw</span><span class="p">()</span>
    
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Hello, please create an account &gt;&gt;
Successfully deposited. Your balance is now 69
You do not have enough money.
Successfully deposited. Your balance is now 69
Successfully withdrawn. Your balance is now 9

</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

</div>
 
