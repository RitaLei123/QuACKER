# QuACKER

**QuACKER – Questionably Accurate Course Knowledge, Evaluation, & Ratings**

QuACKER is a lightweight, web-based platform that helps students explore, evaluate, and review courses. Instead of hunting for recommendations from peers, Reddit threads, or RateMyProfessor, QuACKER centralizes all the key course information in one place: easiness, usefulness, workload, attendance requirements, average grades, and anonymous reviews.

QuACKER embodies the Retro v Modern theme: it’s inspired by the old-school ritual of asking classmates for advice, but built using modern web tech and AI for a fast, interactive experience.

## Features

- **Course Rankings**: Based on multiple metrics (Easiness, Usefulness, Workload, Attendance, Avg. Grade)
- **Anonymous Reviews & Ratings**: Stored securely in Firebase
- **AI-Generated Course Summaries**: Uses the Google Gemini API to summarize student sentiment from reviews.
- **Interactive Web Interface**: Fully built with HTML, CSS, and JavaScript
- **Browser-Based**: No backend server required, hosted on GitHub Pages
- **Search & Filter Courses**: Quickly find the best courses for your interests

## Inspiration

Choosing courses is a pain point for students everywhere. Before QuACKER, students often:

- Asked peers for advice
- Scrolled through Reddit threads for tips
- Checked RateMyProfessor for reviews

QuACKER simplifies this process, making it faster and more reliable to research courses before registering. It captures the nostalgia of peer recommendations while leveraging modern technology and AI to present information clearly and efficiently.

## Tech Stack

- **Frontend**: HTML, CSS, JavaScript
- **Database**: Firebase (for storing anonymous reviews)
- **AI Assistance**: Google Gemini (for generating AI-powered course insights)
- **Hosting**: GitHub Pages

## Data Source

The course catalog data (including course names, numbers, descriptions, and prerequisites) used in this project is sourced from QuACS, the RPI course scheduling tool. This project builds upon their data to add a layer of community-driven reviews and AI-powered insights.

## AI-Powered Insights

QuACKER uses the Google Gemini API to provide valuable, at-a-glance summaries of student feedback. When a course has enough reviews, the platform sends the anonymous comments to the `gemini-2.5-flash-preview-09-2025` model.

The AI, acting as a student advisor, then generates a concise, one-paragraph summary of the general student sentiment. This allows students to quickly understand the common themes around a course's difficulty, workload, and usefulness without having to read every single review.

## Installation / Running Locally

Since QuACKER is hosted on GitHub Pages, you can access it directly:

**URL**: [https://www.quacker.tech/](https://www.quacker.tech/)

### To run it locally:

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/quacker.git
````

2. Navigate into the project folder:

   ```bash
   cd quacker
   ```
3. Open `index.html` in your browser.

(Optional) Connect your own Firebase project for anonymous reviews.

## Usage

* Browse courses by department, professor, or semester
* Check Easiness, Usefulness, Workload, Attendance, and Avg. Grade metrics
* Read AI-generated summaries of student feedback
* Submit anonymous ratings and reviews
* Sort courses based on your preferred criteria

## License

This project is licensed under the MIT License – see [LICENSE](LICENSE) for details.

## Fun Fact

The name QuACKER keeps the “questionably accurate” vibe of QuACS while letting students **quack** about courses anonymously! 🦆