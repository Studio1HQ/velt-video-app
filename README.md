<div align="center">

<img src="https://raw.githubusercontent.com/Studio1HQ/Studio1HQ/main/assets/banners/velt-video-app.webp" alt="Frame.io-Style Video Comments with Velt: Timeline comments on a video player, plus an inventory demo" width="100%" />

<br />
<br />

# Frame.io-Style Video Comments with Velt

### Timeline comments on a video player, plus an inventory demo

A Next.js app that adds Velt comments to a video player with a comment timeline and sidebar. The README also describes an inventory management UI (StockSync) with commenting.

<br />

[![Built by Studio1](https://img.shields.io/badge/Built_by_Studio1-f97316?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNjAgMTYwIiBmaWxsPSJub25lIj48cGF0aCBmaWxsLXJ1bGU9ImV2ZW5vZGQiIGNsaXAtcnVsZT0iZXZlbm9kZCIgZD0iTTAgMzVDMCAxNi42ODA3IDE0LjA3NDQgMS42NDg0NCAzMiAwLjEyNjk1M1YxNDFINTEuMDUyM0M1Mi40MzA4IDEzNy4zNDQgNTQuNzQ0NiAxMzMuNjg5IDU3Ljk5MzggMTMwLjAzM0M2MS4xNDQ2IDEyNi41MDggNjQuNjg5MiAxMjMuNDQgNjguNjI3NyAxMjAuODI5QzcyLjU2NjIgMTE4LjM0OSA3Ni4zNTY5IDExNi43ODIgODAgMTE2LjEyOVY4Ni43NTQ0Qzc1LjQ3MDggODcuOTI5MiA3MS4zODQ2IDg5LjY5MTkgNjcuNzQxNSA5Mi4wNDE1QzY0IDk0LjUyMjUgNjAuNzUwOCA5Ny40NiA1Ny45OTM4IDEwMC44NTRDNTYuNTM0NSAxMDIuNzIgNTUuMjU0NSAxMDQuNjU5IDU0LjE1MzkgMTA2LjY3MVYwSDEyNUMxNDQuMzMgMCAxNjAgMTUuNjY5OSAxNjAgMzVWMTI1QzE2MCAxNDQuMzMgMTQ0LjMzIDE2MCAxMjUgMTYwSDEyNFYxOEgxMDQuOTQ4QzEwMy41NjkgMjEuNjgxNiAxMDEuMjU1IDI1LjM2MjggOTguMDA2MiAyOS4wNDQ0Qzk0Ljg1NTQgMzIuNTk0MiA5MS4zMTA4IDM1LjY4NDEgODcuMzcyMyAzOC4zMTRDODMuNDMzOCA0MC44MTIgNzkuNjQzMSA0Mi4zODk2IDc2IDQzLjA0NzRWNzIuNjMwNEM4MC41MjkyIDcxLjQ0NzMgODQuNjE1NCA2OS42NzI0IDg4LjI1ODUgNjcuMzA1N0M5MiA2NC44MDc2IDk1LjI0OTIgNjEuODQ5MSA5OC4wMDYyIDU4LjQzMDdDOTkuNDY1NSA1Ni41NTEzIDEwMC43NDUgNTQuNTk4NiAxMDEuODQ2IDUyLjU3MjNWMTYwSDM1QzE1LjY3IDE2MCAwIDE0NC4zMyAwIDEyNVYzNVoiIGZpbGw9IiNmZmZmZmYiLz48L3N2Zz4K)](https://studio1hq.com)
[![Built with Velt](https://img.shields.io/badge/Built_with_Velt-141414?style=for-the-badge)](https://velt.dev)

[Velt docs](https://docs.velt.dev) &nbsp;·&nbsp; [Velt](https://velt.dev) &nbsp;·&nbsp; [More examples](https://github.com/Studio1HQ) &nbsp;·&nbsp; [studio1hq.com](https://studio1hq.com)

</div>

<br />

## Overview

A Next.js app that adds frame-accurate style comments to a video using [Velt](https://velt.dev). Turn on comment mode, pause the video, click on the frame to leave a comment, and the comment appears as a marker on the player timeline. Clicking a marker or a sidebar entry seeks the video to that moment.

The page title in the code is "Frame.io style video demo with Velt SDK". The repo also contains inventory-related types, utilities and a README written for a related inventory demo, described under How it works.

<video width="100%" controls>
  <source src="https://github.com/user-attachments/assets/f1afb18e-0893-4e82-97d8-31af2366c7af" type="video/mp4">
Your browser does not support the video tag.
</video>

## Features

- **Video comments**: Comment mode lets you pin comments on the video player with `VeltComments`.
- **Timeline markers**: `VeltCommentPlayerTimeline` shows where comments sit on the playback bar.
- **Seek on click**: Clicking a timeline comment moves the video to that comment's media position.
- **Comments sidebar**: `VeltCommentsSidebar` and `VeltSidebarButton` list and filter threads.
- **Presence**: `VeltPresence` shows who else is viewing.
- **Custom player controls**: Play and pause state and a progress bar driven by the HTMLVideoElement events.

## Tech stack

| Layer | Tool |
| --- | --- |
| Framework | [Next.js](https://nextjs.org) 15, React 19, [TypeScript](https://www.typescriptlang.org) |
| Collaboration | [Velt](https://velt.dev) (`@veltdev/react`) |
| Video | [next-video](https://next-video.dev) |
| Styling | [Tailwind CSS](https://tailwindcss.com) 4, [Lucide](https://lucide.dev) |

## Getting started

### Prerequisites

- Node.js 18 or later
- npm or yarn
- A Velt account and API key from [velt.dev](https://velt.dev)

### Installation

```bash
git clone https://github.com/Studio1HQ/velt-video-app.git
cd velt-video-app
npm install
```

### Environment variables

Create `.env.local` in the project root.

| Variable | Description |
| --- | --- |
| `NEXT_PUBLIC_VELT_API_KEY` | Your Velt API key. `src/app/page.tsx` throws an error if it is missing. |

### Run

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

## How it works

```text
src/
  app/page.tsx                    VeltProvider, VeltComments, VeltPresence, VideoComponent
  components/AuthComponent.tsx    useIdentify with a Velt user
  components/VeltDocument.tsx     useSetDocumentId("my-document-id") and VeltCommentTool
  components/VideoComponent.tsx   Player, timeline, sidebar, comment mode handling
  utils/randomUser.ts             Random demo user
  types/inventory.ts, utils/inventory.ts   Inventory helpers, not used by the page
```

- `AuthComponent` identifies a demo user with `useIdentify`. It must be a child of `VeltProvider`.
- `VideoComponent` uses `useCommentModeState` to pause the video when comment mode starts, and handles timeline comment clicks to seek to the comment's media position.
- The previous README described an inventory system (StockSync) with Velt comments on inventory items. Only its type and utility files remain here; the running app is the video commenter.

## Resources

- [Velt documentation](https://docs.velt.dev): SDK reference.
- [Velt](https://velt.dev): Product site.
- [next-video](https://next-video.dev): Video component used for playback.

<br />

---

<div align="center">

<a href="https://studio1hq.com">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Studio1HQ/website/main/brand/studio1-logo-on-dark.svg" />
    <img src="https://raw.githubusercontent.com/Studio1HQ/website/main/brand/studio1-logo-on-light.svg" alt="Studio1" width="160" />
  </picture>
</a>

Built by **[Studio1](https://studio1hq.com)**, the technical content and DevRel partner for devtool teams. Made with [Velt](https://velt.dev).<br />
Browse more open-source examples at [github.com/Studio1HQ](https://github.com/Studio1HQ).

[![Website](https://img.shields.io/badge/studio1hq.com-0b0807?style=for-the-badge&logo=googlechrome&logoColor=white)](https://studio1hq.com)
[![Book a call](https://img.shields.io/badge/Book_a_strategy_call-f97316?style=for-the-badge&logo=googlecalendar&logoColor=white)](https://cal.com/studio1/collab)
[![X](https://img.shields.io/badge/%40Studio1HQ-141414?style=for-the-badge&logo=x&logoColor=white)](https://x.com/Studio1HQ)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0a66c2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/company/studio1hq/)

<sub><a href="https://studio1hq.com">studio1hq.com</a> · Technical content, docs, video and DevRel for devtools</sub>

</div>
