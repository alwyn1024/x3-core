X3 Core XDK
===========

The X3 Core XDK is a cross-platform 3D graphics engine for the Xojo programming language. The XDK consists of two modules, X3Core and X3IO. X3Core contains all the core objects and methods needed for rendering, while X3IO provides routines to save and load 3D assets.

Usage
-----

Here are the basic steps to start a new X3 project:

1. Create a new Xojo desktop project.
2. Import the X3Core and X3IO modules into the project.
3. Add an OpenGLSurface control to your window.
4. Call X3_Initialize from the OpenGLSurface.Open event.
5. Call X3_SetPerspective from the OpenGLSurface.Resized event.
6. Call OpenGLSurface.Render from the Window.Paint event.
7. Add your rendering code to the OpenGLSurface.Render event, e.g.
  
	' set the background color

	OpenGL.glClearColor(0.2, 0.2, 0.2, 1) 
	OpenGL.glClear(OpenGL.GL_COLOR_BUFFER_BIT + OpenGL.GL_DEPTH_BUFFER_BIT)

	' render an X3Model

	OpenGL.glPushMatrix    
	OpenGL.glTranslatef 0, 0, -2    
	X3_RenderModel CurrentModel    
	OpenGL.glPopMatrix

