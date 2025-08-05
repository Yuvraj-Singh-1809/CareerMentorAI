# CareerMentorAI

CareerMentorAI is an AI-powered web platform that streamlines professional growth by providing personalized guidance, intelligent resume and cover letter builders, interview preparation, and actionable industry insights—all in one integrated application.

---

## 🚀 Features

- **AI Career Guidance:** Delivers tailored career advice and actionable growth recommendations using advanced AI.
- **Resume Builder:** Effortlessly craft ATS-friendly resumes with customizable forms, markdown support, and PDF download.
- **Cover Letter Generator:** Produce personalized, job- and company-specific cover letters with AI assistance.
- **Interview Preparation:** Access custom quiz-based interview training, track performance trends, and get real-time feedback.
- **Industry Insights Dashboard:** Analyze market outlook, salary data, growth rates, and in-demand skills with interactive charts and metrics.
- **Secure Authentication:** Robust user authentication and onboarding, with protected flows to keep user data safe.
- **User-Centric Interface:** Clean and responsive UI for smooth navigation and usability across all devices.

---

## 🛠️ Tech Stack

- **Frontend:** Next.js 15, React 19, Tailwind CSS, Shadcn UI  
- **Backend:** Next.js API Routes, Prisma ORM, PostgreSQL (Neon DB)  
- **AI Integration:** Google Gemini API  
- **Authentication:** Clerk  
- **Other Libraries:** Inngest (for background jobs), React Hook Form, Zod
---

## 📁 Project Folder Structure

Below is the actual project folder structure for CareerMentorAI, illustrating the modular, scalable architecture and clear separation of concerns:
```
CAREERMENTORAI
├── .next
├── actions
├── app
│ ├── (auth)
│ │ ├── sign-in
│ │ │ └── [[...sign-in]]
│ │ │ └── page.jsx
│ │ ├── sign-up
│ │ │ └── [[...sign-up]]
│ │ │ └── page.jsx
│ │ └── layout.js
│ ├── (main)
│ │ ├── ai-cover-letter
│ │ │ ├── _components
│ │ │ │ ├── cover-letter-generator.jsx
│ │ │ │ ├── cover-letter-list.jsx
│ │ │ │ └── cover-letter-preview.jsx
│ │ │ ├── [id]
│ │ │ │ └── page.jsx
│ │ │ └── new
│ │ │ └── page.jsx
│ │ ├── dashboard
│ │ │ ├── _component
│ │ │ │ └── dashboard-view.jsx
│ │ │ └── page.jsx
│ │ ├── interview
│ │ │ ├── _components
│ │ │ │ ├── performace-chart.jsx
│ │ │ │ ├── quiz-list.jsx
│ │ │ │ ├── quiz-result.jsx
│ │ │ │ ├── quiz.jsx
│ │ │ │ └── stats-cards.jsx
│ │ │ ├── mock
│ │ │ └── page.jsx
│ │ ├── onboarding
│ │ │ ├── _components
│ │ │ │ └── onboarding-form.jsx
│ │ │ └── page.jsx
│ │ ├── resume
│ │ │ ├── _components
│ │ │ │ ├── entry-form.jsx
│ │ │ │ └── resume-builder.jsx
│ │ │ └── page.jsx
│ │ └── layout.jsx
│ ├── api
│ │ └── inngest
│ │ ├── route.js
│ ├── lib
│ │ ├── helper.js
│ │ └── schema.js
│ ├── favicon.ico
│ ├── globals.css
│ ├── layout.jsx
│ ├── not-found.jsx
│ └── page.jsx
├── components
│ ├── ui
│ │ ├── accordion.jsx
│ │ ├── alert-dialog.jsx
│ │ ├── badge.jsx
│ │ ├── button.jsx
│ │ ├── card.jsx
│ │ ├── dialog.jsx
│ │ ├── dropdown-menu.jsx
│ │ ├── input.jsx
│ │ ├── label.jsx
│ │ ├── progress.jsx
│ │ ├── radio-group.jsx
│ │ ├── select.jsx
│ │ ├── sonner.jsx
│ │ ├── tabs.jsx
│ │ ├── textarea.jsx
│ ├── header.jsx
│ ├── hero.jsx
│ └── theme-provider.jsx
├── data
│ ├── faqs.js
│ ├── features.js
│ ├── howitWorks.js
│ ├── industries.js
│ └── testimonial.js
├── hooks
│ └── use-fetch.js
├── lib
│ └── inngest
│ ├── client.js
│ ├── function.js
│ ├── checkUser.js
│ ├── prisma.js
│ └── utils.js
├── node_modules
├── prisma
├── public
├── .env
├── .eslintrc.json
├── .gitignore
├── components.json
├── eslint.config.mjs
├── jsconfig.json
├── middleware.js
├── next.config.mjs
├── package-lock.json
├── package.json
├── postcss.config.mjs
```


---

## 📸 Screenshots

- **Homepage (Without Sign In):**  
  ![Homepage without Sign In](./public/Screenshot%202025-08-05%20233658.png)
- **Homepage (With Sign In):**  
  ![Homepage with Sign In](./public/Screenshot%202025-08-05%20233732.png)
- **Industry Insights Dashboard:**  
  ![Industry Insights](./public/Screenshot%202025-08-05%20233748.png)
- **Resume Builder:**  
  ![Resume Builder](./public/Screenshot%202025-08-05%20233805.png)
- **Cover Letter Management:**  
  ![Cover Letter Management](./public/Screenshot%202025-08-05%20233831.png)
- **Interview Preparation:**  
  ![Interview Preparation](./public/Screenshot%202025-08-05%20233851.png)

---

## 📝 Getting Started

1. **Clone the Repository:**
    ```
    git clone https://github.com/yourusername/careermentorai.git
    ```
2. **Install Dependencies:**
    ```
    npm install
    ```
3. **Configure Environment Variables:**
   - Create a `.env` file in the root with the required variables:
    ```
    DATABASE_URL=
    NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
    CLERK_SECRET_KEY=
    NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
    NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
    NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/onboarding
    NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/onboarding
    GEMINI_API_KEY=
    ```
4. **Database Setup:**
    ```
    npx prisma generate
    npx prisma migrate dev
    ```
5. **Run the Development Server:**
    ```
    npm run dev
    ```

---


## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---

**CareerMentorAI empowers individuals to unlock their professional potential with smart automation and AI-driven insights.**