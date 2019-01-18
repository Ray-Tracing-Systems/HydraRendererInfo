# Hydra Renderer Info

## Abstract

Hydra Renderer is a general purpose photo realistic rendering system. It is open source and free for commertial and non commetrial usage (under the most liberal MIT license). It can run both on CPUs and GPUs (however, GPUs are preferred). We position our system as one of the most efficient renderer in the world for complex light transport simulation phenomena. Our main advantages are bidirectional and Markov chain rendering algorithms, elaborated API and programmable shaders that allow you to integrate Hydra your custom application at low cost.   

## WHY use Hydra Renderer

If you need photo realistic rendering engine for your application that is:

* Fast (TBD: reference our comparison with octane here)
* Platform independent (Both OS and hardware independent)
* Free and Open Source
* Reliable solution with customer support (sou you can be sure it works for your particular cases and needs).
* Robust for complex light transport
* Have well specified rendering models for materials and lights. Sou you can feed renderer with existing content. (TBD: this is in progress) 
* Assume clear and transparent debugging during integration and customer development.

Hydra Renderer is propbably is what you are looking for.

## WHAT is Hydra Renderer

* 3-level abstraction solution.
  1. You custom applications. 
  2. HydraAPI. Agnostic intermediate layer between your application and rendering engine.
  3. Rendering engine (usually HydraCore, but you are supposed to make you own engines if this is needed).
  
* Well specified (TBD) rendering engine.


## HOW Hydra Renderer works

