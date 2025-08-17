<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GitHub README Updater</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        .fade-in {
            animation: fadeIn 0.5s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="bg-gray-900 text-gray-200 flex items-center justify-center min-h-screen p-4">

    <div class="w-full max-w-4xl bg-gray-800 rounded-2xl shadow-2xl p-6 md:p-8 border border-gray-700">
        <div class="text-center mb-6">
            <h1 class="text-3xl md:text-4xl font-bold text-white">📊 README Roadmap Updater</h1>
            <p class="text-gray-400 mt-2">Enter your new level to automatically update your project checklist.</p>
        </div>

        <!-- Input Section -->
        <div class="flex flex-col sm:flex-row items-center justify-center gap-4 mb-6">
            <label for="levelInput" class="text-lg font-medium">Enter Your Current Level:</label>
            <input type="number" id="levelInput" min="0" max="100" value="1" class="bg-gray-700 text-white w-24 text-center text-lg p-2 rounded-lg border border-gray-600 focus:ring-2 focus:ring-blue-500 focus:outline-none transition">
            <button id="updateBtn" class="w-full sm:w-auto bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-6 rounded-lg transition-transform transform hover:scale-105 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-opacity-50">
                Generate README
            </button>
        </div>

        <!-- Output Section -->
        <div class="relative">
            <textarea id="output" class="w-full h-96 bg-gray-900 text-gray-300 p-4 rounded-lg border border-gray-700 focus:ring-2 focus:ring-blue-500 focus:outline-none" readonly></textarea>
            <button id="copyBtn" class="absolute top-3 right-3 bg-gray-700 hover:bg-gray-600 text-white font-semibold py-1 px-3 rounded-md text-sm transition-transform transform hover:scale-105">
                Copy
            </button>
        </div>
        
        <!-- Toast Notification -->
        <div id="toast" class="fixed bottom-5 right-5 bg-green-500 text-white py-2 px-4 rounded-lg shadow-lg transition-opacity duration-300 opacity-0">
            Copied to clipboard!
        </div>
    </div>

    <script>
        const levelInput = document.getElementById('levelInput');
        const updateBtn = document.getElementById('updateBtn');
        const outputEl = document.getElementById('output');
        const copyBtn = document.getElementById('copyBtn');
        const toast = document.getElementById('toast');

        const readmeTemplate = `<div align="center">

# 📊 Big Data & Data Science Project Roadmap 🚀

A personal roadmap to track my journey from Level 1 to 100 in the world of Data Science and Big Data.

<!-- 
======================================================================================
== HOW TO UPDATE YOUR LEVEL ==
1. Change the number '{level}' in the URL below to your current level.
2. For example, if you are at level 25, the URL should look like this:
   https://img.shields.io/badge/Current%20Level-25%2F100-brightgreen?style=for-the-badge&logo=python
======================================================================================
-->
<img src="https://img.shields.io/badge/Current%20Level-{level}%2F100-{color}?style=for-the-badge&logo=python" alt="Current Level: {level}/100">

</div>

---

### 🎯 **How to Use This Roadmap**

1.  **Update Your Level:** Edit the image URL above to reflect your current level.
2.  **Track Projects:** As you complete a project, mark the checkbox next to it by changing \`[ ]\` to \`[x]\`.
3.  **Expand Sections:** Click on any level range to see the projects within it.

---

## 🌱 Levels 1-20: Beginner Projects

<details>
<summary><strong>Click to expand/collapse</strong></summary>

- [ ] Data cleaning and visualization with Python
- [ ] Student performance analysis (Excel, Pandas)
- [ ] Simple exploratory studies (Iris dataset, Titanic dataset)
- [ ] Basic classification (flower, wine, heart disease, etc.)
- [ ] Spam detection in emails/texts
- [ ] Credit card fraud detection (simple dataset)
- [ ] Recipe or expense tracker with charts
- [ ] Simple regression (house prices, rainfall)
- [ ] Cartoonify images with OpenCV
- [ ] Calories burnt predictor (fitness dataset)
- [ ] **Project 11**
- [ ] **Project 12**
- [ ] **Project 13**
- [ ] **Project 14**
- [ ] **Project 15**
- [ ] **Project 16**
- [ ] **Project 17**
- [ ] **Project 18**
- [ ] **Project 19**
- [ ] **Project 20**

</details>

---

## 🧑‍💻 Levels 21-40: Novice Projects

<details>
<summary><strong>Click to expand/collapse</strong></summary>

- [ ] Portfolio/Blog with data insights
- [ ] Color detection in images
- [ ] Simple OCR for handwritten digits
- [ ] Churn prediction (telecom)
- [ ] Sentiment analysis (tweets, Facebook posts)
- [ ] Medical insurance predictor
- [ ] Simple clustering (customer segmentation)
- [ ] Simple recommendation system (books, movies)
- [ ] Stock price forecasting
- [ ] Fake news detection
- [ ] **Project 31**
- [ ] **Project 32**
- [ ] **Project 33**
- [ ] **Project 34**
- [ ] **Project 35**
- [ ] **Project 36**
- [ ] **Project 37**
- [ ] **Project 38**
- [ ] **Project 39**
- [ ] **Project 40**

</details>

---

## 🛠️ Levels 41-60: Intermediate Projects

<details>
<summary><strong>Click to expand/collapse</strong></summary>

- [ ] Movie recommendation using collaborative filtering
- [ ] NLP analysis of restaurant reviews
- [ ] Forecasting sales/box office revenue
- [ ] Rainfall prediction using ML
- [ ] Forecasting traffic or vehicle count
- [ ] Expense tracker web app with monthly analytics
- [ ] Loan eligibility prediction
- [ ] Fitness/Workout planner app
- [ ] Detecting faces/objects in images (OpenCV)
- [ ] **Project 50**
- [ ] **Project 51**
- [ ] **Project 52**
- [ ] **Project 53**
- [ ] **Project 54**
- [ ] **Project 55**
- [ ] **Project 56**
- [ ] **Project 57**
- [ ] **Project 58**
- [ ] **Project 59**
- [ ] **Project 60**

</details>

---

## 📈 Levels 61-80: Upper Intermediate Projects

<details>
<summary><strong>Click to expand/collapse</strong></summary>

- [ ] Real-time chat application (Socket.IO)
- [ ] Real-time sentiment analysis (Twitter streaming)
- [ ] Image caption generator
- [ ] Customer churn prediction with ensemble methods
- [ ] Real-time dashboard (stock market, weather)
- [ ] News aggregator with category filters
- [ ] Disease prediction (Parkinson’s, breast cancer, etc.)
- [ ] Predicting home/stock prices with advanced algorithms
- [ ] Personal budget app with predictive analytics
- [ ] **Project 70**
- [ ] **Project 71**
- [ ] **Project 72**
- [ ] **Project 73**
- [ ] **Project 74**
- [ ] **Project 75**
- [ ] **Project 76**
- [ ] **Project 77**
- [ ] **Project 78**
- [ ] **Project 79**
- [ ] **Project 80**

</details>

---

## 🚀 Levels 81-100: Advanced & Expert Projects

<details>
<summary><strong>Click to expand/collapse</strong></summary>

- [ ] Multiclass image classification (using transfer learning)
- [ ] Real-time fraud detection (banking dataset + Kafka)
- [ ] Large-scale log data analysis (Hadoop/Spark)
- [ ] Flight delay prediction (big dataset)
- [ ] Large-scale music/movie recommendation systems
- [ ] Deep learning for lung/pneumonia/covid detection (medical images)
- [ ] Voice assistant/Speech recognition (Google API, Python)
- [ ] NLP-based hate speech detection
- [ ] AI-powered video/image editor
- [ ] Blockchain-based voting or supply-chain management system
- [ ] IoT health dashboard (stream data from multiple sensors)
- [ ] Face and hand landmarks detection
- [ ] Decentralized marketplace on blockchain
- [ ] SaaS project management tool
- [ ] Real-time video streaming platform (HLS/AWS)
- [ ] Real-time multiplayer game (Socket.IO)
- [ ] Language learning app with AI grammar check
- [ ] **Project 98**
- [ ] **Project 99**
- [ ] **Project 100**

</details>

---
<div align="center">
Made with ❤️ and Python.
</div>`;

        function getBadgeColor(level) {
            if (level <= 20) return 'blue';
            if (level <= 40) return 'yellow';
            if (level <= 60) return 'orange';
            if (level <= 80) return 'green';
            return 'brightgreen';
        }

        function updateReadme() {
            let level = parseInt(levelInput.value);
            if (isNaN(level) || level < 0) level = 0;
            if (level > 100) level = 100;
            
            levelInput.value = level; // Sanitize the input field

            // 1. Update badge
            const color = getBadgeColor(level);
            let updatedContent = readmeTemplate.replace(/{level}/g, level);
            updatedContent = updatedContent.replace('{color}', color);

            // 2. Update checkboxes
            let count = 0;
            updatedContent = updatedContent.replace(/\[ \]/g, (match) => {
                count++;
                return count <= level ? '[x]' : '[ ]';
            });

            outputEl.value = updatedContent;
            outputEl.classList.add('fade-in');
            setTimeout(() => outputEl.classList.remove('fade-in'), 500);
        }

        updateBtn.addEventListener('click', updateReadme);
        
        copyBtn.addEventListener('click', () => {
            outputEl.select();
            // Using execCommand for broader compatibility in sandboxed environments
            try {
                document.execCommand('copy');
                toast.classList.remove('opacity-0');
                setTimeout(() => {
                    toast.classList.add('opacity-0');
                }, 2000);
            } catch (err) {
                console.error('Failed to copy text: ', err);
            }
        });

        // Initial generation
        updateReadme();
    </script>
</body>
</html>
