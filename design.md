# GuruPath AI – System Design Document

## 1. Introduction
GuruPath AI is a mobile-based, multilingual AI-powered learning and developer productivity assistant.  
The system is designed using a serverless, scalable architecture to provide AI-driven explanations, learning paths, and productivity tools in multiple Indian languages.

---

## 2. Design Goals
- Mobile-first user experience
- Simple and intuitive UI
- Scalable and cost-effective backend
- Meaningful use of AI for learning and productivity
- Multilingual support for Bharat-scale accessibility

---

## 3. System Architecture Overview
The system follows a client-server architecture with a serverless backend hosted on AWS.

### High-Level Components:
1. Mobile Application (Frontend)
2. Backend Services (API & Business Logic)
3. AI & Language Processing Layer
4. Data Storage Layer

---

## 4. Component Design

### 4.1 Mobile Application (Frontend)
- Built using Flutter or React Native
- Provides the following screens:
  - Language Selection Screen
  - Home Dashboard
  - Concept Tutor Screen
  - Code Explainer Screen
  - Learning Path Generator Screen
  - Document Summarizer Screen

**Responsibilities:**
- Capture user input
- Display AI-generated responses
- Handle language switching
- Provide a smooth mobile learning experience

---

### 4.2 Backend Services
- Implemented using AWS Lambda functions
- Exposed via Amazon API Gateway

**Responsibilities:**
- Receive requests from mobile app
- Validate user input
- Forward requests to AI services
- Return formatted responses to frontend

---

### 4.3 AI & Language Processing Layer

#### 4.3.1 AI Reasoning Engine
- Uses Amazon Bedrock
- Handles:
  - Concept explanations
  - Code understanding
  - Error explanation
  - Learning path generation
  - Document summarization

#### 4.3.2 Translation Service
- Uses Amazon Translate
- Translates AI-generated content into the selected user language

---

### 4.4 Data Storage Layer

#### 4.4.1 User Data Store
- Amazon DynamoDB
- Stores:
  - User language preference
  - Basic interaction history (optional)

#### 4.4.2 Document Storage
- Amazon S3
- Stores uploaded documents for summarization

---

## 5. Data Flow Design

### 5.1 Concept Explanation Flow
1. User enters a topic in the mobile app
2. Request sent to backend API
3. Backend forwards request to Amazon Bedrock
4. AI generates explanation
5. Response translated using Amazon Translate
6. Final output sent back to mobile app

---

### 5.2 Code Explanation Flow
1. User pastes code snippet
2. Backend processes the request
3. Amazon Bedrock analyzes the code
4. Explanation generated
5. Output translated if required
6. Response displayed to the user

---

### 5.3 Learning Path Generation Flow
1. User selects skill level and goal
2. Backend sends prompt to AI engine
3. AI generates structured roadmap
4. Roadmap translated to selected language
5. Learning path displayed in app

---

### 5.4 Document Summarization Flow
1. User uploads document/text
2. File stored temporarily in Amazon S3
3. Backend sends content to AI engine
4. Summary generated
5. Summary translated
6. Final summary shown to user

---

## 6. Security Design
- No sensitive personal data collected
- Secure API access via API Gateway
- Temporary document storage with controlled access
- Input validation to prevent misuse

---

## 7. Scalability & Performance
- Serverless backend ensures automatic scaling
- Pay-as-you-go model minimizes cost
- Stateless Lambda functions enable high availability

---

## 8. Error Handling & Reliability
- Graceful handling of invalid inputs
- Clear error messages for users
- Fallback responses in case of AI service failure

---

## 9. Limitations
- Requires internet connectivity
- AI-generated responses may occasionally be inaccurate
- Initial version focuses on text-based interaction

---

## 10. Future Enhancements
- Voice-based learning assistant
- Offline learning support
- Progress tracking dashboard
- Personalized quizzes and assessments
- AI-powered revision reminders
