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
</ul>
</nav>

<!-- Main content (right column) -->
<main style="flex:1; padding:0 8px;">

---

## <a name="introduction"></a>Welcome & Introduction

Welcome to the OpenGl Tutorial.  
This tutorial will guide you through setting up an OpenGL environment using **Code::Blocks**, **MinGW**, **GLFW**,**GLAD**, and **GLM**.  

You’ll learn to:
- Configure OpenGL to your windows computer
- Build and run a minimal OpenGL program
- Render your first triangle
- Be able to edit shaders to change color using RGB values

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
- GLEW
---

## <a name="installation"></a>Setup & Installation

### Step 1: Install Code::Blocks with MingW
- Download from the [official Code::Blocks download site](https://sourceforge.net/projects/codeblocks/files/Binaries/25.03/Windows/codeblocks-25.03mingw-setup.exe/download)
- The .exe will already have the MingW version selected
- Complete installation with default settings
- When launching CodeBlocks, select the GNU MinGW Compiler from the pop-up menu and press "Ok".
### Step 2: Download Required Libraries
Download the following:
- **OpenGL** (included with your graphics driver)
- **GLFW** → [https://www.glfw.org/download.html](https://www.glfw.org/download.html) and select the 64-bit binary file.
- **GLEW** → [https://sourceforge.net/projects/glew/files/glew/2.1.0/glew-2.1.0-win32.zip/download.html)

### Step 3: Extract & Organize
- Begin by locating the desktop shotcut of CodeBlocks , right click and select open file path.
- Open the folder called MinGW ,then open the folder called lib.
- Open the glfw zip folder we just downloaded and open the /lib-mingw-w64 folder,drag all three files into the MinGW lib folder
- Do the same with the Glew zip folder and drag the two files. The path will look like: glew-2.2.0/lib/Release/x64
- Now open the include folder back in the main MinGW folder and drag the folders from both /include folders in the zips. Make sure to drag the entire folder named GL and GLFW
- Lastly return the the MinGW main folder and open the bin folder. Open the Glew.zip and open the bin folder. Drag the three files into the MinGW bin folder, the file path is: /glew-2.2.0/bin/release/x64.
  
### Step 4: Configure Project in Code::Blocks
- Create a new **Console Application (C++)**
- Go to **Settings → Compiler→ Linker Settings**
- Add the following libraries:
  - `opengl32`
  - `glfw3`
  - `glew32`
  - `gdi32`
  - `user32`
  - `kernel32`

### Step 5: copy , paste and run example program:
-Create a new consol appliation can paste the following code from this .txt file:

<a href="https://raw.githubusercontent.com/Marcos-TAMUCC/OpenGL-Tutorial/refs/heads/main/Triangle.cpp" download style="display:inline-block; margin-top:8px; padding:8px 12px; background:#0078d7; color:white; border-radius:4px; text-decoration:none;">
📄 Download OpenGL_Triangle_Code.txt

### Step 6: Tutorial complete
-If everything worked correctly a red triangle should appear on the screen.
-You can change the color of the triangle by editing the line of code:
-glUniform3f(colorLoc, 1.0f, 0.3f, 0.2f);  In RGB fashion.
  
---

## <a name="workflow"></a>Workflow

1. **Go to Setup Section:**  
   Begin by installing **Code::Blocks with MinGW**, and download **OpenGL**, **GLFW**, and **GLAD**.

2. **Place Libraries:**  
   The tutorial shows where to place each library folder and how to **link** them correctly in Code::Blocks.

3. **Open the Provided Code File:**  
   Open the attached `.txt` file that contains your first OpenGL program.  
   Create a **Console Application**, copy and paste the code into `main.cpp`.

4. **Run the Program:**  
   Build and run — a **triangle** should appear on screen!

5. **Modify Triangle Color:**  
   Open the shader file and modify the RGB color values to change the triangle color dynamically.

---
</main>
</div>
