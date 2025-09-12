# Next.js Chatbot with Gemini AI

A modern chatbot application built with Next.js that integrates Google's Gemini AI for intelligent conversations. This application features Google authentication and local storage for chat history.

## Features

*   **AI-Powered Conversations**: Leverages Google's Gemini API for natural language processing, enabling intelligent and dynamic interactions.
*   **Google Authentication**: Secure user login and session management powered by Google OAuth.
*   **Local Storage**: Chat history persists locally in the browser, providing a seamless user experience across sessions.
*   **Responsive Design**: Optimized to work flawlessly across various devices, from desktops to mobile phones.
*   **Real-time Chat Interface**: Provides a smooth, interactive, and engaging messaging experience.

## Project Purpose

This project aims to provide a robust and user-friendly chatbot application leveraging the power of Google's Gemini AI. It serves as a practical example of integrating advanced AI capabilities with modern web development practices, offering a seamless conversational experience with secure authentication and persistent chat history.

## Tech Stack

*   **Framework**: Next.js 14+ with App Router
*   **Authentication**: NextAuth.js with Google Provider
*   **AI Integration**: Google Gemini API
*   **Styling**: Tailwind CSS
*   **Storage**: Browser Local Storage
*   **Language**: TypeScript

## Prerequisites

Before running this application, ensure you have the following installed:

*   Node.js 18+
*   A Google Cloud Project with the Gemini API enabled
*   Google OAuth credentials configured

## Environment Variables

Create a `.env.local` file in the root directory of your project and add the following environment variables:

```env
# Google OAuth
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret

# NextAuth
NEXTAUTH_URL=http://localhost:3000
NEXTAUTH_SECRET=your_nextauth_secret

# Gemini API
GEMINI_API_KEY=your_gemini_api_key
```

## Installation

Follow these steps to set up and run the application locally:

1.  **Clone the repository**:
    ```bash
    git clone <repository-url>
    cd nextjs-gemini-chatbot
    ```
2.  **Install dependencies**:
    ```bash
    npm install
    # or
    yarn install
    # or
    pnpm install
    ```
3.  **Set up environment variables**: Refer to the "Environment Variables" section above.
4.  **Run the development server**:
    ```bash
    npm run dev
    # or
    yarn dev
    # or
    pnpm dev
    ```
5.  Open [http://localhost:3000](http://localhost:3000) in your browser to view the application.

## Quick Start

To get started quickly, follow these steps:

1.  **Clone the repository**: `git clone <repository-url>`
2.  **Install dependencies**: `npm install` (or `yarn install`, `pnpm install`)
3.  **Configure environment variables**: Create a `.env.local` file and add your `GOOGLE_CLIENT_ID`, `GOOGLE_CLIENT_SECRET`, `NEXTAUTH_SECRET`, and `GEMINI_API_KEY`.
4.  **Run the development server**: `npm run dev` (or `yarn dev`, `pnpm dev`)
5.  Open your browser to `http://localhost:3000`.

## Configuration

### Google Cloud Setup

1.  Go to the [Google Cloud Console](https://console.cloud.google.com/).
2.  Create a new project or select an existing one.
3.  Enable the Gemini API for your project.
4.  Create credentials for OAuth 2.0 Client IDs.

### OAuth Configuration

Add the following to your Google OAuth settings in the Google Cloud Console:

*   **Authorized JavaScript origins**: `http://localhost:3000`
*   **Authorized redirect URIs**: `http://localhost:3000/api/auth/callback/google`

## Usage

*   **Authentication**: Users must sign in with their Google account to access the chatbot.
*   **Start Chatting**: Begin conversations with the AI chatbot immediately after authentication.
*   **Persistent History**: Chat history is automatically saved to local storage, ensuring continuity.
*   **Session Management**: Conversations persist across browser sessions, enhancing user experience.

## API Routes

*   `/api/auth/*`: NextAuth.js authentication endpoints for handling user login and sessions.
*   `/api/chat`: Gemini API integration endpoint for processing and responding to chat messages.

## Project Structure

```
├── app/
│   ├── api/                  # API routes for authentication, chat, and other services
│   │   ├── auth/             # NextAuth.js authentication endpoints
│   │   └── chat/             # Gemini API integration endpoint
│   ├── components/           # Reusable UI components
│   ├── page.tsx              # Main application page
│   └── layout.tsx            # Root layout for the application
├── lib/                      # Utility functions and configurations
│   ├── prisma.ts             # Prisma client for database interactions
│   └── ...                   # Other utility files (e.g., auth, gemini, utils)
├── prisma/                   # Prisma schema and migrations
├── public/                   # Static assets
├── types/                    # TypeScript custom type definitions
├── .env.local                # Environment variables (not committed)
├── next.config.ts            # Next.js configuration
├── package.json              # Project dependencies and scripts
├── tsconfig.json             # TypeScript configuration
└── README.md                 # Project documentation
```

## Features in Detail

### Chat Functionality

*   Real-time message exchange with Gemini AI.
*   Message history stored locally for easy retrieval.
*   Typing indicators and loading states for a dynamic user interface.
*   Robust error handling for API failures to ensure a smooth experience.

### Authentication

*   Secure Google OAuth integration for reliable user authentication.
*   Comprehensive user session management.
*   Protected routes and API endpoints to ensure data security.

### Local Storage

*   Automatic chat history persistence for uninterrupted conversations.
*   Cross-session conversation continuity.
*   User-specific data storage to maintain personalized experiences.

## Deployment

### Vercel (Recommended)

1.  Push your code to a GitHub repository.
2.  Connect your repository to Vercel.
3.  Add environment variables in the Vercel dashboard.
4.  Deploy automatically.

### Other Platforms

Configure environment variables and build commands according to your chosen platform's requirements.

## Contributing

We welcome contributions to this project! Please follow these steps:

1.  Fork the repository.
2.  Create a new feature branch (`git checkout -b feature/YourFeature`).
3.  Make your changes and commit them (`git commit -m 'Add YourFeature'`).
4.  Push to the branch (`git push origin feature/YourFeature`).
5.  Submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

For issues and questions, please refer to the following:

*   Create an issue in the [GitHub repository](https://github.com/your-username/nextjs-gemini-chatbot/issues).
*   Check the documentation for common solutions.

## Acknowledgments

*   **Google Gemini AI**: For providing powerful language processing capabilities.
*   **Next.js Team**: For the excellent framework that powers this application.
*   **NextAuth.js**: For simplifying authentication solutions.

## Future Enhancements

*   **Multi-model Support**: Integrate with other AI models beyond Gemini.
*   **User Profiles**: Allow users to manage their profiles and preferences.
*   **Advanced Chat Features**: Implement features like file uploads, voice input, and message editing.
*   **Database Integration**: Store chat history in a database for more robust persistence and analytics.
*   **Deployment Automation**: Enhance CI/CD pipelines for smoother deployments.