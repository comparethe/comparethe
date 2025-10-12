Collaborative editors for creating and previewing live HTML pages or websites — ideally browser-based, real-time, multi-file, and free.

In a perfect world this would be "paste-and-go": I just paste, get a url, share it and we're live editing.

One use case, we have for this more and more when is when using AI. We can prompt to, say, a pretty decent landing page in HTML and TailwindCSS but we'll want to refine it a little collaboratively outside of the AI. For that, it's much more convenient to be working in a proper collaborative real-time environment.

<img width="2571" height="1738" alt="image" src="https://github.com/user-attachments/assets/acc08061-fe8e-4d9a-9d97-e78622703796" />

## What we're looking for

We’re looking for **real-time collaborative code editors** specifically for **web development (HTML + Tailwind)** that meet the following criteria:

1. **Real-time collaboration** — multiple users can edit simultaneously with shared cursors and minimal lag.
2. **Live website preview** — automatic or easy-to-refresh preview of the rendered HTML/CSS/JS output.
3. **Minimal setup** — either runs entirely in the browser or requires very little installation/configuration.
4. **Supports multi-file projects** — not just single snippets; ideally allows full site structures.
5. **Free to use** — either fully free or with a usable free tier suitable for small projects.

## Recommendations

### Desktop Applications

For these, installation is required.

| Tool                                | Platform                | Collaboration                                            | Live Preview                           | Scope          | Pros                                                | Cons / Friction Points                                 |
| ----------------------------------- | ----------------------- | -------------------------------------------------------- | -------------------------------------- | -------------- | --------------------------------------------------- | ------------------------------------------------------ |
| **[Visual Studio Code](https://code.visualstudio.com/) + Live Share** | Desktop IDE             | ✅ Full multi-cursor editing, shared terminal & localhost | ✅ Via Live Server or similar extension | Multiple files | Mature, powerful, Tailwind support, broad ecosystem | Requires install and Live Share setup for both users   |
| **[Zed](https://zed.dev/)**                             | Desktop IDE (Mac/Linux) | ✅ Built-in, low-latency collaboration                    | ✅ Local web preview                    | Multiple files | Lightweight, fast, intuitive sharing                | Preview setup less automated; smaller plugin ecosystem |

NB: when we say VS Code you can also include all visual studio derived apps e.g. Cursor etc.

### Online Editors (Browser-Based)

| Tool                     | Platform                     | Collaboration                          | Live Preview                    | Scope          | Free Tier               | Pros                                                  | Cons / Friction Points                                   |
| ------------------------ | ---------------------------- | -------------------------------------- | ------------------------------- | -------------- | ----------------------- | ----------------------------------------------------- | -------------------------------------------------------- |
| **GitHub Codespaces**    | Browser (VS Code-in-browser) | ✅ Via [VS Code Live Share ]([url](https://docs.github.com/en/codespaces/developing-in-a-codespace/working-collaboratively-in-a-codespace))              | ✅ Full web server preview       | Multiple files | ✅ (limited hours/month) | Real VS Code in browser; integrates with GitHub repos | Requires GitHub setup; slower startup                    |
| **CodeSandbox** | Browser IDE | ✅ Real-time collaboration      | ✅ Live preview      | Multiple files | ✅ (limited resources)           | Excellent for frontend projects; slightly heavier |

### Secondary Options (Online)

Would comment that as of Oct 2025 Replit and StackBlitz have become all-AI-y and it is actually quite painful to use as pure html editors (hence relegated here). similar thing seems to be happening with CodeSandbox (they have merged with together.ai) though with CodeSandBox it is still easy.

| Tool            | Platform    | Collaboration                  | Live Preview        | Scope          | Free Tier                       | Comments                                          |
| --------------- | ----------- | ------------------------------ | ------------------- | -------------- | ------------------------------- | ------------------------------------------------- |
| **Glitch**      | Browser IDE | ✅ Real-time co-editing         | ✅ Auto live preview | Multiple files | ✅ (projects sleep on free tier) | Friendly interface, but can be slow or unstable   |
| **[Replit](https://replit.com/) (Multiplayer)** | Browser IDE                  | ✅ Native multiplayer                   | ✅ Auto preview for web projects | Multiple files | ✅ (free tier available) | Instant sharing, built-in hosting                     | Multiplayer sometimes buggy; login required              |
| **[Bolt.new (StackBlitz)](https://bolt.new/)**           | Browser IDE                  | ✅ Collaborative editing (invite-based) | ✅ Instant live reload           | Multiple files | ✅ (free tier)           | Very fast, ideal for frontend frameworks, no install  | Collaboration less polished; occasional account friction |
