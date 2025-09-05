# Pinterest Bot II

This script automates creation and scheduling of Pinterest posts based on viral Amazon products. It uses the OpenAI API to gather product details and generate Pinterest titles, descriptions, and tags, then schedules posts through [Bundle.social](https://bundle.social).

## Prerequisites

```bash
sudo apt update
sudo apt install -y python3 python3-venv python3-pip git
```

## Setup

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd pinterest-bot-ii
   ```

2. **Create and activate a virtual environment (recommended)**

   ```bash
   python -m venv .venv
   source .venv/bin/activate  # Windows: .venv\Scripts\activate
   ```

3. **Install Python dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Set environment variables**

   Copy the example file and add your API keys:

   ```bash
   cp .env.example .env
   # then edit .env with your OpenAI and Bundle.social keys
   ```

## Usage

Run the scheduler:

```bash
python main.py
```

The script continuously finds a viral Amazon product, uploads an image to Bundle.social, and schedules Pinterest pins for the configured teams at 09:00, 13:30, and 20:00 America/New_York time.

