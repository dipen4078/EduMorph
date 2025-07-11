# Note
This project was developed specifically for macOS and is intended to run exclusively on that platform. It leverages macOS-compatible libraries and tools throughout.
# Edumorph
Edumorph is your AI-powered learning companion designed to help you master any topic—efficiently and intelligently. By assessing your current knowledge, goals, and time availability, it creates a personalized learning roadmap using the best resources from across the web.

It generates structured study schedules, explains concepts with tailored videos, and evaluates your understanding through dynamic quizzes. With continuous feedback and smart strategies for deeper comprehension, Edumorph transforms learning into an engaging, adaptive, and highly effective journey.

This project is designed to generate PowerPoint slides, voice explanations, and video presentations from a given topic and subtopic using the Groq API for natural language processing.

# Features:

1)Slide Generation: Automatically create PowerPoint slides on a given topic/subtopic.

2)Audio Explanation: Generate audio explanations for each slide using the gTTS library.

3)Video Creation: Convert PowerPoint slides into images and create a synchronized video using the moviepy library.

4)MCQ Test: Generate multiple-choice questions (MCQs) for testing knowledge on the topic.

5)PDF Generation: Generate detailed explanation and example and stores it to local disk as a PDF for in depth learning.

# Technologies Used:

  - Python
  
  - Flask: For web-based interaction and user interface.
  
  - Groq: For generating text content (slides and MCQs).
  
  - gTTS: For converting text to speech (audio explanations).
  
  - moviepy: For combining slides and audio into video.
  
  - FPDF: For generating PDFs with explanations.
  
  - pdf2image: For converting .pptx slides to images


# Prerequisites

Python 3.11

## Setup Instructions (macOS)

### 1. Clone the repository

```bash
git clone https://github.com/dipen4078/Edumorph.git
cd Edumorph
```
### 2. Create and activate a virtual environment(recommended)
```bash
python3 -m venv venv
source venv/bin/activate 
```

### 3. Install system-level dependencies(macOS)
Make sure Homebrew is installed
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Install system tools via
```bash
brew bundle
```
### 4. Install python dependencies
```bash
pip install -r requirements.txt
```

### 5. Configure Groq API key
Set up the Groq API by configuring your API key. Replace placeholder keys with your credentials in the code in line number 30 in place of your_api_key. You can generate it by following steps in the generate_key.txt file.

### 6. Run application
```python
python Edumorph.py
```
Navigate to host link generated in terminal.

# Key Functions:

1) generate_slides(): Generates a list of slide content based on the topic and subtopic using Groq.

2) create_ppt(): Converts the generated slides into a .pptx PowerPoint file.

3) convert_pptx_to_images(): Converts the PowerPoint slides into individual images.

4) generate_voice_explanations(): Generates voice explanations for each slide using gTTS.

5) create_video(): Combines the images and audio into a final video file.

6) generate_mcq_questions(): Generates multiple-choice questions for the given topic using Groq.

7) generate_pdf(): You can also generate detailed PDF Explanation for any topic by calling the generate_pdf function.

# Notes:

MacOS only.

Groq API: Ensure that Groq is properly configured for text generation.

# Contributing:
Feel free to submit issues or pull requests to improve the project.
