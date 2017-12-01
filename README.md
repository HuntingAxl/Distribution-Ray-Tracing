# Distribution-Ray-Tracing
In this project, we have used distribution ray tracing to create effects like Soft Shadows, Depth of Field and Motion Blur.

Team Size - 2

Operating System - Ubuntu

External libraries - 
  (linux) xorg-dev for GL/gl.h header file.
  (Windows) OpenGL library containing GL/gl.h .

Contributors:
  - HuntingAxl
  
# Effects Covered

Soft Shadows:-
  We have created area light sources for light sources and then we are sampling the shadow rays at every point. For creating soft shadows, we need to sample the area light source at point using an integral. In order to make this process computationally viable, We assume the area light source as a combination of point light sources present in a rectangular area. 

Depth of Field:-
  In this effect, the object near focus plane remain sharp and everything else becomes blurred. We simulate a lens in this effect. The rays start from a lens from the chosen pixel (i,j) and from any point on the lens, we try to collect samples with the help of rays going towards the focal plane. The rays are randomly chosen with the degree of randomness chosen with the aperture. We have set a focal distance which specifies the distance of focal plane from the camera.

Motion Blur:-
  The objects are moving, and we sample the values at a given pixel in number of samples.
  
The program enabled with all the effects takes quite a lot of time as it is unoptimized and running on the CPU only, you can expect the whole output in about 15-20 minutes. Optimizing the Ray Tracer was out of the scope of our project and thus it was left out.

