---

# 📄 Customer Review Insights & Response Generator

---

## 🚀 Project Overview

The **Customer Review Insights & Response Generator** is an automated, AI-powered workflow built using **n8n**, designed to process customer feedback in real-time and transform it into actionable insights.

This system integrates **Google Forms, Google Sheets, and Large Language Models (LLMs)** to:

- Analyze customer reviews
- Generate summaries
- Detect sentiment and tone
- Trigger automated alerts for negative feedback

The goal of this project is to demonstrate how modern automation tools combined with AI can streamline customer feedback analysis and improve response time for businesses.

---

## 🎯 Objectives

- Automate the collection and processing of customer reviews
- Extract meaningful insights using AI models
- Classify sentiment (**Positive / Neutral / Negative**)
- Identify tone (**Informative / Friendly / Persuasive**)
- Store structured insights for analysis
- Trigger alerts for negative reviews

---

## 🛠️ Technologies Used

- **n8n** – Workflow automation platform
- **Google Forms** – Data collection
- **Google Sheets** – Data storage & analytics
- **LLMs (Google Gemini / OpenAI)** – Text processing
- **Gmail API** – Automated notifications
- **JavaScript (n8n Code Node)** – Data filtering logic

---

## 🔄 Workflow Architecture

### 📌 Step-by-Step Flow

### 1. Data Collection

- Users submit feedback via Google Form
- Responses are stored in Google Sheets

### 2. Trigger Activation

- n8n Google Sheets Trigger detects new row entry

### 3. Latest Record Filtering

- A Code node ensures only the **latest entry** is processed
- Prevents duplicate processing and redundant entries

### 4. AI Processing Pipeline

- **Basic LLM Chain**
    - Generates a concise summary of the review
- **Sentiment Analysis**
    - Classifies sentiment with a confidence score
- **Tone Classification**
    - Determines communication tone of the review

### 5. Data Merging

- Original data (**Product Name, Feedback**) is merged with AI outputs
- Ensures complete structured output

### 6. Storage

- Processed insights are appended to a new Google Sheet

### 7. Conditional Logic

- IF node checks:
    - If sentiment = **Negative**

### 8. Automated Alert

- Gmail node sends notification to team lead

---

## 🧠 Key Features

### ✅ Real-Time Processing

Automatically processes incoming reviews without manual intervention.

### ✅ AI-Powered Insights

Uses LLMs to extract:

- Summaries
- Sentiment scores
- Tone classification

### ✅ Smart Filtering

Ensures only the **latest review** is processed to avoid duplication.

### ✅ Automated Alerts

Negative reviews trigger instant email notifications.

### ✅ Scalable Architecture

Workflow can be extended to:

- Dashboards
- CRM systems
- Customer support tools

---

## ⚠️ Challenges Faced

### 1. Duplicate Data Processing

- **Issue:** Multiple rows processed simultaneously
- **Solution:** Implemented Code node to filter latest record

### 2. Data Loss in LLM Nodes

- **Issue:** LLM nodes overwrite original JSON
- **Solution:** Used Merge node to combine original + processed data

### 3. OAuth Integration Issues

- **Issues Encountered:**
    - 414 URI Too Long error
    - Client authentication failures
- **Solution:**
    - Proper OAuth configuration
    - Use of tunnel/ngrok for stable URLs

---

## 💡 Why This Project is Important

### 🔍 Business Impact

- Enables **real-time customer feedback monitoring**
- Helps identify issues before escalation
- Improves customer satisfaction

### ⚡ Efficiency

- Eliminates manual review analysis
- Reduces response time significantly

### 📊 Data-Driven Decisions

- Structured insights allow trend analysis
- Supports strategic improvements

### 🤖 AI Integration

- Demonstrates practical use of LLMs in automation
- Bridges gap between AI and business workflows

---

## 📈 Use Cases

- E-commerce product feedback analysis
- SaaS customer experience monitoring
- Customer support escalation systems
- Market research automation

---

## 🔮 Future Enhancements

- Dashboard visualization (Google Data Studio / Power BI)
- Multi-language support
- Advanced sentiment scoring
- Integration with Slack / Teams
- Database storage (PostgreSQL / MongoDB)
- Webhook-based real-time system (instead of polling)

---

## 🧾 Conclusion

This project showcases how automation platforms like **n8n**, combined with AI models, can transform raw customer feedback into meaningful insights. It highlights the power of integrating multiple tools to create a scalable, intelligent system that enhances decision-making and customer engagement.

---

## 📌 Deliverables

- n8n Workflow (JSON export)
- Google Sheets (raw + processed data)
- Email alert system
- Documentation (this report)
