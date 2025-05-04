# Contributing to CompetA-arena 🇷🇼

Thank you for considering contributing to CompetA! This document will help you get started with the project setup and contribution guidelines.

---

## 🛠 Tech Stack
- **Backend**: Node.js + Express, TypeORM, PostgreSQL, TypeScript
- **Frontend**: React + TypeScript, Tailwind CSS
- **Tools**: Git, npm, PostgreSQL

---

## 🚀 Getting Started

### Prerequisites
- Node.js ≥ v18.x
- npm ≥ v9.x
- PostgreSQL ≥ v14
- Git

### Installation

1. **Fork the Repository**
   ```bash
   git clone https://github.com/jeid12/competA-arena.git
   cd competA-arena
   ```
2. **Install Dependencies**
   ```bash
    # Backend setup
    cd backend
    npm install
    
    # Frontend setup
    cd ../frontend
    npm install
   ```
 

3.**Database Setup**

    ```bash
       # Create PostgreSQL database
      createdb competa_db
  
     # Configure environment variables (backend/.env)
     cp backend/.env.example backend/.env

4. **Run Migrations**

   ```
   cd backend
   npm run typeorm:run

5. **Start Servers**
   ```
    # Backend (from /backend)
    npm run dev
    
    # Frontend (from /frontend)
    npm run dev
6. **📂 Project Structure**
   ```
    competA/
    ├── backend/
    │   ├── src/
    │   │   ├── controllers/   # Route controllers
    │   │   ├── entities/      # TypeORM entities
    │   │   ├── routes/        # Express routes
    │   │   └── utils/         # Helper functions
    │   ├── .env               # Environment variables
    │   └── package.json
    │
    └── frontend/
        ├── src/
        │   ├── components/    # Reusable components
        │   ├── pages/         # Page components
        │   ├── types/         # TypeScript types
        │   └── App.tsx
        ├── tailwind.config.js
        └── package.json

 7. **📜 Coding Standards**
     
      Backend (Node/TypeScript)
      Use TypeORM decorators for entity definitions
      
      Follow RESTful API conventions
      
      Validate inputs using class-validator
      
      Use DTOs for data transfer objects
      
      Write unit tests with Jest (coming soon)
      
      Frontend (React/TypeScript)
      Functional components with TypeScript
      
      Use Tailwind utility classes for styling
      
      Follow atomic design principles
      
      Type all props and API responses
      
      Use axios for API calls

***General***
 ```
  # Both backend and frontend
    npm run lint
```
Commit Messages

Use Conventional Commits

Format: <type>(scope): description

Example: feat(auth): add login endpoint

Documentation

Update README.md for major changes

Use JSDoc for complex functions

Keep TypeScript interfaces self-documenting

🤝 Contribution Workflow
Create a Branch

bash
git checkout -b feat/your-feature-name
# or
git checkout -b fix/your-bug-fix
Make Changes

Keep commits atomic

Test locally before pushing

Create Pull Request

Target main branch

Include screenshots for UI changes

Describe changes clearly

PR Checklist
Tests pass (if applicable)

Linter passes

Documentation updated

No console.log statements

Follows project structure

🐛 Reporting Issues
Use our issue template and include:

Expected vs actual behavior

Steps to reproduce

Environment details

Screenshots (if UI-related)

📄 License
By contributing, you agree that your contributions will be licensed under the project's MIT License.

🙏 Acknowledgments
First-time contributors are especially welcome!

Please add yourself to the contributors list after your first PR is merged.







   
