# CedCloudServerless

**CedCloudServerless** is a serverless web application that organizes educational YouTube content — starting with the MIT OpenCourseWare channel — to help users discover, filter, and explore academic video material efficiently.

This project is built using AWS Amplify, AppSync (GraphQL), Lambda, Cognito, and OpenSearch, with a Vue 3 front end. It is part of a dual-architecture initiative alongside its companion project, **CedCloudManaged**, which uses a traditional Spring Boot + EC2 setup.

---

## 🧱 Architecture

- **Frontend**: Vue 3 (Vite + TypeScript)
- **Backend**: AWS Lambda + AppSync (GraphQL)
- **Authentication**: Amazon Cognito
- **Search**: Amazon OpenSearch
- **Data Source**: YouTube API (via Lambda)
- **Hosting & CI/CD**: To be integrated with GitHub Actions (future)
- **Data Storage**: DynamoDB (primary), OpenSearch (for search/filter)

---

## 📁 Branching Strategy

- `development` – Active development work
- `release` – Staging area before merging to main
- `main` – Production-ready code (future CI/CD target)

---

## 🛠 Project Setup (Local Development)

```bash
# Install dependencies
npm install

# Start development server
npm run dev
