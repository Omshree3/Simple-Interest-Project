# Simple-Interest-Project

import zipfile

# File contents
files = {
    'LICENSE': """Apache License\nVersion 2.0, January 2004\n... (full license text) ...""",
    'README.md': """# Simple Interest Calculator\n\nThis project contains a shell script that calculates simple interest based on user input.\n\n## Usage\n1. Run the script using `bash simple-interest.sh`.\n2. Input principal, rate, and time when prompted.\n3. The script calculates and displays the simple interest.""",
    'CODE_OF_CONDUCT.md': """# Code of Conduct\n\nAll participants are expected to adhere to respectful and inclusive behavior.\n- Be respectful\n- Avoid offensive language\n- Follow contribution guidelines""",
    'CONTRIBUTING.md': """# Contributing Guidelines\n\nTo contribute:\n1. Fork the repository\n2. Create a branch for your changes\n3. Submit a pull request\n4. Follow coding standards and include meaningful commit messages""",
    'simple-interest.sh': """#!/bin/bash\n# Simple Interest Calculator\nread -p 'Enter Principal Amount: ' P\nread -p 'Enter Rate of Interest: ' R\nread -p 'Enter Time (years): ' T\nSI=$((P * R * T / 100))\necho 'Simple Interest is: ' $SI"""
}

# Create ZIP file
with zipfile.ZipFile('/mnt/data/simple_interest_project.zip', 'w') as zipf:
    for filename, content in files.items():
        zipf.writestr(filename, content)

'/mnt/data/simple_interest_project.zip'
