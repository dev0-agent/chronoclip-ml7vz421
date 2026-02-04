# Task List

This file shows the current progress of all tasks in this project.
It is automatically updated by dev0 as tasks are completed.

---

## Phase 1

- [ ] ⏳ **Environment & Drizzle Setup**
  Create an `env.ts` file to validate environment variables (DATABASE_URL). Initialize Drizzle ORM with a basic configuration file (`drizzle.config.ts`) and a database connection client. Ensure the database connection works.

- [ ] ⏳ **Define Database Schema**
  Create the Drizzle schema definitions. We need tables for: `videos` (id, youtubeId, title, url, createdAt), `clips` (id, videoId, timestampSeconds, note, createdAt), and `tags` (id, name). Include a many-to-many relation for video/clip tags if possible, or keep it simple with a `tags` table linked to clips. Run the migration generation.

- [ ] ⏳ **App Shell & Navigation**
  Create the main layout using shadcn/ui components. Include a Sidebar for navigation (Library, Tags) and a Header. Set up the root layout file. Remove default Next.js boilerplate styles.

## Phase 2

- [ ] ⏳ **Video Ingestion Feature**
  Create a server action to add a video. It should accept a YouTube URL, extract the Video ID using regex, and save it to the `videos` table. Create a simple UI dialog or form to input the URL and trigger this action.

- [ ] ⏳ **Video Player Component**
  Implement a VideoPlayer component using the YouTube IFrame API (or `react-youtube`). It must accept a `videoId` and expose a method or prop to seek to a specific timestamp programmatically. Ensure it handles the 'onReady' state correctly.

- [ ] ⏳ **Clip Creation Logic**
  Create the UI and Server Action to save a 'Clip'. The UI needs a button 'Capture Timestamp' which reads the current player time, and a text area for a note. The Server Action saves this to the `clips` table linked to the current video.

- [ ] ⏳ **Video Detail View & Clip Playback**
  Build the dynamic page `/video/[id]`. It should display the Player (Task 5) on one side and a scrollable list of Clips (fetched from DB) on the other. Clicking a Clip card should trigger the Player to seek to that clip's timestamp.

## Phase 3

- [ ] ⏳ **Library Dashboard**
  Create the main dashboard page (`/`). Display a grid of saved videos using shadcn Cards. Show the video thumbnail (fetched from YouTube standard URL structure) and title.

- [ ] ⏳ **Tagging System Implementation**
  Implement the UI to add tags to a Clip. Update the schema if needed to support tags. Create a Server Action to associate tags with clips. Display tags as badges on the Clip cards.

## Phase 4

- [ ] ⏳ **Clip Management (Edit/Delete)**
  Add functionality to delete a clip or edit its note. Add a delete button to the Video card in the library to remove the video and all associated clips.

- [ ] ⏳ **UI Polish & Empty States**
  Add loading skeletons for the video player and clip list. Add nice empty states for the Library (when no videos exist) and the Clip list (when no clips exist). Ensure responsive design for mobile (stack player above clips).

---

_Last updated by dev0 automation_
