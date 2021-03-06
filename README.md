# Hydra Renderer Info

## Abstract

Hydra Renderer is a general purpose photo realistic rendering system. It is open source and free for commertial and non commetrial usage (under the most liberal MIT license). It can run both on CPUs and GPUs (however, GPUs are preferred). We position our system as one of the most efficient renderer in the world for complex light transport simulation phenomena. Our main advantages are Bidirectional and Markov Chain rendering algorithms (Kelemen Metropolis Light Transport (in progress) and Multiplexed Metropolis Light Transport), elaborated API and programmable shaders that allow you to integrate Hydra your custom application at low cost.   

## WHY use Hydra Renderer

If you need photo realistic rendering engine for your application that is:

* Real time and fast offline rendering (TBD: reference our comparison with octane here)
* Platform independent (Both OS and hardware independent)
* Free and Open Source
* Reliable solution with customer support (sou you can be sure it works for your particular cases and needs).
* Robust for complex light transport
* Have well specified rendering models for materials and lights. Sou you can feed renderer with existing content. (TBD: this is in progress) 
* Assume clear and transparent debugging during integration and customer development.

Hydra Renderer is propbably is what you are looking for.

## WHAT is Hydra Renderer

* 3-level abstraction solution.
  1. **You custom application** (for example Blender or 3ds Max plugin). It's yours.
     Btw our 3ds Max and Blender plugins are both open source.
  
  2. **Agnostic intermediate layer** between your application and rendering engine called "HydraAPI".
     This level is well specifiend and was carefully designed to fulfill concrete reqremens:
     
     1. Interactivity. You can add content (3d models, texture, materislas, shaders) quick and in a non blocking way.
     2. No restrictions on memory. You don't have to worry about memory. You "scene library" is supposed to exceed the available amount of RAM many times. 
     3. Parameters variability and extensibility. By using HydraAPI you can pass any desired models (of materials, lights or material parameters via "texture shaders") inside engine. Even such that is not yet supported by particular rendering engine.
     4. Serialization. All data is stored in XML and can be dumped to files for various needs (analysis, debugging, network transfer or other). 
     5. Debugging. All input to API is recorded for each object and can be reproduced without customer application for debugging or rendering purpose. However content loses editing ability. 
     6. Distributed rendering. The API is constructed in such a way that it can track changes of scene between "Commit" operations. So, only changes are supposed to transfer over network.
     
     By using Hydra API you can be sure that these reqremens will not be broken for existing or future rendering cores.
     This is achived by API construction (TBD: reference our paper). 
     https://github.com/Ray-Tracing-Systems/HydraAPI
     
  3. **Rendering engine** (usually HydraCore, but you are supposed to make you own engines if you want).
  
     Hydra is supposed to have many rendering engines for real time or offline rendering. 
     However currently we officially support only offline rendering engine called "HydraCore". 
     
     https://github.com/Ray-Tracing-Systems/HydraCore 
     
     It uses OpenCL (so it runs on Nvidia, AMD and late Intel GPUs and on CPUs too). It's OS independent. So we succesfully used it under Linux and Windows. It is fast and robust for complex lighting phenomena due to GPU optimised Bidirectional Path Tracing and Metropolis Light Transport algorithms.

## HOW can i use Hydra Renderer

   1. Download and build HydraAPI with Cmake or Visual Studio (yes, you don't have to use Cmake under Windows). https://github.com/Ray-Tracing-Systems/HydraAPI
   
   2. Install HydraCore (if under Linux you need to build it with Cmake). https://github.com/Ray-Tracing-Systems/HydraCore 
   
   3. Run samples from our non extisting SDK or run some tests from HydraAPI project (for example "test40_several_changes")
      We have C++ and Python API. If you need bindings for your language please let us know.
      
   4. Look through our feature spec pdf (TBD: add reference here) to figure out how to implement some feature in your application via Hydra Renderer. Or contact us if you have a questions.

