# YouTube Video to Article Generator

## Overview

This project aims to automate the process of generating articles from YouTube videos. Users can register and login to the platform, where they can paste the link to a YouTube video. The system then retrieves the video, extracts its transcript using the Assembly AI API, and generates an article based on the transcript using the Gemini API. The generated article is saved in the user's profile for future reference.

## Features

1. **User Registration and Authentication**: Users can register for an account and log in securely to access the platform's features.

2. **YouTube Video Link Submission**: Users can paste the link to a YouTube video they want to generate an article from.

3. **Video Download**: The system automatically retrieves the YouTube video associated with the provided link.

4. **Transcript Extraction**: The Assembly AI API is utilized to extract the transcript from the video.

5. **Article Generation**: The extracted transcript is used as input for the Gemini API to generate an article summarizing the video content.

6. **User Profile**: Generated articles are saved in the user's profile for easy access and reference.

## Technology Stack

- **Backend Framework**: Django is used for the backend development, providing a robust and scalable framework for building web applications.
  
- **Database**: Render for cloud PostgreSQL database is utilized as the database management system, ensuring data integrity and reliability.
  
- **APIs**:
  - **Assembly AI API**: Used for extracting transcripts from YouTube videos.
  - **Gemini API**: Utilized for generating articles based on the extracted transcripts.

## Installation

To set up the project locally, follow these steps:

1. Clone the repository: ``` git clone https://github.com/shoplikov/youtube-to-article.git ```

2. Move to the project directory

3. Create config.py file to include the neccesary keys for: `POSTGRES_KEYS`, `ASSEMBLY_AI_API` and `GEMINI_API` variables

3. Apply database migrations
``` python manage.py migrate ```

4. Run the server
``` python manage.py runserver ```

5. Access the application at http://localhost:8000.
