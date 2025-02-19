Open Model Initiative - Generation Tools
=====================================

.. |License| image:: https://img.shields.io/badge/License-Apache%202.0-blue.svg
   :target: LICENSE

Welcome to the Open Model Initiative Generation Tools repository!

This repository serves as a home for various generation tools and experiments that support the Open Model Initiative's model and data missions. It provides a collection of utilities and cookbooks for specialized data generation tasks.

.. toctree::
   :maxdepth: 2
   :caption: Tools & Utilities
   
   hdr
   
.. toctree::
   :maxdepth: 2
   :caption: Contributing
   
   contributing/issues

Tools Overview
------------

HDR Tools
~~~~~~~~~
Collection of tools and utilities for working with High Dynamic Range (HDR) images:

- HDR SDXL Generator - Create HDR images using StableDiffusionXL
- HDR Data Instructions - Guides for creating HDR data using various engines
  
See :doc:`hdr` for detailed documentation.

About the Project
---------------

The Generation Tools repository is designed to be an experimental workspace for developing and sharing specialized data generation utilities. These tools complement our broader data curation and model development efforts, providing focused solutions for specific use cases.

Repository Structure
------------------

Each tool is contained in its own directory with dedicated documentation::

    generation-tools/
    ├── hdr/                # HDR tools and utilities
    │   ├── hdr_sdxl/       # HDR image generation via SDXL
    │   └── hdr_data_instructions/  # HDR creation guides
    ├── doc/                # Documentation
    └── future-tools/       # Additional tools to come

Contributing
-----------

We welcome contributions from the community! Whether you're:

- Adding new generation tools
- Improving existing utilities
- Fixing bugs
- Enhancing documentation

Please read our :doc:`contributing/issues` for more information on how to get started.

License
-------

|License|

This project is licensed under the `Apache License, Version 2.0 <https://www.apache.org/licenses/LICENSE-2.0.html>`_

Please see the license file for full details.

Contact
-------

For questions, suggestions, or discussions, please:

- Open an issue in this repository
- Join our community `Discord server <https://discord.gg/vANKjzDDkQ>`_

We look forward to your participation in the Open Model Initiative!

.. toctree::
   :maxdepth: 1
   :caption: Additional Resources
   :hidden:
   
   GitHub Repository <https://github.com/OpenModelInitiative/generation-tools>
   Discord Community <https://discord.gg/vANKjzDDkQ>