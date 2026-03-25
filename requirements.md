# Requirements Document

## Project Goals and Objectives
- Create an educational Flutter application for children aged 8+ years
- Provide interactive AI-powered chatbot for learning core concepts
- Support both learning and assessment modes
- Ensure child-friendly, secure, and distraction-free environment
- Enable cross-platform deployment (Android, iOS, Web, Desktop)
- Restructure the application for better modularity to easily accommodate new features such as user authentication, offline mode, data synchronization, and advanced analytics
- Enhance security with a logout/reset feature for clearing child data and allowing new child setup
- Improve debugging with centralized logging, error reporting, crash analytics, and detailed debug traces

## Functional Requirements

### Core Features
- **AI Chatbot Integration**: Interactive conversational AI using OpenRouter's preset model with multimodal capabilities
- **Dual Mode Operation**:
  - Learning Mode: Free-form exploration and teaching of concepts
  - Assessment Mode: Structured 10-question evaluation with difficulty progression
- **Image Support**: Upload images from camera or gallery for AI analysis
- **PDF Support**: Upload PDF documents (worksheets, textbook pages) from file picker for AI analysis
- **Progress Tracking**: Monitor student performance and learning milestones
- **User Profile Management**: Store student information (name, birth year, grade, learning medium)
- **Logout/Reset Feature**: Provide a mechanism to securely clear entered child data and allow setup for a new child/student
- **Modular Architecture**: Restructure the codebase into separate modules (screens, services, utilities, widgets) for better maintainability and feature addition
- **Windows Desktop Support**: Provide EXE installer for Windows laptops, enabling teachers to install and use the application locally
- **Student Demo Account**: Offer a one-week trial access without payment
- **Convert Demo to Regular Account**: Upgrade demo account automatically upon fee confirmation
- **Drawing Board**: Integrated drawing board in the chat interface for rough work and calculations

### User Interface
- **Consent Screen**: Age verification using birth year and parental consent collection
- **Welcome Screen**: Mode selection (Learn/Assess) with app version display
- **Chat Interface**: WebView-based chat UI with image and PDF upload capabilities
- **Kiosk Mode**: Immersive fullscreen experience preventing distractions
- **Exit Protection**: Secret key required to exit the application

### Data Management
- **Local Storage**: SQLite database for sessions, questions, answers, and progress
- **Session Persistence**: Save at least one previous session and current ongoing session for continuation across app launches
- **Secure Storage**: Encrypted storage for sensitive user data and API keys
- **Firebase Integration**: Remote prompt templates and potential future cloud features

## Non-functional Requirements

### Performance
- Fast app startup and smooth WebView interactions
- Efficient image processing and base64 encoding
- Efficient PDF processing with size optimization
- Responsive UI suitable for touch interfaces

### Security
- Age-appropriate content filtering
- Encrypted data storage complying with privacy regulations
- Secure API key management
- Kiosk mode preventing unauthorized access
- Logout/reset functionality for secure clearing of child data

### Debugging
- Centralized logging system for tracking app events and errors
- Error reporting and crash analytics for issue identification
- Debug mode with detailed traces for development and troubleshooting

### Scalability
- Modular architecture supporting future feature additions
- Firebase-based prompt management for easy updates
- Cross-platform compatibility

### Usability
- Child-friendly interface with simple navigation
- Intuitive image upload process
- Intuitive PDF upload process with file picker
- Clear mode distinction (Learn vs Assess)
- Accessible design for young learners

## User Stories

### Student User Stories
- As a student, I want to choose between learning new concepts or taking assessments
- As a student, I want to upload images of my homework or textbook pages for AI analysis
- As a student, I want to upload PDF worksheets or textbook pages for AI analysis
- As a student, I want the AI to explain concepts in an age-appropriate way
- As a student, I want to track my learning progress over time

### Parent/Teacher User Stories
- As a parent, I want to ensure my child only accesses educational content
- As a parent, I want to review my child's learning progress
- As a teacher, I want to see assessment results to identify areas needing reinforcement
- As a tuition teacher, I want to install the application as an EXE on my Windows laptop for offline use

## Deliverables and Milestones

### MVP Deliverables
- ✅ Basic Flutter app structure with consent screen
- ✅ WebView integration with HTML chat interface
- ✅ AI chatbot integration (OpenRouter API)
- ✅ Image upload functionality (camera/gallery)
- ✅ Local SQLite database for data persistence
- ✅ Secure storage for user data
- ✅ Kiosk mode implementation
- ✅ Firebase setup for prompt management
- 🔄 Application restructuring for modularity
- 🔄 Logout/reset feature implementation
- 🔄 Student demo account (one-week trial)
- 🔄 Convert demo to regular account after fees confirmation
- 🔄 Debugging tools integration

### Future Enhancements
- 🔄 Advanced progress analytics and reporting
- 🔄 Multi-language support beyond English/Hindi
- 🔄 Offline mode capabilities
- 🔄 Parent dashboard for progress monitoring
- 🔄 Integration with educational platforms
- 🔄 Windows EXE build and installer for desktop deployment
- 🔄 Specified subject tutor: Maths, Science, English and Language
- 🔄 Master login for teacher
- ✅ SVG support in AI chat box
- 🔄 Drawing board in chat box for rough work and calculations

## Constraints and Assumptions

### Technical Constraints
- Target platforms: Android (primary), iOS, Web, Desktop
- Flutter SDK version: ^3.10.4
- WebView dependency limitations for some platforms
- Firebase Storage for prompt management

### Business Constraints
- Educational focus to all academic curriculum
- Age range: 8+ year
- Content must be child-appropriate and educational

### Assumptions
- Internet connectivity available for AI interactions
- OpenRouter API availability and reliability
- Firebase services remain accessible
- Image and PDF sizes remain within reasonable limits for mobile processing
- PDF documents are text-based educational materials (worksheets, textbook pages)

## Tracker Status

### Requirements Status
- ✅ Core chatbot functionality implemented
- ✅ Image upload feature implemented
- ✅ PDF upload feature (file picker) - Completed
- ✅ User consent and profile management implemented (consent schema versioning added)
- ✅ Kiosk mode implemented
- ✅ Basic progress tracking implemented
- 🔄 Advanced analytics pending
- 🔄 Parent dashboard pending
- 🔄 Multi-language expansion pending
- 🔄 Windows EXE build and installer in progress (SDK setup required)
- 🔄 Session persistence pending
- ✅ Application restructuring for modularity completed
- ✅ Logout/reset feature completed
- ✅ SVG support in AI chat box completed
- 🔄 Student demo account (one-week trial) pending
- 🔄 Convert demo to regular account after fees confirmation pending
- 🔄 Debugging tools integration pending
- 🔄 Secure API key management (hardcoded fallback present)
- 🔄 Drawing board in chat box for rough work and calculations pending