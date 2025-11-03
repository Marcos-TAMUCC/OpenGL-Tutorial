# Technical Tutorial Task #4: OpenGL Demo  
**Team Name:** XM²  

<div style="display:flex; gap:32px; align-items:flex-start;">

<!-- Sidebar (left column) -->
<nav aria-label="Tutorial sidebar" style="width:260px; background:#ffffff; padding:16px; border:1px solid #e1e4e8; border-radius:6px; box-shadow:0 1px 3px rgba(0,0,0,0.05);">
<b>Sections</b>
<ul style="list-style:none; padding-left:8px; line-height:1.8;">
  <li><a href="#introduction">Introduction to OpenGL</a></li>
  <li><a href="#prerequisites">Setup Prerequisites</a></li>
  <li><a href="#installation">Installation</a></li>
  <li><a href="#demo">Demo</a></li>
</ul>
</nav>

<!-- Main content (right column) -->
<main style="flex:1; padding:0 8px;">

![OpenGL Banner](../images/banner.png "OpenGL Tutorial Banner") 

---

## <a name="introduction"></a>Welcome & Introduction

Welcome to **XM²’s OpenGL Horizontal Prototype Tutorial**.  
This tutorial will guide you through setting up an OpenGL environment using **Code::Blocks**, **MinGW**, **GLFW**, and **GLAD**.  

You’ll learn to:
- Configure OpenGL to your windows computer
- Build and run a minimal OpenGL program
- Render your first triangle
- Edit shaders to change color using RGB values

---

## <a name="prerequisites"></a>Prerequisites or Conditions

This tutorial assumes you:
- Are using **Windows**
- Have an **internet connection**
- Have a **CPU/GPU capable of running OpenGL**
- Have permission to install development software

**Tools & Libraries Needed**
- Code::Blocks IDE with MinGW compiler
- OpenGL
- GLFW
- GLAD

---

## <a name="installation"></a>Setup & Installation

### Step 1: Install Code::Blocks
- Download from the [official Code::Blocks site](https://www.codeblocks.org/downloads/)
- Choose the version **with MinGW included**
- Complete installation with default settings

### Step 2: Download Required Libraries
Download the following:
- **OpenGL** (included with your graphics driver)
- **GLFW** → [https://www.glfw.org/download.html](https://www.glfw.org/download.html)
- **GLAD** → [https://glad.dav1d.de/](https://glad.dav1d.de/)

### Step 3: Extract & Organize
- Place **GLFW** and **GLAD** folders inside your Code::Blocks project directory  
  Example: `C:\Users\<name>\Documents\OpenGL_Tutorial\libs\`

### Step 4: Configure Project in Code::Blocks
- Create a new **Console Application (C++)**
- Go to **Project → Build Options → Linker Settings**
- Add the following libraries:
  - `opengl32`
  - `glfw3`
  - `glew32` or `glad`
- Under **Search Directories**, add paths for:
  - Include: `libs\include`
  - Library: `libs\lib`

---

## <a name="workflow"></a>Workflow

1. **Go to Setup Section:**  
   Begin by installing **Code::Blocks with MinGW**, and download **OpenGL**, **GLFW**, and **GLAD**.

2. **Place Libraries:**  
   The tutorial shows where to place each library folder and how to **link** them correctly in Code::Blocks.

3. **Open the Provided Code File:**  
   Open the attached `.txt` file that contains your first OpenGL program.  
   Create a **Console Application**, copy and paste the code into `main.cpp`.

4. **Load Shaders:**  
   Import a provided shader file into your project to handle vertex and fragment operations.

5. **Run the Program:**  
   Build and run — a **triangle** should appear on screen!

6. **Modify Triangle Color:**  
   Open the shader file and modify the RGB color values to change the triangle color dynamically.

7. **Finish Tutorial:**  
   Congratulations — you’ve completed your first OpenGL render!

---

## <a name="demo"></a>Demo & Next Steps

Include:
- A **GIF or screenshot** of the running triangle
- (Optional) A link to a hosted demo repository

![Triangle Demo Placeholder](../images/demo.png "Triangle Render Example")

---

Navigation:  
[← Previous: Installation](#installation) • [Next: Shader Customization →](#workflow)

</main>
</div>
