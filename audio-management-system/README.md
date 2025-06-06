# Audio Management System

A Strapi-based system for managing and processing bulk audio transcriptions and record keeping.

## Features

- Bulk audio file upload
- Audio file management and organization
- Transcription status tracking
- User role management
- API endpoints for audio processing
- Project-based organization

## Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- PostgreSQL (recommended) or SQLite
- FFmpeg (for audio processing)

## Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Configure your database in `config/database.js`
4. Start the development server:
   ```bash
   npm run develop
   ```

## Project Structure

```
audio-management-system/
├── config/
│   ├── database.js
│   ├── server.js
│   └── plugins.js
├── src/
│   ├── api/
│   │   ├── audio/
│   │   ├── project/
│   │   └── transcription/
│   ├── components/
│   └── extensions/
├── public/
└── uploads/
```

## Content Types

### Audio Files
- Title
- Description
- File (Media)
- Duration
- Status
- Project (Relation)
- User (Relation)

### Projects
- Name
- Description
- Status
- Audio Files (Relation)
- Users (Relation)

### Transcriptions
- Audio File (Relation)
- Text Content
- Status
- Language
- Timestamps

## API Endpoints

- POST /api/audio/upload - Upload audio files
- GET /api/audio - List audio files
- POST /api/projects - Create project
- GET /api/transcriptions - Get transcriptions
- PUT /api/transcriptions/:id - Update transcription

## Security

- JWT authentication
- Role-based access control
- File upload restrictions
- API rate limiting

## Development

1. Start the development server:
   ```bash
   npm run develop
   ```
2. Access the admin panel at http://localhost:1337/admin
3. Create your first admin user
4. Configure content types and permissions

## Production Deployment

1. Build the admin panel:
   ```bash
   npm run build
   ```
2. Start the production server:
   ```bash
   npm start
   ```

## License

MIT 