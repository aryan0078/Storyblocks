# Story Blocks

Story Blocks is an open-source project that utilizes generative AI to transform text into visual narratives. By combining OpenAI's text generation model and Stable Diffusion(Automatic1111) with LORA for image synthesis, this project allows users to explore new frontiers of storytelling.

## [One Click Run Google Colab](https://colab.research.google.com/github/adithya-s-k/Storyblocks/blob/main/Storyblocks.ipynb)

| Colab Page                                                                                                                                                                               | Function                          |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------- |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/adithya-s-k/Storyblocks/blob/main/Storyblocks.ipynb)               | Run Story blocks in One Click     |
| [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/adithya-s-k/Storyblocks/blob/main/Storyblocks_Automatic1111.ipynb) | Run Automatic1111 Web UI with API |

## Example

Input Prompt : Boy going to the moon

https://github.com/adithya-s-k/Storyblocks/assets/27956426/9ba3e564-a78b-47a7-a845-6f5155d44fbd

https://github.com/adithya-s-k/Storyblocks/assets/27956426/17864858-0eea-49a7-9299-d36f6bf6a01a

## Features

-   Transforms text prompts into captivating video narratives with vivid visuals
-   Uses cutting-edge AI technology for text, image, video generation like OpenAI , Automatic1111 and ElevenLabs
-   Customizable options to tailor user experience

## Usage

To use Story Blocks, simply provide a text prompt and watch as the project generates a unique story accompanied by stunning visuals. Users can customize their experience by adjusting various parameters such as image style and animation speed.

### **Todo list**

-   [x] complete video compilation pipeline
-   [x] add stable diffusion support for image generation
-   [x] add automatic1111 APIs
-   [x] add diffusechain
-   [x] Convert it into a Python file
-   [x] Add Colab notebook
-   [x] Add Gradio
-   [x] Project Creation and Section
-   [x] Implement Story Generation on Gradio
-   [x] Add Audio Generation using ElevenLabs
-   [x] Add Audio generation using pyttx3
-   [ ] Add SDXL Model for Image Generation locally
-   [ ] Add proper Subtitles support
-   [ ] Add Support for other image generation models (from Stability AI)
-   [ ] Add support for flashcards
-   [ ] prompts optimization
-   [ ] Become Automatic1111 agnostic

## 🌟 Show Your Support

We hope you find Storyblocks helpful! If you do, let us know by giving us a star ⭐ on the repo. It's easy, just click on the 'Star' button at the top right of the page. Your support means a lot to us and keeps us motivated to improve and expand Storyblocks. Thank you and happy content creating! 🎉

[![GitHub star chart](https://img.shields.io/github/stars/adithya-s-k/Storyblocks?style=social)](https://github.com/adithya-s-k/Storyblocks/stargazers)

# Instructions for running Storyblocks

This guide provides step-by-step instructions for installing ImageMagick and FFmpeg on your system, which are both required to do automated editing. Once installed, you can proceed to run `runStoryblocks.py` successfully.

## Prerequisites

Before you begin, ensure that you have the following prerequisites installed on your system:

-   Python 3.x
-   Pip (Python package installer)

## Installation Steps

Follow the instructions below to install ImageMagick, FFmpeg, and clone the Storyblocks repository:

### Step 1: Install ImageMagick

1. For `Windows` download the installer from the official ImageMagick website and follow the installation instructions.
   [https://imagemagick.org/script/download.php](https://imagemagick.org/script/download.php)
2. For Ubuntu/Debian-based systems, use the command:
    ```
    sudo apt-get install imagemagick
    ```
    Then run the following command to fix a moviepy Imagemagick policy.xml incompatibility problem:
    ```
    !sed -i '/<policy domain="path" rights="none" pattern="@\*"/d' /etc/ImageMagick-6/policy.xml
    ```
3. For macOS using Homebrew, use the command:

    ```
    brew install imagemagick
    ```

4. Verify the installation by running the following command:

    ```
    convert --version
    ```

    You should see the ImageMagick version information if the installation was successful.

### Step 2: Install FFmpeg (REQUIRED FOR STORYBLOCKS TO WORK)

1. For `Windows`Download the FFmpeg binaries from this Windows Installer (It will download ffmpeg, ffprobe and add it to your path).
   [https://github.com/icedterminal/ffmpeg-installer/releases/tag/6.0.0.20230306](https://github.com/icedterminal/ffmpeg-installer/releases/tag/6.0.0.20230306)
2. For macOS using Homebrew, use the command:
    ```
    brew install ffmpeg
    ```
    For Ubuntu/Debian-based systems, use the command:
    ```
    sudo apt-get install ffmpeg
    ```
3. Verify the installation by running the following command:

    ```
    ffmpeg -version
    ```

    You should see the FFmpeg version information if the installation was successful.

### Step 3: Clone the Storyblocks Repository

1. Open a terminal or command prompt.
2. Execute the following command to clone the Storyblocks repository:
    ```
    git clone https://github.com/adithya-s-k/Storyblocks.git
    ```

### Step 4: Install Python Dependencies

1. Open a terminal or command prompt.
2. Navigate to the directory where `runStoryblocks.py` is located (the cloned repo).
3. Execute the following command to install the required Python dependencies:

    ```
    pip install -r requirements.txt
    ```

    This command will install the necessary packages specified in the `requirements.txt` file.

## Running runStoryblocks.py Web Interface

Once you have successfully installed ImageMagick, FFmpeg, and the Python dependencies, you can run `runStoryblocks.py` by following these steps:

1. Open a terminal or command prompt.
2. Navigate to the directory where `runStoryblocks.py` is located (the cloned repo).
3. Execute the following command to run the script:
    ```
    python runStoryblocks.py
    ```
4. After running the script, a Gradio interface should open at your local host on port 4000 (http://localhost:4000).

## Contributing

We welcome contributions from the community to help improve Story Blocks. To contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch and make your changes.
3. Submit a pull request.

## Technologies Used

Storyblocks utilizes the following technologies to power its functionality:

-   **Moviepy**: Moviepy is used for video editing, allowing Storyblocks to make video editing and rendering

-   **Openai**: Openai is used for automating the entire process, including generating scripts and prompts for LLM automated editing processes.

-   **ElevenLabs**: ElevenLabs is used for voice synthesis, supporting multiple languages for voiceover creation.

-   **Diffusechain**: A library that makes it easier to generate images using diffusion models.

-   **Automatic1111**: A UI first project which is used to generate , modify images and much more.

These technologies work together to provide a seamless and efficient experience in automating video and short content creation with AI.

## License

Story Blocks is licensed under the MIT License. See `LICENSE` for more information.

## Contact

Stay updated with the latest happenings, announcements, and insights about Story Blocks by checking out my Twitter accounts. Engage in fascinating dialogues, access the latest news about the project, and gain insights from the person behind Story Blocks.

-   **Developer**: [@adithya-s-k](https://twitter.com/adithya_s_k).

<p align="center">
  <a href="https://adithyask.com">
    <img src="https://api.star-history.com/svg?repos=adithya-s-k/Storyblocks&type=Date" alt="Star History Chart">
  </a>
</p>
