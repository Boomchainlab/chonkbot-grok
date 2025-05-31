# chonkbot-grok
: A sarcastic, meme-native AI bot for CHONK9K/Boomchainlab with integrations for Telegram, Discord, Twitter, and LLM-powered interactions.

🔧 Core Components
	•	Backend API: FastAPI application serving as the central hub for processing requests and managing interactions.
	•	Bot Interfaces: Telegram and Discord bots built using python-telegram-bot and discord.py, respectively, facilitating user engagement across platforms.
	•	LLM Integration: OpenAI’s GPT-4 Turbo integrated with a custom prompt layer to emulate Grok’s sarcastic and edgy persona.
	•	Twitter Data Fetcher: Module leveraging Twitter API v2 to pull real-time trending topics and relevant tweets.
	•	Sentiment Analysis: Incorporates VADER and transformer-based models to assess sentiment of fetched tweets and user inputs.
	•	Scheduler: Celery integrated with Redis for handling periodic tasks such as daily updates and scheduled messages.

⸻

🚀 Setup Instructions

1. Clone the Repository
2. git clone https://github.com/boomchainlab/chonkbot-grok.git
cd chonkbot-grok

2. Create and Activate Virtual Environment
3. python3 -m venv venv
source venv/bin/activate
3. Install Dependencies
4. pip install -r requirements.txt

5. 4. Configure Environment Variables
   5. Create a .env file in the root directory and populate it with the following keys:
   6. OPENAI_API_KEY=your_openai_api_key
TWITTER_BEARER_TOKEN=your_twitter_bearer_token
TELEGRAM_BOT_TOKEN=your_telegram_bot_token
DISCORD_BOT_TOKEN=your_discord_bot_token
REDIS_URL=redis://localhost:6379/0

5. Run the Application
6. uvicorn main:app --reload

7. 🧠 Prompt Engineering: Grok Persona

The bot is designed to emulate a sarcastic, meme-obsessed degen with a rebellious streak. Below is the prompt template used:

prompt_template = """
You are Chonkbot: a sarcastic, meme-obsessed, GPT-4-powered AI. You roast rugpulls, praise diamond hands, and always speak like a jaded degen who’s seen 3 bear markets. Format responses with meme energy, add emojis if needed. Stay edgy, but never NSFW.

User Input: {user_input}
"""
📅 Scheduler: Periodic Tasks

Utilizing Celery and Redis, the bot performs the following periodic tasks:
	•	Daily Alpha Drops: Shares daily market insights with a sarcastic twist.
	•	Token Roasts: Analyzes and mocks underperforming tokens.
	•	Trivia Challenges: Engages users with meme-themed trivia questions. ￼

⸻

📈 Future Enhancements
	•	WebSocket Integration: Enable real-time updates and interactions on the CHONK9K dApp.
	•	Advanced Sentiment Analysis: Incorporate more sophisticated models for nuanced sentiment detection.
	•	User Personalization: Allow users to customize the bot’s tone and response style.

⸻

📬 Next Steps
	1.	Deploy the Application: Set up the application on a cloud platform such as AWS, GCP, or Heroku.
	2.	Configure Webhooks: Establish webhooks for Telegram and Discord to enable real-time interactions.
	3.	Monitor and Iterate: Collect user feedback and iterate on the bot’s features and responses to enhance engagement.
