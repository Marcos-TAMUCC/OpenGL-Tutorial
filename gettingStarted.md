# Getting Started with OpenGL

<div style="display:flex; gap:32px; align-items:flex-start;">

<!-- Sidebar (left column) -->
<nav aria-label="Tutorial sidebar" style="width:260px; background:#ffffff; padding:16px; border:1px solid #e1e4e8;">
- **Welcome & Introduction**
- [Setup Prerequisites](#setup-your-environment)
- [First Program](#your-first-opengl-program)
- Rendering Pipeline
- Live Demo
- Summary & Quiz
</nav>

<!-- Main content (right column) -->
<main style="flex:1; padding:0 8px;">

![OpenGL Banner](../images/banner.png "OpenGL Tutorial Banner") <!-- replace with a real image -->

## Welcome & Introduction

Welcome to our tutorial. In this session you’ll learn how to set up your environment and create your first graphics program using OpenGL. We'll follow a step-by-step, hands-on approach: set up the toolchain, create a minimal OpenGL window, and walk through the basics of the rendering loop.

[Start Tutorial](#setup-your-environment)

---

## Setup Your Environment
<a name="setup-your-environment"></a>

Before writing code we’ll install and configure the tools and libraries you need to start building OpenGL applications.

### Prerequisites
- C++ compiler (GCC, Clang, or MSVC)
- IDE or editor (VS Code, CLion, Visual Studio)
- OpenGL loader and windowing library (GLAD or GLEW + GLFW or SDL)

### Installation Steps
1. Install a C++ compiler:
   - Windows: Install Visual Studio (Desktop development with C++) or Mingw-w64
   - macOS: Install Xcode command line tools
   - Linux: Install build-essential or the equivalent package
2. Install an IDE or editor:
   - VS Code (recommended): install C/C++ extensions
   - CLion or Visual Studio are also good choices
3. Install GLFW:
   - Using your package manager (brew, apt, pacman) or download binaries from the GLFW website
4. Install GLAD (or GLEW):
   - Generate a GLAD loader at https://glad.dav1d.de/ (select OpenGL, desired version, and language C/C++)
   - Or install GLEW through your package manager
5. Configure your project:
   - Add include paths for GLAD/GLFW
   - Link against glfw3, opengl32 (Windows) or OpenGL frameworks (macOS), and any other needed libraries

![IDE install screenshot](../images/ide-install.png "IDE installation") <!-- placeholder -->

Navigation: [Previous: Welcome & Introduction](#welcome--introduction) • [Next: Your First OpenGL Program](#your-first-opengl-program)

---

## Your First OpenGL Program
<a name="your-first-opengl-program"></a>

Here we’ll write a simple C++ program that creates a window with GLFW and an OpenGL context using GLAD, then runs a basic render loop that clears the screen.

### Code: Minimal window (GLFW + GLAD)
```cpp
// minimal_window.cpp
#include <glad/glad.h>
#include <GLFW/glfw3.h>
#include <iostream>

int main() {
    if (!glfwInit()) {
        std::cerr << "Failed to init GLFW\n";
        return -1;
    }

    glfwWindowHint(GLFW_CONTEXT_VERSION_MAJOR, 3);
    glfwWindowHint(GLFW_CONTEXT_VERSION_MINOR, 3);
    glfwWindowHint(GLFW_OPENGL_PROFILE, GLFW_OPENGL_CORE_PROFILE);

    GLFWwindow* window = glfwCreateWindow(800, 600, "OpenGL - Minimal Window", nullptr, nullptr);
    if (!window) {
        std::cerr << "Failed to create window\n";
        glfwTerminate();
        return -1;
    }

    glfwMakeContextCurrent(window);

    if (!gladLoadGLLoader((GLADloadproc)glfwGetProcAddress)) {
        std::cerr << "Failed to initialize GLAD\n";
        return -1;
    }

    // Main loop
    while (!glfwWindowShouldClose(window)) {
        // Input (poll events)
        glfwPollEvents();

        // Render
        glClearColor(0.1f, 0.12f, 0.15f, 1.0f);
        glClear(GL_COLOR_BUFFER_BIT);

        // Swap buffers
        glfwSwapBuffers(window);
    }

    glfwDestroyWindow(window);
    glfwTerminate();
    return 0;
}
```

### Quick explanations
#### Initializing GLFW
- glfwInit() sets up the library.
- glfwWindowHint(...) chooses an OpenGL profile and version.

#### Creating a window
- glfwCreateWindow(800, 600, ...) creates a window and a context.
- glfwMakeContextCurrent(window) makes the OpenGL context current for the calling thread.

#### Main loop
- Poll events with glfwPollEvents().
- Clear the screen each frame and swap buffers with glfwSwapBuffers().

### Run Example
- Build linking with glfw and your OpenGL implementation. Example (Linux/macOS):
  ```
  g++ minimal_window.cpp -o minimal_window -lglfw -ldl -lGL
  ```
- Run `./minimal_window` — you should see a blank window with the clear color.

Navigation: [Previous: Setup Prerequisites](#setup-your-environment) • [Next: Rendering Pipeline](#rendering-pipeline)

---

## Rendering Pipeline
This section will explain the programmable pipeline, shaders, VAOs/VBOs, and how to draw shapes. (Expand this section with examples of vertex and fragment shaders, buffer uploads, and a triangle draw call.)

---

## Live Demo
Include a link to a live demo (if hosted) or a recorded GIF showing the running program and a growing set of rendered objects.

---

## Summary & Quiz
Wrap up the key concepts and offer a short quiz to validate understanding:
- What function initializes GLFW?
- How do you swap buffers?
- What is the purpose of a shader program?

---

## Next steps / Conclusion
- Implement a triangle using a VAO/VBO.
- Add simple vertex and fragment shaders.
- Explore transformations and camera setup.

</main>
</div>
