# Study Group Finder

## Project Overview

Study Group Finder is a comprehensive web-based platform designed to facilitate student collaboration through organized study groups. The application features real-time chat, session scheduling, file sharing, and robust group management tools, making it easier for students to connect and study together effectively.

## Features

1. **User Authentication System**: 
   - Secure registration and login with bcrypt password encryption
   - Session-based authentication with timeout protection
   - User-friendly error messaging
   - Automatic logout functionality

2. **Group Management**: 
   - Create and customize study groups
   - Join/leave existing groups
   - View available and joined groups
   - Advanced group creator privileges
   - Member removal with automatic redirection
   - Real-time group status updates

3. **Real-time Chat System**: 
   - Text messaging within groups
   - File sharing capabilities:
     - Support for multiple file types (PDF, DOC, XLS, etc.)
     - Image file preview
     - File preview before sending
     - File download functionality
     - File type detection and appropriate icons
   - Image handling:
     - Direct image preview in chat
     - Full-size image viewing modal
     - Image download capability
   - Automatic message updates (5-second intervals)
   - Message history persistence

4. **File Management**:
   - Support for various file types:
     - Documents (PDF, DOC, DOCX, TXT)
     - Spreadsheets (XLS, XLSX)
     - Presentations (PPT, PPTX)
     - Images (JPG, PNG, GIF)
     - Archives (ZIP, RAR, 7Z)
   - File preview features:
     - Image preview for image files
     - File information display for other types
     - File size and type information
   - Secure file storage
   - Easy file sharing interface

5. **Study Session Management**: 
   - Schedule study sessions with datetime picker
   - View upcoming sessions
   - Session management for group creators
   - Real-time session updates
   - Session deletion capability

6. **Member Management**: 
   - Real-time member list updates
   - Remove members (group creator only)
   - Automatic member redirection on removal
   - Member status tracking
   - Group creator immunity

7. **Responsive Interface**: 
   - Bootstrap 5-based responsive design
   - Real-time AJAX updates
   - Interactive notifications system
   - Modal-based forms and previews
   - Font Awesome icons integration

## Technical Stack

### Frontend:
- HTML5/CSS3
- Bootstrap 5
- Vanilla JavaScript
- Font Awesome 6.0
- AJAX for asynchronous operations

### Backend:
- PHP 7.4+
- MySQL Database
- Session Management
- File Upload Handling
- File Type Detection

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/study-group-finder.git
   ```

2. Database Setup:
   ```sql
   CREATE DATABASE study_group_finder;
   USE study_group_finder;
   
   -- Import the provided SQL schema
   source schema.sql;
   ```

3. Configure database connection in `php/db.php`:
   ```php
   $servername = "localhost";
   $username = "your_username";
   $password = "your_password";
   $dbname = "study_group_finder";
   ```

4. Server Requirements:
   - PHP 7.4 or higher
   - MySQL 5.7 or higher
   - Apache/Nginx web server
   - mod_rewrite enabled
   - GD Library for image processing
   - Appropriate file upload limits configured

5. File Permissions:
   ```bash
   chmod 755 -R /path/to/project
   chmod 777 -R /path/to/project/uploads
   ```

## Security Features

- SQL injection prevention using prepared statements
- XSS protection through input sanitization
- CSRF protection for forms
- Secure password hashing using bcrypt
- File upload validation and sanitization
- File type verification
- Session security with timeout
- Member removal tracking system

## Directory Structure

```
study-group-finder/
├── css/
│   └── styles.css              # Main stylesheet with custom styling
├── js/
│   ├── scripts.js              # Core JavaScript functionality
│   └── group-chat.js           # Chat and file handling functions
├── php/
│   ├── admin_dashboard.php     # Admin control panel
│   ├── chat.php               # Chat message handling
│   ├── create_group.php       # Group creation logic
│   ├── dashboard_data.php     # Dashboard data fetching
│   ├── db.php                 # Database connection configuration
│   ├── db.template.php        # Database configuration template
│   ├── delete_group.php       # Group deletion handling
│   ├── delete_session.php     # Session deletion logic
│   ├── fetch_chat_messages.php # Chat message retrieval
│   ├── fetch_groups.php       # Group list fetching
│   ├── get_sessions.php       # Study session retrieval
│   ├── group_data.php         # Group information handling
│   ├── join_group.php         # Group joining logic
│   ├── leave_group.php        # Group leaving functionality
│   ├── login.php              # User authentication
│   ├── logout.php             # Session termination
│   ├── register.php           # User registration
│   ├── remove_member.php      # Member removal handling
│   ├── schedule_session.php   # Study session scheduling
│   └── upload_image.php       # File upload handling
├── uploads/                   # File storage directory
│   └── .gitkeep              # Keeps the uploads directory in git
├── index.php                 # Application entry point
├── dashboard.php             # User dashboard interface
├── group.php                 # Group management interface
├── .gitignore               # Git ignore configuration
└── README.md                # Project documentation
```

## Future Improvements

1. **Enhanced Security**:
   - Two-factor authentication
   - API rate limiting
   - Enhanced password policies
   - Session fingerprinting
   - IP-based blocking
   - Advanced file scanning

2. **Feature Additions**:
   - WebRTC video chat
   - Advanced file preview
   - Calendar integration
   - Email notifications
   - Mobile app version
   - File version control

3. **Performance Optimization**:
   - Redis caching
   - Query optimization
   - Image compression
   - CDN integration
   - WebSocket implementation
   - Chunked file uploads

4. **UI/UX Improvements**:
   - Dark/Light theme toggle
   - Customizable interfaces
   - Keyboard shortcuts
   - Drag-and-drop uploads
   - Voice messages
   - File organization features

## Contributing

We welcome contributions! Please follow these steps:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

Copyright (c) 2024 Pui Hei Wong

This project is licensed under the MIT License. This means you are free to:
- Use this code commercially
- Modify this code
- Distribute this code
- Use this code privately
- Sublicense this code

See the [LICENSE](LICENSE) file for full details.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Support

For support, please open an issue in the GitHub repository or contact the maintainers.

## Acknowledgments

- Bootstrap team for the UI framework
- Font Awesome for the icon set
- All contributors and testers
- The open source community

## Database Configuration

1. Copy the database configuration template:
   ```bash
   cp php/db.template.php php/db.php
   ```

2. Edit `php/db.php` with your database credentials:
   ```php
   $servername = "your_host";
   $username = "your_username";
   $password = "your_password";
   $dbname = "your_database";
   $port = "your_port"; // Usually 3306
   ```

3. Make sure your database user has the necessary permissions.
