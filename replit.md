# MooMoo.io Clone

## Overview
This is a fully working MooMoo.io private server implementation, imported from GitHub and configured to run on Replit. The project consists of:
- A webpack-powered client (frontend) with game assets and UI
- An Express + WebSocket server (backend) handling game logic and multiplayer functionality
- npm workspaces for monorepo management

## Project Structure
- `client/` - Frontend source code and static assets
- `server/` - Game server source using ES modules
- `shared/` - Shared configuration between client and server
- `dist/` - Build artifacts (auto-generated, ignored by git)

## Setup Configuration
- **Port**: 5000 (Replit requirement for frontend)
- **Host**: 0.0.0.0 (allows Replit proxy access)
- **Cache Control**: Disabled to prevent stale content in iframe
- **Build System**: Webpack for client bundling

## Commands
- `npm run build` - Build production client bundle
- `npm run build:dev` - Build client in development mode with watch
- `npm start` - Start the game server
- `npm run dev` - Start server in development mode

## Recent Changes (November 26, 2025)
- Configured server to run on port 5000 for Replit compatibility
- Added cache-control headers to prevent browser caching issues
- Set up workflow for automatic server startup
- Built initial client bundle
- Configured deployment with build and run commands
- Verified game loads and displays correctly

## Architecture
- The server serves both the static client files and WebSocket API
- Client connects via WebSocket for real-time multiplayer gameplay
- Express handles HTTP routes, WebSocket handles game communication
- MsgPack used for efficient binary message encoding

## Disclaimer
This is a non-commercial, educational fan project and clone of MooMoo.io intended solely for learning purposes.
