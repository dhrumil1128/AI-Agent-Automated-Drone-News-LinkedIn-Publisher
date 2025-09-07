# AI-Agent-Automated-Drone-News-LinkedIn-Publisher

![n8n](https://img.shields.io/badge/n8n-Automation-orange?style=flat-square\&logo=n8n)
![Google Gemini](https://img.shields.io/badge/Google_Gemini-1.5_Flash-blue?style=flat-square\&logo=google)
![LinkedIn API](https://img.shields.io/badge/LinkedIn-API-0A66C2?style=flat-square\&logo=linkedin)
![RSS](https://img.shields.io/badge/News-Feeds-green?style=flat-square\&logo=rss)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)

---

## 🚀 Project Overview

This project implements an **AI-powered automation workflow** that collects the **latest drone industry news**, generates professional LinkedIn posts, and publishes them automatically.

The system leverages:

* 📡 **RSS feeds** for news discovery
* 🤖 **Google Gemini** for summarization and content generation
* ⚙️ **n8n workflow automation** for orchestration
* 💼 **LinkedIn API** for social media posting

The workflow runs **daily at 9:00 AM IST**, ensuring fresh, professional content is consistently posted on LinkedIn.

---

## ✨ Features

* **Automated News Discovery:** Collects the latest 3–5 drone-related news articles daily.
* **AI Summarization:** Summarizes each article into **3–5 professional paragraphs** suitable for LinkedIn.
* **Content Formatting:** Creates engaging posts with:

  * 🚨 Hook line
  * 📌 Concise professional summary
  * 🔹 Relevant hashtags
  * 🔗 Article link & call-to-action
* **Auto-Posting:** Publishes directly to **LinkedIn** using LinkedIn API.
* **Error Handling:** Prevents duplicate posts by appending timestamps.

---

## 🛠️ Technologies Used

* **n8n** – Workflow automation engine
* **RSS Feeds** – News discovery sources:

  * [DroneLife](https://dronelife.com/feed/)
  * [MIT UAV Technology](https://news.mit.edu/topic/uav/feed/)
  * [DGCA/India Drone Feeds](https://rss.feedspot.com/india_drone_rss_feeds/)
* **Google Gemini API (gemini-1.5-flash)** – Summarization & content generation
* **LinkedIn API** – Auto-post integration
* **JavaScript Expressions in n8n** – For content formatting and deduplication logic

---

## ⚙️ Architecture & How It Works

The automation operates in **4 key stages**:

1. **News Discovery**

   * RSS nodes fetch the latest articles from 3 drone-related feeds.
   * Limited to 3 articles per source to keep output focused.

2. **AI Summarization**

   * Each article’s content is passed to **Google Gemini**.
   * Gemini returns:

     * Long professional summary
     * Hashtags
     * Keywords

3. **Content Formatting**

   * n8n Set node structures the output into a LinkedIn post format:

     * 🚨 Hook line
     * 📌 Summary
     * 🔹 Hashtags
     * 🔗 CTA + link
     * 🕒 Timestamp

4. **Auto-Posting**

   * LinkedIn node publishes the content with **PUBLIC visibility**.
   * Runs daily at **9:00 AM IST**.

---

## 📂 Project Structure

```
/Drone-News-Automation
 ├── workflow.json           # n8n workflow export
 ├── /screenshots            # screenshots of UI/output
 │    ├── workflow.png
 │    ├── gemini_output.png
 │    ├── linkedin_post.png
 ├── README.md               # project documentation (this file)
```

---

## 🖼️ Sample Outputs

### 🔄 Workflow in n8n

![Workflow Screenshot](./screenshots/workflow.png)

### 🤖 AI-Generated Content

![Gemini Output](./screenshots/gemini_output.png)

### 💼 LinkedIn Auto-Post

![LinkedIn Post](./screenshots/linkedin_post.png)

---

## 💻 Local Setup & Installation

To set up and run this project locally:

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/your-username/drone-news-automation.git
   cd drone-news-automation
   ```

2. **Import the Workflow into n8n:**

   * Open your n8n instance.
   * Import `workflow.json`.

3. **Configure Credentials:**

   * Add your **Google Gemini API Key** in n8n credentials.
   * Connect your **LinkedIn OAuth2 API**.

4. **Test the Workflow:**

   * Manually trigger the workflow.
   * Verify LinkedIn receives the post.

---

## ☁️ Deployment

This automation can be deployed in:

* **n8n Cloud** (hosted by n8n.io)
* **Self-hosted n8n** on AWS, Docker, or Render
* **Cron-based servers** for consistent scheduling

Once deployed, the workflow runs **daily at 9:00 AM IST** automatically.

---

## 🤝 Contributing

Contributions are welcome! You can suggest improvements or open issues in this repo.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

⚡ Now your **Drone News Automation** repo will look just as professional as your RAG chatbot repo.

Do you also want me to prepare the **short PDF project report (2–3 pages with screenshots)** for HR submission, based on this README?
