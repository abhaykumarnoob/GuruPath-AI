# GuruPath AI – Requirements Specification

## 1. Project Overview
GuruPath AI is a mobile-based, multilingual AI-powered learning and developer productivity assistant.  
The application aims to help students and beginner developers learn faster, understand complex concepts, debug code, and follow personalized learning paths in their preferred Indian languages.

---

## 2. Problem Statement
Learners and beginner developers often struggle with:
- Understanding complex technical concepts
- Reading lengthy documentation
- Debugging programming errors
- Learning from English-only tools

This leads to slow learning, reduced confidence, and low productivity.

---

## 3. Objectives
- Provide clear and simple explanations for technical concepts
- Improve developer productivity by explaining code and errors
- Offer personalized learning paths based on user goals
- Support multiple Indian languages to improve accessibility
- Deliver a mobile-first learning experience

---

## 4. Target Users
- College students
- Beginner developers
- Non-English native learners
- Self-learners in Tier-2 and Tier-3 cities

---

## 5. Functional Requirements

### 5.1 User Onboarding
- The system shall allow users to access the app without mandatory login.
- The system shall allow users to select their preferred language at startup.

### 5.2 Language Support
- The system shall support the following languages:
  - English
  - Hindi
  - Marathi
  - Gujarati
  - Tamil
  - Telugu
- The system shall allow users to change language at any time.

### 5.3 AI Concept Tutor
- The system shall allow users to input a topic or concept.
- The system shall generate step-by-step explanations.
- The system shall use simple language and examples.
- The system shall translate explanations into the selected language.

### 5.4 Code Explanation & Debugging
- The system shall allow users to paste code snippets.
- The system shall explain the purpose of the code.
- The system shall identify common errors.
- The system shall provide suggestions for improvement.

### 5.5 Learning Path Generator
- The system shall allow users to input:
  - Current skill level
  - Learning goal
- The system shall generate a personalized learning roadmap.
- The system shall recommend next learning steps.

### 5.6 Documentation Summarizer
- The system shall allow users to upload text or documents.
- The system shall generate concise summaries.
- The system shall highlight key takeaways.

### 5.7 User Preferences & Progress
- The system shall store user language preference.
- The system shall track basic learning interactions (optional).

---

## 6. Non-Functional Requirements

### 6.1 Usability
- The application shall be mobile-friendly.
- The UI shall be simple and beginner-friendly.

### 6.2 Performance
- AI responses shall be generated within acceptable time limits.
- The system shall handle multiple user requests efficiently.

### 6.3 Scalability
- The system shall use a serverless architecture.
- The system shall scale automatically based on usage.

### 6.4 Security
- The system shall not store sensitive personal data.
- Uploaded documents shall be handled securely.

---

## 7. Technology Requirements
- Mobile Application: Flutter / React Native
- Backend: AWS Lambda, API Gateway
- AI Services: Amazon Bedrock
- Translation: Amazon Translate
- Database: Amazon DynamoDB
- Storage: Amazon S3

---

## 8. Constraints
- The project is developed by a single team member.
- The solution focuses on MVP-level implementation.
- Internet connectivity is required for AI processing.

---

## 9. Assumptions
- Users have basic smartphone access.
- Users are beginners or intermediate learners.
- AI responses are used as learning assistance, not authoritative sources.

---

## 10. Future Enhancements
- Voice-based interaction
- Offline learning mode
- Progress analytics dashboard
- Gamified learning experience
