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
  <button class="tablinks" onclick="openCity(event, 'Duper')" id="defaultOpen">Duper</button>
  <button class="tablinks" onclick="openCity(event, 'Keller')">Keller Reduction</button>
  <button class="tablinks" onclick="openCity(event, 'PLF')">PLF</button>
  <button class="tablinks" onclick="openCity(event, 'Zeus')">Zeus</button>
</div>

<!-- Tab content -->
<div id="Duper" class="tabcontent">
<h4>Duper: A Higher-Order Proof Producing Theorem Prover</h4>
<center>
<img style="float: center; padding-bottom: 5px" src="../img/Duper_Example.png" alt="A screenshot of Duper proving a Group theory lemma" width="620"/>
</center>

<p>
One of the most important factors impacting the usability of an interactive theorem prover (ITP) is the power of its automation. For example, in Isabelle/HOL, the general purpose automation provided by Metis and Sledgehammer has become an essential part of the typical user's workflow.
</p>
<p>
Most current ITP automation is either targeted to a particular domain or designed primarily for first-order logic. But most ITPs support a language much richer than that of first-order logic. My research with Yicheng Qian and <a href="https://abentkamp.github.io/">Alexander Bentkamp</a> concerns general-purpose ITP automation designed to handle higher-order logic. Together we are developing <a href="https://github.com/leanprover-community/duper">Duper</a>, an automatic theorem prover in Lean 4 based on the superposition calculus. We intend to make Duper capable of native higher-order reasoning, and we are also exploring how it might be extended to additionally support reasoning in the presence of dependent types.
</p>
</div>

<div id="Keller" class="tabcontent">
<h4>A Formalized Reduction of Keller's Conjecture</h4>
<center>
<iframe height="175px" src="https://www.youtube.com/embed/3EtEGxWB6Gs" allowfullscreen="true"></iframe>
</center>

<p>
If you attempted to entirely cover a 2-dimensional Euclidean plane with non-overlapping unit squares, you would quickly find that it is necessary to have at least two squares share a complete edge. Similarly, if you attempted to fill a 3-dimensional Euclidean space with non-overlapping unit cubes, you would find that it is necessary to have at least two cubes share a complete face.
</p>

<p>
Keller's Conjecture states that this trend holds in arbitrary dimensions. As it turns out, Keller's Conjecture is true in 7 or fewer dimensions, and is false in 8 or more dimensions.
</p>

<p>
The proof that Keller's Conjecture holds in 7 dimensions critically relies on a reduction from the original geometric conjecture to a finite graph clique problem. My research involved using the Lean 3 theorem prover to formalize and verify this reduction. I also used this formalized reduction to produce the first verified proof that Keller's Conjecture is false in 8 dimensions. You can read more about this work <a href="{{ site.baseurl }}/pdfs/Keller_Reduction.pdf">here</a>, and you can check out the formal proofs <a href="https://github.com/JOSHCLUNE/Keller_reduction">here</a>.
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
My research with <a href="https://www.cs.cmu.edu/~crary/">Karl Crary</a> involved developing an extension to LF that supports representing and reasoning about polymorphic types. The primary aims for this work were to define the extension’s type system and semantics, validate it by proving that the system honors identity expansion and cut admissibility, and potentially formalize the extension and the proofs that validate it in Coq.
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
To learn more about how Zeus is designed, and how it can be used to make human feedback more accessible, feel free to watch my OOPSLA talk embedded above. For more information on Zeus' theoretical foundations, you can read our conference paper <a href="{{ site.baseurl }}/pdfs/Zeus.pdf">here</a> and its extended version <a href="{{ site.baseurl }}/pdfs/Zeus_extended.pdf">here</a>. 
</p>
</div>
<script src="{{site.base.url}}/js/common.js"></script>
