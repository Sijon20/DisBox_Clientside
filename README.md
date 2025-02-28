# Disbox Client

A web-based file management application that uses Discord webhooks for storage. Built with Vue.js and Tailwind CSS.

## Features

- **File Management**
  - Upload and download files
  - Create, rename, and delete folders
  - Move files and folders
  - Support for large files with chunking
  - File type icons for better visualization

- **Modern UI**
  - Responsive design for mobile and desktop
  - Dark/Light theme with system preference support
  - Progress indicators for operations
  - Context menu for quick actions
  - Breadcrumb navigation

- **Data Management**
  - Import/Export backup (metadata) functionality
  - IndexedDB for local meta data storage
  - Files stored on discord

## Technical Stack

- **Frontend Framework**: Vue.js 3 (Production Build)
- **CSS Framework**: Tailwind CSS
- **Icons**: Font Awesome
- **Storage**: Discord Webhooks + IndexedDB
- **File Handling**: Chunk-based upload/download (8MB chunks)

## Setup

1. Open the application in a web browser
2. Enter your Discord webhook URL when prompted
3. Start managing your files

## Theme Support

- Automatic dark/light theme detection based on system preferences
- Manual theme toggle available
- Dark theme optimized for reduced eye strain

## File Operations

### Upload
- Supports any file type
- Automatic file chunking for large files
- Progress tracking during upload

### Download
- Direct download for supported browsers
- Fallback to manual part downloading
- Progress tracking during download

### Organization
- Create nested folder structures
- Move files between folders
- Rename files and folders
- Delete files and folders

## Storage Implementation

The application uses Discord webhooks as a storage backend:
- Files are split into 8MB chunks for Discord's file size limits
- Each chunk is uploaded as a separate attachment
- File metadata and structure are stored in IndexedDB
- Backup functionality for exporting/importing data

## Browser Support

Requires a modern browser with support for:
- IndexedDB
- Fetch API
- Blob API
- ES6+ JavaScript features

## Coming Soon

- File sharing functionality
- Local file caching
- Improved mobile experience
- Enhanced file preview capabilities