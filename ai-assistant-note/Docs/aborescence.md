## Project Directory Structure 

    This project is a note-taking application integrated with ChatGPT, allowing users to create simple notes or complex projects composed of multiple notes. The app also features a calendar to view notes by date and a review section for the latest notes. The tech stack includes React, Next.js, TypeScript, Prisma, PostgreSQL, Tailwind CSS, shadcnUI, and AI ChatGPT & Whisper.

## Directory Structure
```
  src/
    ├── app/
    │   ├── api/
    │   │   ├── chatgpt/
    │   │   │   └── route.ts
    │   │   ├── notes/
    │   │   │   └── route.ts
    │   │   ├── projects/
    │   │   │   └── route.ts
    │   │   ├── whisper/      
    │   │   │   └── route.ts  
    │   │   └── route.ts
    │   ├── calendar/
    │   │   └── page.tsx
    │   ├── notes/
    │   │   ├── create/
    │   │   │   └── page.tsx
    │   │   ├── [id]/
    │   │   │   └── page.tsx
    │   │   └── page.tsx
    │   ├── projects/
    │   │   ├── create/
    │   │   │   └── page.tsx
    │   │   ├── [id]/
    │   │   │   ├── notes/
    │   │   │   │   └── create/
    │   │   │   │       └── page.tsx
    │   │   │   └── page.tsx
    │   │   └── page.tsx
    │   ├── dashboard/
    │   │   └── page.tsx
    │   ├── layout.tsx
    │   └── page.tsx
    ├── components/
    │   ├── Calendar/
    │   │   ├── Calendar.tsx
    │   │   ├── CalendarEvent.tsx
    │   │   └── index.ts
    │   ├── ChatGPT/
    │   │   ├── ChatGPTComponent.tsx
    │   │   └── index.ts
    │   ├── Whisper/       
    │   │   ├── WhisperComponent.tsx   
    │   │   └── index.ts
    │   ├── Note/
    │   │   ├── NoteForm.tsx
    │   │   ├── NoteItem.tsx
    │   │   └── index.ts
    │   ├── Project/
    │   │   ├── ProjectForm.tsx
    │   │   ├── ProjectItem.tsx
    │   │   └── index.ts
    │   ├── Layout/
    │   │   ├── Footer.tsx
    │   │   ├── Header.tsx
    │   │   └── index.ts
    │   └── UI/
    │       ├── Button.tsx
    │       ├── Modal.tsx
    │       └── index.ts
    ├── prisma/
    │   ├── schema.prisma
    │   └── client.ts
    ├── services/
    │   ├── chatgpt.ts
    │   ├── notes.ts
    │   ├── projects.ts
    │   ├── whisper.ts     
    │   └── index.ts
    ├── styles/
    │   ├── globals.css
    │   ├── tailwind.css
    │   └── shadcn.css
    ├── types/
    │   ├── chatgpt.ts
    │   ├── note.ts
    │   ├── project.ts
    │   └── index.ts
    ├── utils/
    │   ├── api.ts
    │   ├── constants.ts
    │   ├── helpers.ts
    │   └── index.ts
    └── hooks/
        ├── useFetch.ts
        ├── useChatGPT.ts
        ├── useNotes.ts
        ├── useProjects.ts
        └── index.ts
```

## Description of Directory Structure:

src/:

    app/:

        api/: This directory contains API routes for different functionalities of the application.
            chatgpt/route.ts: API route for integrating ChatGPT functionality.
            notes/route.ts: API route for handling note-related operations.
            projects/route.ts: API route for managing projects.
            whisper/route.ts: API route for integrating Whisper functionality.
            route.ts: Main API route handler.

        calendar/: This directory contains pages and components related to the calendar feature.
            page.tsx: Calendar page for viewing and interacting with events.

        notes/: This directory contains pages and components related to note management.
            create/page.tsx: Page for creating a new note.
            [id]/page.tsx: Dynamic page for viewing a specific note identified by its ID.

        projects/: This directory contains pages and components related to project management.
            create/page.tsx: Page for creating a new project.
            [id]/page.tsx: Dynamic page for viewing a specific project and its associated notes.
                notes/create/page.tsx: Page for creating a new note within a specific project.

        dashboard/: This directory contains pages and components related to the dashboard feature.
            page.tsx: Dashboard page of the application.

        layout.tsx: Main layout component defining the structure of the application.

        page.tsx: Homepage of the application.

    components/:

        Calendar/: Components related to the calendar feature.
            Calendar.tsx: Main calendar component.
            CalendarEvent.tsx: Component for rendering individual calendar events.

        ChatGPT/: Components for integrating ChatGPT functionality.
            ChatGPTComponent.tsx: Main component for interacting with ChatGPT.

        Whisper/: Components for integrating Whisper functionality.
            WhisperComponent.tsx: Main component for interacting with Whisper.

        Note/: Components related to note management.
            NoteForm.tsx: Form component for creating and editing notes.
            NoteItem.tsx: Component for displaying an individual note.

        Project/: Components related to project management.
            ProjectForm.tsx: Form component for creating and editing projects.
            ProjectItem.tsx: Component for displaying an individual project.

        Layout/: Components defining the global layout of the application.
            Footer.tsx: Footer component.
            Header.tsx: Header component.

        UI/: Reusable UI components.
            Button.tsx: Component for rendering buttons.
            Modal.tsx: Component for displaying modal dialogs.

    prisma/:
        schema.prisma: Prisma database schema definition.
        client.ts: Configuration file for the Prisma client.

    services/:
        chatgpt.ts: Service module for interacting with the ChatGPT API.
        notes.ts: Service module for handling note-related operations.
        projects.ts: Service module for managing projects.
        whisper.ts: Service module for interacting with the Whisper API.
        index.ts: Entry point for service modules.

    styles/:
        globals.css: Global CSS styles applicable throughout the application.
        tailwind.css: Configuration file for TailwindCSS.
        shadcn.css: Custom styles specific to the ShadcnUI framework.

    types/:
        chatgpt.ts: TypeScript types/interfaces related to ChatGPT integration.
        note.ts: TypeScript types/interfaces related to notes.
        project.ts: TypeScript types/interfaces related to projects.
        index.ts: Entry point for type definitions.

    utils/:
        api.ts: Utility functions for configuring and making API calls.
        constants.ts: Constants used throughout the application.
        helpers.ts: Helper functions for common tasks.
        index.ts: Entry point for utility functions.

    hooks/:
        useFetch.ts: Custom React hook for handling data fetching logic.
        useChatGPT.ts: Custom React hook for interacting with ChatGPT functionality.
        useWhisper.ts: Custom React hook for interacting with Whisper functionality.
        useNotes.ts: Custom React hook for managing note-related state and logic.
        useProjects.ts: Custom React hook for managing project-related state and logic.
        index.ts: Entry point for custom hooks.






