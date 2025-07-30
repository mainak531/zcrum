# 🏁 SprintBoard – Agile Sprint & Issue Management Tool

**SprintBoard** is a modern agile project management system with organization-based access control, sprint planning, drag-and-drop issue boards, and markdown support.

Built using **Next.js 14**, **Prisma ORM**, **PostgreSQL**, and **Clerk Authentication**, this project mimics the sprint lifecycle workflow used in real-world agile teams.

---

## 🔥 Features
## 📌 Key Features

- ✅ **Clerk Auth Integration**: Secure login/signup, user sessions, and organization support
- 🏢 **Organization Management**: View and switch orgs, invite users, enforce org-level roles (`org:admin`)
- 📁 **Project Control**: Create/delete projects per org; accessible only by authorized members
- 📦 **Sprint Planning**: Create sprints with start/end dates, manage status (`PLANNED`, `ACTIVE`, `COMPLETED`)
- 🧵 **Issue Management**: Assign issues to users, set priority/status, and order by status & drag-drop support
- 🔐 **Role-Based Access Control**: Only org admins can manage projects/sprints
- 📚 **Modular App Router Structure**: Clear separation of server actions, client components, and page routes

### 🔐 Organization & Authentication
- Role-based access via **Clerk** (`org:admin`, `org:member`)
- Project creation restricted to admins only
- Multi-organization support via Clerk's org switching

### 🚀 Project & Sprint Management
- Create/delete projects under specific organizations
- Auto-generated sprint naming (e.g., `PROJ-1`)
- Sprint lifecycle:
  - **Planned** – upcoming
  - **Active** – current sprint
  - **Completed** – archived
- Date validation to prevent invalid sprint start/end

### ✅ Issue Tracking System
- Create issues with:
  - Title, Markdown description
  - Assignee selection (from org members)
  - Priority (LOW → URGENT)
  - Status column: `TODO`, `IN PROGRESS`, `DONE`
- Drag-and-drop reordering within and across status columns
- Live updates using optimistic UI + toast notifications

---

## 📦 Tech Stack

| Category      | Stack                                                   |
|---------------|----------------------------------------------------------|
| Frontend      | Next.js App Router, React 19, Tailwind CSS, ShadCN       |
| Auth & RBAC   | Clerk (users + organizations + roles)                    |
| Database      | PostgreSQL (via Prisma ORM)                              |
| UI Libraries  | Sonner (toast), Lucide Icons, @hello-pangea/dnd, MDEditor|
| State & Hooks | Custom `useFetch` hook, React Hook Form, Zod Validation  |
---
## 🧩 UI Components (Accessible + Headless + Themed)

> Built on Radix Primitives + Tailwind + ShadCN Design System

| Component    | Description |
|--------------|-------------|
| `Button`, `Avatar`, `Badge` | Base components with CVA variants |
| `Input`, `Textarea`         | Fully accessible form fields, aria-compliant |
| `Select`, `Popover`, `Tabs` | Built with Radix UI, keyboard-navigable |
| `Card`, `Dialog`, `Drawer`  | Layouts with animated transitions |
| `Toast` (`Sonner`)          | System-themed notifications |
| `Carousel`                  | Powered by Embla Carousel, mobile-ready |
| `Toaster`                   | Dark/light mode aware, dynamic styles via `next-themes` |

All components:
- 🌙 Support dark/light mode
- ♿ Fully accessible (Radix + WAI-ARIA)
- 🧠 Themed using Tailwind CSS tokens
- ⚡ Composable via `@/lib/utils` and `class-variance-authority`


---

## 📸 Screenshots

> [Optional – Add images/GIFs showcasing sprint creation, issue drawer, and board]

---

## ⚙️ Getting Started

```bash
git clone https://github.com/yourgithub/sprintboard
cd sprintboard
npm install
npx prisma generate
npx prisma db push
npm run dev
This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.js`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
