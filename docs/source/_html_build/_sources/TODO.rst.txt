TO DO
======

Gantt Chart for Fall 2016 - Fall 2017
-------------------------------------
========  ===========
Acronymn  Description
========  ===========
OCP       optimal control problem
CL        close/d loop
OL        open loop
KE        known environment
UE        unknown environment
SO        static obstacles
MO        moving obstacles
VM        vehicle model
DOF       degree of freedom
VEXP      virtual experimentation
PEXP      physical experimentation
========  ===========

.. raw:: html

    <iframe src="_static/gantt.html" height="500px" width="180%"></iframe>

Current High Level Goals
------------------------
1) Close the Loop with the 14 DOF vehicle model

  * Put MATLAB on my UBUNTU machine
  * Create interface between MATLAB and julia

2) Close the Loop with the 3 DOF vehicle model

  * Create functionality in julia to solve ODEs given optimized control signals -> **DONE**
  * Figure out what is going on with infeasibility issue -> **Current Focus**


Weekly Meeting | 1/6/2017
----------------------------
**Accomplishments**

1) Developed functionality for:

  * Lagrange basis polynomials
  * LGR multiple interval
  * NLP Problem Initialization

2) Developed notes for:

  * Lagrange basis polynomials
  * LGR multiple interval
  * NLP Problem Initialization

3) Developed examples for:

  * Lagrange basis polynomials

    * Simple Interpolation
    * Investigated Runge's Phenomena

  * LGR multiple interval

    * Calculate derivatives
    * Calculate integrals
    * Approximate state at the end of the mesh grid

  * NLP Problem Initialization

    * Problem Initialization
    * Single Interval
    * Multiple Interval
    * Multiple States


**Goals**

1) Continue to on package NLOptControl.jl package

2) Meet with Jiayan



Future Ideas:
-------------

