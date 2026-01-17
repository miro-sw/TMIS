# TMIS Portal (Modernized)

The Mother Institute of Science (TMIS) Management Portal.
This project has been modernized with a new UI using **Django** and **Tailwind CSS**.

## Prerequisites

- **Python** 3.8+
- **Node.js** 16+ (for building Tailwind CSS)

## Installation

1. **Clone the repository** (if applicable) or navigate to the project root.

2. **Set up a Virtual Environment** (Recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Python Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
   *Note: This project uses `crispy-tailwind` for form styling.*

4. **Install Node dependencies** (for Tailwind CSS):
   ```bash
   npm install
   ```

## Building CSS

Tailwind CSS needs to be built to generate the `output.css` file used by the templates.

- **One-time build**:
  ```bash
  npm run build:css
  ```

- **Watch mode** (during development):
  If you are changing HTML templates or styles, run this in a separate terminal:
  ```bash
  npx tailwindcss -i ./static/css/input.css -o ./static/css/output.css --watch
  ```

## Running the Application

1. **Apply Migrations**:
   ```bash
   python manage.py migrate
   ```

2. **Create Superuser** (if needed):
   ```bash
   python manage.py createsuperuser
   ```

3. **Run the Server**:
   ```bash
   python manage.py runserver
   ```

4. **Access the Portal**:
   Open [http://127.0.0.1:8000](http://127.0.0.1:8000) in your browser.

## Features

- **Modern UI**: Completely redesigned interface using Tailwind CSS.
- **Dark Mode**: Fully supported with auto-detection and a manual toggle.
- **Responsive**: Mobile-friendly sidebar and layouts.
- **Role-Based Access**: Student and Admin portals.
