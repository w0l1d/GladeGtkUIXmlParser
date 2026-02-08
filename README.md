# Glade GTK UI XML Parser

A C program that reads and parses [Glade](https://glade.gnome.org/) XML interface files and dynamically constructs the corresponding GTK+ window with all described widgets and attributes at runtime.

## Overview

Glade is a visual UI designer that exports interface descriptions as XML files. This parser reads those XML files directly and builds the GTK+ interface programmatically — without relying on GtkBuilder. It demonstrates low-level XML parsing and GTK widget construction in pure C.

## Tech Stack

- **C** — Core language
- **GTK+ 3** — GUI toolkit
- **Glade** — UI designer (XML source)
- **CMake** — Build system

## Features

- Parses Glade `.glade` XML files to extract widget hierarchy
- Dynamically creates GTK+ windows with all child widgets
- Supports widget attributes (size, position, labels, styling)
- CSS styling support via external stylesheets
- Image and background rendering within widgets
- Macro-based utility functions for common GTK patterns

## Project Structure

```
├── main.c                      # Application entry point
├── parsers.c / parsers.h       # XML parsing and GTK widget construction
├── utils.h                     # Utility macros
├── macros_supplimentaires.h    # Additional GTK helper macros
├── examTP.glade                # Sample Glade UI file
├── simplest interface.glade    # Minimal Glade UI example
├── exam2020.glade              # Exam-style Glade UI file
└── CMakeLists.txt              # Build configuration
```

## Getting Started

### Prerequisites

- GCC or Clang
- GTK+ 3 development libraries
- CMake 3.10+

### Build & Run

```bash
mkdir build && cd build
cmake ..
make
./parseGtkXML
```

## Academic Context

Built as part of the ILISI curriculum at FSTM, exploring systems programming with C and GUI development using GTK+.

## License

This project is provided for educational purposes.
