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
  1. You custom application (for example Blender or 3ds Max plugin). It's yours. 
  
  2. Agnostic intermediate layer between your application and rendering engine called "HydraAPI".
     This level is well specifiend and was carefully designed to fulfill concrete reqremens:
     
     2.1. Interactivity. 
     2.2. No restrictions on memory.
     2.3. Parameters variability.
     2.4. Serialization.
     2.5. Debugging.
     2.6. Distributed rendering.
     
     By using Hydra API you can be sure that these reqremens will not be broken for existing or future rendering cores.
     This is achived by construction (TBD: reference our paper). 
     
  3. Rendering engine (usually HydraCore, but you are supposed to make you own engines if you want).
  
* Well specified (TBD) rendering engine.


## HOW Hydra Renderer works

