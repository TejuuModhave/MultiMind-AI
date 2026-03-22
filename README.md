# 🧠 MultiMind AI

A modular **Spring Boot backend application** that integrates multiple AI capabilities using **Spring AI**.  
This project exposes REST APIs for conversational AI, image generation, and intelligent recipe creation.

---

## 🚀 Features

- 💬 **AI Chatbot**  
  Generate conversational responses using OpenAI chat models.

- 🖼️ **Image Generation**  
  Create AI-generated images based on prompts with configurable quality, size, and count.

- 🍳 **Recipe Generator**  
  Generate structured recipes based on ingredients, cuisine type, and dietary restrictions.

---

## 🏗️ Architecture

The project follows a **modular service-based architecture**:

- **Controller Layer**
  - Handles HTTP requests and routes them to appropriate services

- **Service Layer**
  - `ChatService` → Handles chatbot responses  
  - `ImageService` → Handles image generation  
  - `RecipeService` → Handles recipe creation using prompt templates  

- **Configuration Layer**
  - CORS configuration for frontend integration

---

## ⚙️ Tech Stack

- **Backend:** Java, Spring Boot  
- **AI Integration:** Spring AI (OpenAI)  
- **API Communication:** REST APIs  
- **Build Tool:** Maven  
- **Configuration:** application.properties  

---

## 📡 API Endpoints

### 1. Chatbot

`GET /ask-ai?prompt=your_text`

Example:

/ask-ai?prompt=What is Java?


---

### 2. Image Generation

`GET /generate-image?prompt=your_text&quality=hd&n=1&width=1024&height=1024`

Parameters:
- `prompt` → description of image  
- `quality` → hd / standard  
- `n` → number of images  
- `width`, `height` → resolution  

---

### 3. Recipe Generator

`GET /recipe-creator?ingredients=...&cuisine=...&dietaryRestriction=...`

Example:

/recipe-creator?ingredients=chicken,tomato&cuisine=indian


---

## 🖼️ Screenshots

> Add your screenshots inside a `screenshots` folder

### 🔹 Chatbot Response
![Chat Screenshot](./screenshots/chat.png)

### 🔹 Image Generation
![Image Screenshot](./screenshots/image.png)

### 🔹 Recipe Generator
![Recipe Screenshot](./screenshots/recipe.png)

---

## 🔐 Environment Variables

Add your OpenAI API key in `application.properties`:


spring.ai.openai.api-key=YOUR_API_KEY


---

## ▶️ Running the Project

1. Clone the repository:

git clone https://github.com/your-username/multimind-ai.git


2. Navigate to project:

cd multimind-ai


3. Add your API key in `application.properties`

4. Run the application:

mvn spring-boot:run

---

## 🔮 Future Improvements

- Implement logging and monitoring  
- Add conversation memory  
- Introduce retry and fallback mechanisms  

---

## 📌 Key Learnings

- Integrating AI into backend systems  
- Importance of prompt engineering  
- Handling non-deterministic AI responses  
- Designing modular and scalable services  

