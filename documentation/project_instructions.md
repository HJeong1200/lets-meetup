# Agent Guidelines & Project Standards

> [!IMPORTANT]
> This document outlines the **Workflow** and **Standards** required when working on this repository. As an agent, you must adhere to these rules strictly.

## 1. Operating Procedure: Design First
*   **Do Not Code Prematurely**: When a new feature or significant change is requested, you **MUST** first locate or create the relevant Design Specification in `documentation/`.
*   **Update Docs First**: If requirements change, update the corresponding markdown file in `documentation/` (e.g., `design_auth.md`, `design_new_meeting.md`) **BEFORE** modifying any code or database schema.
*   **User Validation**: Ask for user confirmation on the design spec updates before proceeding to implementation.

## 2. Technical Architecture Standards
*   **Repository Structure**: Maintain a strict Monorepo structure. Frontend (Next.js) and Backend logic (Server Actions/API Routes) reside together.
*   **Styling**: Use **Tailwind CSS** with **Shadcn UI** components. Avoid custom CSS files (`index.css` is for global directives only).
*   **State Management**: Use React Query (TanStack Query) for server state. Avoid complex client-side state managers (Redux/Zustand) unless absolutely necessary.
*   **Database**: All schema changes must be versioned in `supabase/migrations`. Do not make manual changes to the database without a migration file.

## 3. Implementation Rules
*   **MVP Approach**: Always question if a feature (e.g., Social Login, Complex Settings) is necessary for the MVP. Default to the simplest implementation unless instructed otherwise.
*   **Type Safety**: All code must be strictly typed (TypeScript). No `any`.
*   **Components**: Create small, reusable components in `src/components`.

## 4. Documentation Directory Structure
*   `documentation/design_spec.md`: High-level overview.
*   `documentation/design_*.md`: Specific domain logic. **Read these for business rules.**
