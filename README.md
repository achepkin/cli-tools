# CLI Tools

Personal collection of command-line tools to enhance daily workflow.

## 🛠 Tools

### mpdf (Merge PDFs)
Merges multiple PDF files in a directory into a single PDF file.

```bash
mpdf <directory>
```

### pdf2md (Convert PDF to Markdown)
Converts PDF files to Markdown format, preserving text and tables.

```bash
pdf2md <pdf_file> [-o output_file]
```

Features:
- Automatically finds all PDF files in the specified directory
- Shows progress with file sizes
- Creates output file named after the input directory
- Preserves original files
- Extracts text and tables from PDF
- Preserves basic formatting
- Supports custom output path
- Shows conversion progress

## 🚀 Installation

1. First, ensure you have the required dependencies:
```bash
# macOS
brew install qpdf
pip install pdfplumber

# Ubuntu/Debian
sudo apt-get install qpdf python3-pip
pip install pdfplumber
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
mpdf --help
```

## 📁 Directory Structure
```
~/.local/
├── bin/            # Your executable scripts (symlinks)
└── cli-tools/      # This repository
    ├── mpdf       # PDF merger tool
    ├── pdf2md     # PDF to Markdown converter
    ├── ...        # Other tools
    └── README.md   # This file
```

## 💡 Usage Examples

Merge all PDFs in a directory:
```bash
# Navigate to where you want the merged file
cd ~/Documents

# Merge PDFs from a specific directory
mpdf ~/Downloads/reports

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
  - pdfplumber: PDF text extraction library

## 📝 License
