# Photo Gallery App - Django

A fully-featured Django-based gallery application where users can upload images, which are stored in an AWS S3 bucket. The app allows users to filter images by category, providing an efficient way to manage and view your photo collection.

## Features

- **AWS S3 Integration**: Images are securely uploaded to and served from AWS S3, ensuring scalable and reliable storage.
- **Category Filtering**: Easily filter and view images by category, enhancing user experience.
- **User Authentication**: Secure login/logout functionality to protect user data and manage access.

## Prerequisites

Before you begin, make sure your system meets the following requirements:

- **Python 3.x**: Ensure you have Python 3.x installed on your local machine.
- **Django 3.2.10 or later**: The project is built on Django, so you'll need version 3.2.10 or later.
- **AWS Account**: You'll need an AWS account with an S3 bucket configured to store images.
- **AWS Credentials**: Have your S3 Access Key and Secret Key ready for configuring the application.

## Installation

Follow these steps to set up the project locally:

1. **Clone the Repository**:

    Begin by cloning the repository to your local machine using Git:

    ```bash
    git clone https://github.com/yourusername/photo-gallery-app-django.git
    cd photo-gallery-app-django
    ```

2. **Create a Virtual Environment**:

    It’s recommended to create a virtual environment to manage dependencies:

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

3. **Install Dependencies**:

    Install the necessary Python packages using `pip`:

    ```bash
    pip install -r requirements.txt
    ```

    Your `requirements.txt` file should include the following:

    ```plaintext
    Django==3.2.10
    boto3==1.26.10
    Pillow==9.2.0
    django-storages==1.13.1
    ```

4. **Configure Environment Variables**:

    Set up your environment variables to securely manage AWS S3 credentials and Django settings. Create a `.env` file in the project root with the following content:

    ```plaintext
    AWS_ACCESS_KEY_ID=your-access-key-id
    AWS_SECRET_ACCESS_KEY=your-secret-access-key
    AWS_STORAGE_BUCKET_NAME=your-bucket-name
    SECRET_KEY=your-django-secret-key
    DEBUG=True
    ```

5. **Apply Database Migrations**:

    Prepare your database by applying migrations:

    ```bash
    python manage.py migrate
    ```

6. **Run the Development Server**:

    Start the Django development server to view your app locally:

    ```bash
    python manage.py runserver
    ```

7. **Access the Application**:

    Open your web browser and go to `http://127.0.0.1:8000/` to access the gallery app.

## Usage

- **Login**: Use the provided login functionality to authenticate and manage your images.
- **Upload Images**: Easily upload images to your gallery, which will be stored in your AWS S3 bucket.
- **Filter by Category**: Organize and view your images by selecting specific categories.

## Dependencies

This project requires the following dependencies:

- **Django 3.2.10+**: A high-level Python web framework that encourages rapid development and clean, pragmatic design.
- **boto3**: The AWS SDK for Python, used for accessing AWS services including S3.
- **Pillow**: A Python Imaging Library that adds image processing capabilities to your application.
- **django-storages**: A collection of custom storage backends for Django, used here for managing files with AWS S3.

## Contact

If you have any questions or need further assistance, feel free to contact the repository owner via [GitHub](https://github.com/ShauryaDusht).
