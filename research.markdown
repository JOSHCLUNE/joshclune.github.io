---
layout: page
title: Research 
permalink: /research/
---
<head>
	<link href="{{site.baseurl}}/css/common.css" rel="stylesheet">
</head>

<!-- Tab links -->
<div class="tab">
  <button class="tablinks" onclick="openCity(event, 'Keller')" id="defaultOpen">Keller Reduction</button>
  <button class="tablinks" onclick="openCity(event, 'PLF')">PLF</button>
  <button class="tablinks" onclick="openCity(event, 'Zeus')">Zeus</button>
</div>

<!-- Tab content -->
<div id="Keller" class="tabcontent">
<h4>A Formalized Reduction of Keller's Conjecture</h4>
<center>
<img style="float: center; padding-bottom: 20px" src="../img/Keller_Picture.png" alt="An arrow pointing from a tiling of three-dimensional cubes to a Keller graph" width="400"/>
</center>

<p>
If you attempted to entirely cover a 2-dimensional Euclidean plane with non-overlapping unit squares, you would quickly find that it is necessary to have at least two squares share a complete edge. Similarly, if you attempted to fill a 3-dimensional Euclidean space with non-overlapping unit cubes, you would find that it is necessary to have at least two cubes share a complete face.
</p>

<p>
Keller's Conjecture states that this trend holds in arbitrary dimensions. In precise terms, it states that any tiling of n-dimensional Euclidean space by identical hypercubes must contain at least two hypercubes that share an (n-1)-dimensional face. As it turns out, Keller's Conjecture is true up to and including dimension 7, and false afterwards, a result that strikes me as deeply arbitrary.
</p>

<p>
The proof that Keller's Conjecture holds in dimension 7 critically relies on a reduction from the original geometric conjecture to a finite graph clique problem. My research involves using the interactive theorem prover Lean to formalize this reduction and obtained a verified proof of it. 
</p>
</div>

<div id="PLF" class="tabcontent">
  <h4>A Polymorphic Logical Framework</h4>
  <center>
  <img style="float: center; padding-bottom: 20px" src="../img/PLF_Syntax.png" alt="The syntax of PLF" width="500"/>
  </center>
  <p> The LF logical framework is a formal system designed to provide a general means of presenting deductive systems. But the ease with which a logical framework can present certain deductive systems and support various applications depends significantly on the language features provided by that framework. For this reason, attention has been given to areas in which LF can be improved for certain applications, yielding extensions to LF such as LLF (a linear logical framework), RLF (a logical framework for relevant logics), and CLF (a concurrent logical framework).
</p>

<p>
My research with <a href="https://www.cs.cmu.edu/~crary/">Karl Crary</a> involves developing an extension to LF that supports representing and reasoning about polymorphic types. The primary aims for this work are to define the extension’s type system and semantics, validate it by proving that the system honors identity expansion and cut admissibility, and potentially formalize the extension and the proofs that validate it in Coq.
</p>
</div>

<div id="Zeus" class="tabcontent">
  <h4>Program Equivalence for Assisted Grading of Functional Programs</h4>
  <center>
  <iframe height="175px" src="https://www.youtube.com/embed/kEefoZ2sTho" allowfullscreen="true"></iframe>
  </center>
  <p>In courses that involve programming assignments, giving meaningful feedback to students is an important
challenge. In a perfect world, every student would receive personalized human feedback. But as computer science courses grow in demand, this ideal is increasingly costly.</p>

<p>To make human feedback more accessible, even as class sizes grow considerably, I worked with <a href="https://vijayramamurthy.me/">Vijay Ramamurthy</a>, <a href="https://sat-group.github.io/ruben/">Ruben Martins</a>, and <a href="https://www.umut-acar.org/">Umut Acar</a> to create <a href="https://github.com/CMU-TOP/zeus">Zeus</a>. Zeus is a tool that can take a set of programs written in Standard ML, and, using the SMT solver Z3, partition them into buckets of provably equivalent programs. This makes it possible to simultaneously give human feedback to all students that implemented the same algorithm or made the same error.
</p>
 
<p>
To learn more about how Zeus is designed, and how it can be used to make human feedback more accessible, feel free to watch my OOPSLA talk embedded above. For more information on Zeus' theoretical foundations, you can read our conference paper <a href="{{ site.baseurl }}/pdfs/zeus.pdf">here</a> and its extended version <a href="{{ site.baseurl }}/pdfs/zeus_extended.pdf">here</a>. 
</p>
</div>
<script src="{{site.base.url}}/js/common.js"></script>
