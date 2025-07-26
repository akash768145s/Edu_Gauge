# Edu-Gauge: Student Grade Analysis Dashboard

Edu-Gauge is a web application designed for academic institutions to efficiently manage, analyze, and visualize student performance data. It provides a comprehensive dashboard to view student grades, calculate GPA, rank students, and derive other meaningful analytics. Built with modern web technologies, it offers a fast, secure, and user-friendly experience.

## ✨ Features

- **User Authentication:** Secure sign-in for authorized personnel using Firebase Authentication.
- **Comprehensive Dashboard:** A central dashboard to view and analyze student data.
- **Dynamic Filtering:** Filter student data by academic year, semester, and a range of registration numbers.
- **In-depth Analysis:** Automatically calculates and displays:
  - **GPA (Grade Point Average)** for each student.
  - Total **Grade Points**.
  - **Deviation** from the class average GPA.
  - **Rank** of each student within the filtered group.
- **Data Management:** Functionality to add new batches, upload results, and manage records (inferred from project structure).
- **NBA Reports:** Potential for generating reports for the National Board of Accreditation (inferred from `nba` directory).
- **Responsive UI:** A clean and responsive user interface built with Tailwind CSS and shadcn/ui.

## 🛠️ Tech Stack

- **Framework:** [Next.js](https://nextjs.org/)
- **Language:** [TypeScript](https://www.typescriptlang.org/)
- **Authentication:** [Firebase Authentication](https://firebase.google.com/docs/auth)
- **Backend & Database:** [Firebase](https://firebase.google.com/) (Firestore likely)
- **Styling:** [Tailwind CSS](https://tailwindcss.com/)
- **UI Components:** [shadcn/ui](https://ui.shadcn.com/)
- **Deployment:** (Not specified, but `server.js` suggests a custom server setup might be possible)

## 🚀 Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

- [Node.js](https://nodejs.org/en/) (version 18.x or later recommended)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)

### Installation

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/your-username/edu-gauge.git
    cd edu-gauge
    ```

2.  **Install dependencies:**

    ```bash
    npm install
    ```

3.  **Set up Firebase:**

    - Create a new project on the [Firebase Console](https://console.firebase.google.com/).
    - Go to your project's settings and get your Firebase configuration object.
    - Create a `.env.local` file in the root of the project and add your Firebase configuration as environment variables:
      ```
      NEXT_PUBLIC_FIREBASE_API_KEY=your_api_key
      NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_auth_domain
      NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_project_id
      NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your_storage_bucket
      NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
      NEXT_PUBLIC_FIREBASE_APP_ID=your_app_id
      ```
    - Enable Email/Password sign-in in the Firebase Authentication section.
    - Set up Firestore database and define security rules as needed.

4.  **Run the development server:**
    ```bash
    npm run dev
    ```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## 📂 Project Structure

```
.
├── app/                  # Main application directory (App Router)
│   ├── sign-in/          # Sign-in page
│   ├── dashboard/        # Main dashboard page and components
│   ├── grade-analysis/   # Page for grade analysis
│   ├── add-batch/        # Page to add a new batch of students
│   ├── add-result/       # Page to add student results
│   ├── layout.tsx        # Root layout
│   └── page.tsx          # Main landing page
├── components/           # Shared UI components
│   ├── firebase/         # Firebase configuration and initialization
│   ├── navbar/           # Navigation bar components
│   └── ui/               # shadcn/ui components
├── lib/                  # Utility functions and libraries
├── public/               # Static assets (images, etc.)
├── tailwind.config.ts    # Tailwind CSS configuration
└── next.config.mjs       # Next.js configuration
```
