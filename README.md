# OpenVector

An open-source hardware and data repository for **VectorCam** — an AI-enabled mosquito-imaging tool built around a smartphone and a 3D-printed lens/light attachment. This repo holds everything a builder needs: the bill of materials, reference documents, and 3D-printable parts.

The full build guide — with an interactive parts list, cost calculator, and step-by-step instructions for Plan, Print, Assemble, Qualify, and Deploy — is here:

**[Build guide →](https://claude.ai/code/artifact/afdf79ba-fde8-4a13-9ad4-b09d487b3546)**

OpenVector is a community build guide. Visit [vectorcam.org](https://vectorcam.org) for more details.

## Repository structure
catalog/
catalog.csv Bill of materials — phones, hardware, filament, and lab equipment,
with sourcing links and cost. This is the source of truth for the
build guide's parts list; the guide re-syncs from this file.
docs/
tool-specifications.pdf
assembly-instructions.pdf
print-specifications.pdf
app-install.pdf
qualification-instructions.pdf
documentation-guidelines.pdf
stl/
3D-printable parts. See stl/README.md for the folder layout and naming convention.

