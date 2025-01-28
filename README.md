# Reddit Automation Bot

This project is a Reddit automation bot designed to perform various tasks on Reddit, such as logging into an account, posting images with titles, and commenting on specific posts. The bot uses Selenium integrated with Undetected ChromeDriver to automate browser interactions, ensuring stability and stealth.

---

## Features

### 1. **Login Automation**
- Automatically logs into a Reddit account using the credentials securely stored in a `.env` file.
- Ensures a smooth and error-free login process.

### 2. **Post Creation**
- Uploads images with descriptive titles to a specified subreddit.
- Retrieves titles dynamically from a JSON file (`image_titles.json`).

### 3. **Comment Posting**
- Posts random comments to a target post using predefined text stored in a `comments.txt` file.
- Ensures randomized interaction to avoid detection.

### 4. **Dynamic Configuration**
- Environment variables are used for customizable settings, enabling flexibility in bot behavior without modifying code.

---

## Prerequisites

Before setting up the bot, ensure you meet the following requirements:

### **1. Python**
- Install **Python 3.7 or above**.

### **2. Google Chrome**
- Ensure the **latest version of Google Chrome** is installed on your system.
- Chrome updates may require an updated ChromeDriver, so keep both in sync.

### **3. Required Python Packages**
Install the following dependencies:
- `selenium`
- `undetected-chromedriver`
- `python-dotenv`

---

## Installation Steps

### **Step 1: Clone the Repository**
Open your terminal and run the following commands:
```bash
# Clone the repository
git clone https://github.com/Kirtan-Rajesh/Reddit_Bot.git

# Navigate into the project directory
cd Reddit_Bot
```

### **Step 2: Set Up a Virtual Environment (Optional but Recommended)**
Creating a virtual environment helps manage dependencies without affecting your global Python installation.

- **Create a virtual environment:**
  ```bash
  python -m venv venv
  ```

- **Activate the virtual environment:**
  - On macOS/Linux:
    ```bash
    source venv/bin/activate
    ```
  - On Windows:
    ```bash
    venv\Scripts\activate
    ```

### **Step 3: Install Dependencies**
Install all required Python packages using the `requirements.txt` file:
```bash
pip install -r requirements.txt
```

### **Step 4: Configure Environment Variables**
Create a `.env` file in the root directory of the project with the following content:
```plaintext
REDDIT_USERNAME=<your_reddit_username>
REDDIT_PASSWORD=<your_reddit_password>
IMAGE_FOLDER=<path_to_folder_with_images>
COMMENTS_FILE=<path_to_comments.txt>
TITLES_FILE=<path_to_image_titles.json>
TARGET_POST_URL=<url_of_the_target_post>
```
Replace the placeholder values (e.g., `<your_reddit_username>`) with actual data for your Reddit account and file paths.

### **Step 5: Prepare Supporting Files**

1. **Images**:
   - Place all images you want to upload in the folder specified in `IMAGE_FOLDER`.

2. **Comments**:
   - Create a `comments.txt` file containing comments, one per line, for randomized posting. Example:
     ```plaintext
     This is an amazing post!
     Loved the content, keep it up!
     Incredible insights, thank you for sharing!
     ```

3. **Titles**:
   - Create an `image_titles.json` file to map image filenames to their respective titles. Example:
     ```json
     {
       "image1.jpg": "A Funny Meme Title",
       "image2.png": "Another Interesting Meme Title",
       "image3.jpeg": "Insightful Meme Title"
     }
     ```

---

## Usage

### **Run the Bot**
To execute the bot, simply run the following command:
```bash
python reddit_bot.py
```

### **Bot Workflow**
The bot performs the following steps:
1. Logs into Reddit using the credentials specified in the `.env` file.
2. Posts a random image from the specified folder along with its title.
3. Posts a random comment to the specified target post.

---

## Challenges Faced

### **1. Appium Setup Issues**
- Initially attempted to use Appium for mobile browser automation, but faced compatibility issues with ChromeDriver.
- Switched to Selenium with Undetected ChromeDriver for better stability and ease of use.

### **2. Dynamic Web Elements**
- Encountered difficulties in locating dynamic elements (e.g., comment boxes, post buttons).
- Resolved these issues by using `WebDriverWait` and explicit conditions in Selenium.

### **3. ChromeDriver Updates**
- Regular Chrome updates required ensuring that the ChromeDriver version matched the browser version.
- Addressed this by keeping Chrome and ChromeDriver in sync.

### **4. Rate Limits**
- Managed Reddit's API rate limits by pacing automation tasks to avoid triggering security measures.

---

## Future Enhancements

1. **Additional Features**:
   - Implement functionalities like upvoting posts or replying to comments.
   - Enable multiple account support for diverse interactions.

2. **Improved Error Handling**:
   - Add robust exception handling for scenarios where dynamic elements are missing or change frequently.

3. **AI Integration**:
   - Use AI models to generate more engaging comments and post titles dynamically.

4. **Scheduling Support**:
   - Add features to schedule posts and comments for specific times.

---

## Contribution Guidelines

We welcome contributions! If you'd like to contribute:
1. **Fork the repository** and create a new branch.
2. Make your changes or additions.
3. Submit a **pull request** with a clear description of your modifications.

For any queries or suggestions, feel free to open an issue in the repository.

---

## Contact
For questions, you can reach out via:
- GitHub Issues: [GitHub Repository](https://github.com/Kirtan-Rajesh/Reddit_Bot)
- Email: [pyanggz@gmail.com](mailto:pyanggz@gmail.com)

---

This bot demonstrates expertise in browser automation, showcasing how tools like Selenium can be used to interact with websites dynamically and efficiently.

