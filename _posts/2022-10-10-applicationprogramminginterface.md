---
keywords: fastai
title: API's
toc: true
categories: [api]
permalink: /apis
tags: [api]
nb_path: _notebooks/2022-10-10-applicationprogramminginterface.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-10-10-applicationprogramminginterface.ipynb
-->

<div class="container" id="notebook-container">
        
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Our-Use-of-API's">Our Use of API's<a class="anchor-link" href="#Our-Use-of-API's"> </a></h3><p>Right now, our purpose is promoting KFC. We found this API that lists each KFC location in the United States of America. This can be used for advertising KFC on a geographical mindset.</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">requests</span>

<span class="n">url</span> <span class="o">=</span> <span class="s2">&quot;https://kfc-locations.p.rapidapi.com/kfc/location/0&quot;</span>

<span class="n">headers</span> <span class="o">=</span> <span class="p">{</span>
	<span class="s2">&quot;X-RapidAPI-Key&quot;</span><span class="p">:</span> <span class="s2">&quot;f9e05fed4fmshda97f8933d9e076p192198jsn5018f8cb51c3&quot;</span><span class="p">,</span>
	<span class="s2">&quot;X-RapidAPI-Host&quot;</span><span class="p">:</span> <span class="s2">&quot;kfc-locations.p.rapidapi.com&quot;</span>
<span class="p">}</span>

<span class="n">response</span> <span class="o">=</span> <span class="n">requests</span><span class="o">.</span><span class="n">request</span><span class="p">(</span><span class="s2">&quot;GET&quot;</span><span class="p">,</span> <span class="n">url</span><span class="p">,</span> <span class="n">headers</span><span class="o">=</span><span class="n">headers</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="n">response</span><span class="o">.</span><span class="n">json</span><span class="p">())</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[{&#39;id&#39;: 1, &#39;storeName&#39;: &#39;Kentucky Fried Chicken&#39;, &#39;address&#39;: &#39;2350 Miracle Mile&#39;, &#39;zipCode&#39;: &#39;86442&#39;, &#39;phone&#39;: &#39;(928) 763-2111&#39;, &#39;stateName&#39;: &#39;AZ&#39;, &#39;cityName&#39;: &#39;Bullhead City&#39;, &#39;latitude&#39;: &#39;35.099735982044&#39;, &#39;longitude&#39;: &#39;-114.59584849976&#39;, &#39;monday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;tuesday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;wednesday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;thursday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;friday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;saturday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;sunday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}}, {&#39;id&#39;: 2, &#39;storeName&#39;: &#39;Kentucky Fried Chicken&#39;, &#39;address&#39;: &#39;14200 Ramona Blvd&#39;, &#39;zipCode&#39;: &#39;91706&#39;, &#39;phone&#39;: &#39;(626) 412-0246&#39;, &#39;stateName&#39;: &#39;CA&#39;, &#39;cityName&#39;: &#39;Baldwin Park&#39;, &#39;latitude&#39;: &#39;34.085007092947&#39;, &#39;longitude&#39;: &#39;-117.96434596872&#39;, &#39;monday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;tuesday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;wednesday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;thursday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;friday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;saturday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;sunday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}}, {&#39;id&#39;: 3, &#39;storeName&#39;: &#39;Kentucky Fried Chicken&#39;, &#39;address&#39;: &#39;126 Vermont Avenue&#39;, &#39;zipCode&#39;: &#39;90004&#39;, &#39;phone&#39;: &#39;(213) 487-4503&#39;, &#39;stateName&#39;: &#39;CA&#39;, &#39;cityName&#39;: &#39;Los Angeles&#39;, &#39;latitude&#39;: &#39;34.072344596213&#39;, &#39;longitude&#39;: &#39;-118.29140177489&#39;, &#39;monday&#39;: {&#39;openTime&#39;: &#39;09:09 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;tuesday&#39;: {&#39;openTime&#39;: &#39;09:09 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;wednesday&#39;: {&#39;openTime&#39;: &#39;09:09 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;thursday&#39;: {&#39;openTime&#39;: &#39;09:09 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;friday&#39;: {&#39;openTime&#39;: &#39;09:09 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;saturday&#39;: {&#39;openTime&#39;: &#39;09:09 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;sunday&#39;: {&#39;openTime&#39;: &#39;09:09 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}}, {&#39;id&#39;: 4, &#39;storeName&#39;: &#39;Kentucky Fried Chicken&#39;, &#39;address&#39;: &#39;3250 Dale Road&#39;, &#39;zipCode&#39;: &#39;95356&#39;, &#39;phone&#39;: &#39;(209) 523-3868&#39;, &#39;stateName&#39;: &#39;CA&#39;, &#39;cityName&#39;: &#39;Modesto&#39;, &#39;latitude&#39;: &#39;37.686596884382&#39;, &#39;longitude&#39;: &#39;-121.04934331039&#39;, &#39;monday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;tuesday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;wednesday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;thursday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;friday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;saturday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;sunday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}}, {&#39;id&#39;: 5, &#39;storeName&#39;: &#39;Kentucky Fried Chicken&#39;, &#39;address&#39;: &#39;12319 San Pablo Avenue&#39;, &#39;zipCode&#39;: &#39;94805&#39;, &#39;phone&#39;: &#39;(510) 232-1527&#39;, &#39;stateName&#39;: &#39;CA&#39;, &#39;cityName&#39;: &#39;Richmond&#39;, &#39;latitude&#39;: &#39;37.935616540158&#39;, &#39;longitude&#39;: &#39;-122.32562680736&#39;, &#39;monday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;tuesday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;wednesday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;thursday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;friday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;saturday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;sunday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}}, {&#39;id&#39;: 6, &#39;storeName&#39;: &#39;Kentucky Fried Chicken&#39;, &#39;address&#39;: &#39;5225 Canyon Crest Dr&#39;, &#39;zipCode&#39;: &#39;92507&#39;, &#39;phone&#39;: &#39;(951) 787-0761&#39;, &#39;stateName&#39;: &#39;CA&#39;, &#39;cityName&#39;: &#39;Riverside&#39;, &#39;latitude&#39;: &#39;33.955670429343&#39;, &#39;longitude&#39;: &#39;-117.32950953312&#39;, &#39;monday&#39;: {&#39;openTime&#39;: &#39;09:09 AM&#39;, &#39;closeTime&#39;: &#39;23:11 PM&#39;}, &#39;tuesday&#39;: {&#39;openTime&#39;: &#39;09:09 AM&#39;, &#39;closeTime&#39;: &#39;23:11 PM&#39;}, &#39;wednesday&#39;: {&#39;openTime&#39;: &#39;09:09 AM&#39;, &#39;closeTime&#39;: &#39;23:11 PM&#39;}, &#39;thursday&#39;: {&#39;openTime&#39;: &#39;09:09 AM&#39;, &#39;closeTime&#39;: &#39;23:11 PM&#39;}, &#39;friday&#39;: {&#39;openTime&#39;: &#39;09:09 AM&#39;, &#39;closeTime&#39;: &#39;23:11 PM&#39;}, &#39;saturday&#39;: {&#39;openTime&#39;: &#39;09:09 AM&#39;, &#39;closeTime&#39;: &#39;23:11 PM&#39;}, &#39;sunday&#39;: {&#39;openTime&#39;: &#39;09:09 AM&#39;, &#39;closeTime&#39;: &#39;23:11 PM&#39;}}, {&#39;id&#39;: 7, &#39;storeName&#39;: &#39;Kentucky Fried Chicken&#39;, &#39;address&#39;: &#39;2260 Callagan Hwy&#39;, &#39;zipCode&#39;: &#39;92136&#39;, &#39;phone&#39;: &#39;(760) 580-7977&#39;, &#39;stateName&#39;: &#39;CA&#39;, &#39;cityName&#39;: &#39;San Diego&#39;, &#39;latitude&#39;: &#39;32.68984&#39;, &#39;longitude&#39;: &#39;-117.128494&#39;, &#39;monday&#39;: {&#39;openTime&#39;: None, &#39;closeTime&#39;: None}, &#39;tuesday&#39;: {&#39;openTime&#39;: None, &#39;closeTime&#39;: None}, &#39;wednesday&#39;: {&#39;openTime&#39;: None, &#39;closeTime&#39;: None}, &#39;thursday&#39;: {&#39;openTime&#39;: None, &#39;closeTime&#39;: None}, &#39;friday&#39;: {&#39;openTime&#39;: None, &#39;closeTime&#39;: None}, &#39;saturday&#39;: {&#39;openTime&#39;: None, &#39;closeTime&#39;: None}, &#39;sunday&#39;: {&#39;openTime&#39;: None, &#39;closeTime&#39;: None}}, {&#39;id&#39;: 8, &#39;storeName&#39;: &#39;Kentucky Fried Chicken&#39;, &#39;address&#39;: &#39;1065 East El Camino Real&#39;, &#39;zipCode&#39;: &#39;94087&#39;, &#39;phone&#39;: &#39;(408) 246-8924&#39;, &#39;stateName&#39;: &#39;CA&#39;, &#39;cityName&#39;: &#39;Sunnyvale&#39;, &#39;latitude&#39;: &#39;37.352596825301&#39;, &#39;longitude&#39;: &#39;-122.0037313434&#39;, &#39;monday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;tuesday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;wednesday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;thursday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;friday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;saturday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;sunday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}}, {&#39;id&#39;: 9, &#39;storeName&#39;: &#39;Kentucky Fried Chicken&#39;, &#39;address&#39;: &#39;230 Route&#39;, &#39;zipCode&#39;: &#39;06340&#39;, &#39;phone&#39;: &#39;(860) 449-1888&#39;, &#39;stateName&#39;: &#39;CT&#39;, &#39;cityName&#39;: &#39;Groton&#39;, &#39;latitude&#39;: &#39;41.368902247397&#39;, &#39;longitude&#39;: &#39;-72.069774193484&#39;, &#39;monday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;tuesday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;wednesday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}, &#39;thursday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;23:11 PM&#39;}, &#39;friday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;23:11 PM&#39;}, &#39;saturday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;23:11 PM&#39;}, &#39;sunday&#39;: {&#39;openTime&#39;: &#39;10:10 AM&#39;, &#39;closeTime&#39;: &#39;22:10 PM&#39;}}, {&#39;id&#39;: 10, &#39;storeName&#39;: &#39;Kentucky Fried Chicken&#39;, &#39;address&#39;: &#39;8363 W Flagler Street&#39;, &#39;zipCode&#39;: &#39;33144&#39;, &#39;phone&#39;: &#39;(305) 267-1356&#39;, &#39;stateName&#39;: &#39;FL&#39;, &#39;cityName&#39;: &#39;Miami&#39;, &#39;latitude&#39;: &#39;25.770171050322&#39;, &#39;longitude&#39;: &#39;-80.331015579154&#39;, &#39;monday&#39;: {&#39;openTime&#39;: &#39;05:05 AM&#39;, &#39;closeTime&#39;: &#39;04:04 AM&#39;}, &#39;tuesday&#39;: {&#39;openTime&#39;: &#39;05:05 AM&#39;, &#39;closeTime&#39;: &#39;04:04 AM&#39;}, &#39;wednesday&#39;: {&#39;openTime&#39;: &#39;05:05 AM&#39;, &#39;closeTime&#39;: &#39;04:04 AM&#39;}, &#39;thursday&#39;: {&#39;openTime&#39;: &#39;05:05 AM&#39;, &#39;closeTime&#39;: &#39;04:04 AM&#39;}, &#39;friday&#39;: {&#39;openTime&#39;: &#39;06:06 AM&#39;, &#39;closeTime&#39;: &#39;05:05 AM&#39;}, &#39;saturday&#39;: {&#39;openTime&#39;: &#39;06:06 AM&#39;, &#39;closeTime&#39;: &#39;05:05 AM&#39;}, &#39;sunday&#39;: {&#39;openTime&#39;: &#39;05:05 AM&#39;, &#39;closeTime&#39;: &#39;04:04 AM&#39;}}]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="A-Recap-of-our-CollegeBoard-Requirements-Being-Met">A Recap of our CollegeBoard Requirements Being Met<a class="anchor-link" href="#A-Recap-of-our-CollegeBoard-Requirements-Being-Met"> </a></h3><ul>
<li><p>The Purpose - Right now, our purpose is to promote KFC. I personally think we should change it, but I also want to challenge myself to market something that I don't fully believe in, to better test my promotion and marketing skills. We may change our purpose in the future, but for now, this is our purpose</p>
</li>
<li><p>Data Abstraction, Managing Complexity, and Procedural Abstraction - With the use of JSON API's, we store data relevant to our purpose to use later for both frontend and backend development</p>
</li>
<li><p>Algorithm Implimentation - We are planning on using algorithms to make interactive features on our application that will help the user get hooked to purchasing from KFC</p>
</li>
<li><p>Testing - As the DevOps, I will make sure that the application is ready for deployment once Scrum Master Samarth and I come to a stage where we feel that it is indeed ready.</p>
</li>
</ul>

</div>
</div>
</div>
</div>
 
