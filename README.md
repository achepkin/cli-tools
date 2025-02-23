# CLI Tools

Personal collection of command-line tools to enhance daily workflow.

## 🛠 Tools

### pdfmerge (Merge PDFs)
Merges multiple PDF files in a directory into a single PDF file.

```bash
pdfmerge <directory>
```

### pdf2md (Convert PDF to Markdown)
Converts PDF files to Markdown format using PyMuPDF4LLM, with enhanced support for:

```bash
pdf2md <pdf_file> [-o output_file]
```

Features:
- Multi-column page support
- Better table detection and formatting
- Automatic header detection (H1-H6)
- Bold, italic, and code block formatting
- Ordered and unordered lists support
- Image and vector graphics extraction

## 🚀 Installation

1. First, ensure you have the required dependencies:
```bash
# macOS
brew install qpdf

# Ubuntu/Debian
sudo apt-get install qpdf python3-pip
```

2. Create a bin directory (if it doesn't exist):
```bash
mkdir -p ~/.local
```

3. Clone the repository:
```bash
git clone git@github.com:achepkin/cli-tools.git ~/projects/
```

4. Make scripts executable:
```bash
chmod +x ~/projects/cli-tools/*
```

5. Create symbolic links:
```bash
ln -s ~/projects/cli-tools/ ~/.local/bin/
```

6. Add the bin directory to your PATH:
```bash
# Add to ~/.zshrc or ~/.bash_profile
export PATH="$HOME/.local/bin:$PATH"
```

7. Reload your shell configuration:
```bash
source ~/.zshrc  # or source ~/.bash_profile
```

8. Verify installation:
```bash
pdfmerge --help
```

## 📁 Directory Structure
```
~/.local/
├── bin/            # Your executable scripts (symlinks)
└── cli-tools/      # This repository
    ├── pdfmerge   # PDF merger tool
    ├── pdf2md     # Enhanced PDF to Markdown converter
    ├── ...        # Other tools
    └── README.md   # This file
```

## 💡 Usage Examples

Merge all PDFs in a directory:
```bash
# Navigate to where you want the merged file
cd ~/Documents

# Merge PDFs from a specific directory
pdfmerge ~/Downloads/reports

# The merged file will be created as 'reports_merged.pdf'
```

Convert PDF to Markdown:
```bash
# Convert a PDF file to Markdown
pdf2md document.pdf

# Specify custom output path
pdf2md document.pdf -o custom_output.md
```

## 🔍 Requirements

- Shell: Bash or Zsh
- Dependencies:
  - qpdf: PDF manipulation tool
  - bc: Basic calculator (usually pre-installed)
  - Python 3.x
  - pymupdf4llm: Enhanced PDF to Markdown conversion

## 📝 License
