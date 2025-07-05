# AI Smartboard

An AI-powered interactive smartboard solution for modern classrooms, featuring real-time collaboration, AI teaching assistance, and various educational tools.

## Features

- **Interactive Whiteboard**: Draw, write, and annotate with various tools
- **AI Teaching Assistant**: 
  - Chat with AI for educational queries
  - Math problem solver with step-by-step solutions
  - Concept explainer with grade-level adjustments
  - Automatic quiz generation
- **Real-time Collaboration**: Teachers and students can interact in real-time
- **Classroom Management**: Create and manage multiple classrooms
- **Drawing Tools**: Pencil, eraser, shapes, text, and more
- **Export & Save**: Save whiteboard content as images

## Tech Stack

- **Frontend**: React, Fabric.js (canvas), Socket.io-client
- **Backend**: Node.js, Express, Socket.io
- **AI Integration**: OpenRouter API (supports multiple LLM models)
- **OCR**: Tesseract.js for text recognition

## Setup Instructions

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- OpenRouter API key

### Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file based on `.env.example`:
   ```bash
   cp .env.example .env
   ```

4. Add your OpenRouter API key to the `.env` file:
   ```
   OPENROUTER_API_KEY=your_api_key_here
   ```

5. Start the backend server:
   ```bash
   npm run dev
   ```

### Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the React development server:
   ```bash
   npm start
   ```

## Usage

### For Teachers

1. Open the application at `http://localhost:3000`
2. Go to Teacher Dashboard (`/teacher`)
3. Create a new classroom
4. Start a session to open the whiteboard
5. Share the student link with your class

### For Students

1. Use the student link provided by the teacher
2. Enter your name to join the classroom
3. View the whiteboard in real-time

### Whiteboard Tools

- **Drawing Tools**: Pencil, eraser, shapes (rectangle, circle, triangle, line)
- **Text Tool**: Add text annotations
- **Color Picker**: Choose drawing colors
- **Brush Size**: Adjust drawing thickness
- **Undo/Redo**: Navigate through drawing history
- **Save**: Export whiteboard as PNG
- **Clear**: Clear the entire canvas

### AI Features

1. **Chat Assistant**: Ask educational questions and get instant answers
2. **Math Solver**: Input math problems and get step-by-step solutions
3. **Concept Explainer**: Get explanations tailored to different grade levels
4. **Quiz Generator**: Automatically generate quizzes on any topic

## API Endpoints

- `POST /api/chat` - Chat with AI assistant
- `POST /api/solve-math` - Solve math problems
- `POST /api/explain-concept` - Explain educational concepts
- `POST /api/generate-quiz` - Generate quizzes
- `POST /api/ocr` - Extract text from images
- `POST /api/generate-diagram` - Generate educational diagrams

## WebSocket Events

- `join-room` - Join a classroom session
- `canvas-update` - Sync canvas state
- `drawing` - Real-time drawing updates
- `user-joined` - Notification when users join

## Future Enhancements

- Voice recognition for hands-free operation
- Screen recording and playback
- Assignment submission system
- Student analytics and progress tracking
- Integration with popular LMS platforms
- Multi-language support

## License

MIT License