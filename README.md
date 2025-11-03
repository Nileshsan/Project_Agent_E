# AI Email Agent

An intelligent email management system that uses machine learning to categorize, summarize, and manage emails efficiently. The system integrates with email providers through OAuth and provides smart email organization capabilities.

## Features

- **Email Classification**: Automatically categorizes emails into different types (tasks, reminders, newsletters, etc.)
- **Smart Summarization**: Generates concise summaries of email content
- **OAuth Integration**: Secure email access through Google OAuth
- **Web Interface**: User-friendly web application for email management
- **AI-Powered**: Uses deep learning models for intelligent email processing

## Project Structure

```
.
├── Application/          # Flask web application
│   ├── static/          # CSS, JavaScript, and other static assets
│   ├── templates/       # HTML templates
│   ├── app.py          # Main Flask application
│   └── requirements.txt # Python dependencies
│
├── Database_AI_Email/   # Training datasets and examples
│   ├── dataset_*.json  # Categorized email datasets
│   └── *_summary.json  # Email summary examples
│
├── vectorizers/        # Model vectorizer files
│   ├── input_vocab.txt # Input vocabulary for the model
│   └── target_vocab.txt# Target vocabulary for the model
│
├── Nilesh_AI.ipynb    # Jupyter notebook with model training code
└── README.md          # Project documentation
```

## Setup and Installation

1. **Environment Setup**:
   ```powershell
   # Create and activate virtual environment
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
   
   # Install dependencies
   pip install -r Application\requirements.txt
   ```

2. **OAuth Configuration**:
   - Create a project in [Google Cloud Console](https://console.cloud.google.com/)
   - Enable Gmail API
   - Create OAuth 2.0 credentials
   - Configure OAuth consent screen
   - Set up environment variables:
     ```
     # Application/.env
     GOOGLE_CLIENT_ID=your-client-id-here
     GOOGLE_CLIENT_SECRET=your-client-secret-here
     ```

3. **Run the Application**:
   ```powershell
   cd Application
   python app.py
   ```
   Access the web interface at `http://localhost:5000`

## Model Details

The project uses a deep learning model trained on a diverse email dataset to:
- Classify emails into categories
- Generate relevant summaries
- Extract key information

Model files:
- `Nilesh_Model_Final.keras`: Trained model (not in repository due to size)
- `vectorizers/`: Vocabulary files for text processing

## Security Considerations

- **OAuth Security**: Uses secure OAuth 2.0 for email access
- **Credentials**: All sensitive credentials stored in `.env` (not committed)
- **Model Storage**: Large model files stored separately from repository
- **Environment Variables**: Sensitive configuration managed via environment variables

## Development Guidelines

1. **Code Organization**:
   - Flask routes in `app.py`
   - Static assets in `static/`
   - Templates in `templates/`

2. **Dataset Management**:
   - Training data in `Database_AI_Email/`
   - Properly formatted JSON files
   - Include summary examples

3. **Model Development**:
   - Use `Nilesh_AI.ipynb` for model training
   - Keep vocabularies updated in `vectorizers/`
   - Document model changes

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to your branch
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Maintainers
- Nilesh

## Acknowledgments

- Thanks to contributors who provided email datasets
- Special thanks to the Flask and TensorFlow communities
- Inspired by modern email management needs
