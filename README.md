# Automated-Drone-News-LinkedIn-Publisher

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

<img width="1917" height="737" alt="image" src="https://github.com/user-attachments/assets/f4b0e234-04eb-4e04-95e5-fa38e1b09d70" />


### 🤖 AI-Generated Content

<img width="1852" height="760" alt="image" src="https://github.com/user-attachments/assets/3e9e97ed-849e-4be7-ab5d-7a1838f4092c" />
<img width="738" height="250" alt="image" src="https://github.com/user-attachments/assets/3205add9-5ec6-4504-8f22-cec6459a3b2e" />



### 💼 LinkedIn Auto-Post

<img width="708" height="772" alt="Linkdin post" src="https://github.com/user-attachments/assets/308e1994-de44-4919-9ce1-9c1e22e76ab6" />
<img width="741" height="622" alt="Lindin post" src="https://github.com/user-attachments/assets/3d016cda-32eb-41e8-a45f-a74fe0e07703" />



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

