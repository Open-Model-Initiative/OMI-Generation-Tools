=================
HDR Tools
=================

This section documents the HDR (High Dynamic Range) tools and utilities available in the repository.

HDR Data Creation Tools
======================

The repository provides multiple methods for creating HDR image data using different engines and tools.

Godot Engine
-----------

A free and open-source game engine with built-in HDR capabilities.

Features:
   - Free-flying camera script for HDR screenshots
   - Automatic file naming and organization
   - Saves in EXR format with PNG previews
   - Configurable camera controls

Setup:
   1. Add the camera script to a Camera3D node
   2. Configure input mappings:

      - ``screenshot`` -> left mouse
      - ``move_forward`` -> w
      - ``move_backward`` -> s
      - ``move_left`` -> a
      - ``move_right`` -> d
      - ``move_up`` -> e
      - ``move_down`` -> q

   3. Screenshots will be saved to a ``screenshots`` folder

Unreal Engine
------------

A professional game engine with HDR rendering capabilities.

Features:
   - Console-based HDR screenshot system
   - Supports multiple HDR formats
   - Professional-grade rendering

Usage:
   1. Position the editor camera
   2. Open console with tilde (~)
   3. Run command::

      HighResShot 1 filename="screenshot_00001.exr"

   4. Increment number for subsequent shots

HDR SDXL Generator
=================

A specialized tool for generating HDR images using StableDiffusionXL.

Key Features
-----------

- Generates HDR images by combining multiple exposures
- Supports both CLI and UI interfaces
- Multiple output formats:
   - EXR
   - HDR
   - DNG
   - TIFF

Operation Modes
-------------

Command Line Interface
^^^^^^^^^^^^^^^^^^^^

Suitable for batch operations. Available through wrapper scripts:

- Linux: ``hdr.sh``
- Windows: ``hdr.bat``

Key parameters:
   - ``--model``: SDXL model path
   - ``--prompt``: Generation prompt
   - ``--steps``: Number of sampling steps
   - ``--format``: Output format
   - ``--exp``: Exposure correction
   - ``--gamma``: Gamma adjustment

UI Interface
^^^^^^^^^^

Experimental interface based on Streamlit:

1. Install additional dependency::

      pip install streamlit

2. Launch the UI::

      streamlit run hdr.py

3. Optional arguments can be passed after ``--``::

      streamlit run hdr.py -- --model sdxl/model.safetensors

Technical Details
---------------

The HDR generation process:

1. Runs denoising loop for N-threshold steps
2. Stores interim latents
3. Modifies latents to mimic exposure changes
4. Completes remaining steps
5. Repeats for N-exposure steps
6. Merges multiple 8-bit images into single 16-bit HDR

Performance
^^^^^^^^^^

For standard settings (20 steps, 0.2 threshold):

- 16 base steps
- 3 x 4 steps for different exposures
- Total: 28 steps
- Overhead: ~20%

Contributing
===========

New HDR creation methods can be added by:

1. Creating a new subdirectory with a descriptive name
2. Including detailed setup instructions
3. Adding necessary scripts or configurations
4. Documenting licensing requirements
5. Providing example workflows
6. Updating the main documentation

See Also
========

- :doc:`index`
- :doc:`contributing/issues`
- `HDR SDXL Repository <https://github.com/OpenModelInitiative/generation-tools/tree/main/hdr/hdr_sdxl>`_ 