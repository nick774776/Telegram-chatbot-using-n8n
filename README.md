Telegram AI Agent Bot (n8n Workflow


A lightweight, scalable Telegram chatbot powered by n8n and OpenAI. This bot receives messages via Telegram, processes them through an intelligent AI Agent, and responds back to the user in real-time.🚀

How It WorksThe workflow follows a linear logic path designed for low latency and high reliability:Telegram Trigger: Watches for new incoming messages in your Telegram bot.AI Agent Node: The brain of the operation. It processes the incoming text using the connected model.OpenAI Chat Model: Provides the LLM capabilities (e.g., GPT-4o or GPT-3.5) to generate contextually relevant responses.Telegram Send Message: Delivers the AI-generated response back to the original sender.

🛠️ PrerequisitesBefore importing this workflow, ensure you have the following:n8n Instance: Self-hosted or n8n Cloud (Version 1.19.x or higher recommended for AI nodes).Telegram Bot Token: Created via @BotFather.OpenAI API Key: To power the "OpenAI Chat Model" node.


📦 InstallationClone the Repo:Bashgit clone https://github.com/your-username/telegram-ai-bot.git
Import to n8n:Open your n8n canvas.Copy the content of the workflow.json file.Paste it directly into the n8n editor.Configure Credentials:Click on the Telegram Trigger and Send Message nodes to add your Telegram API credentials.Click on the OpenAI Chat Model node to add your OpenAI API key.Activate: Toggle the "Active" switch in the top right corner of n8n.

⚙️ Configuration DetailsNodePurposeKey SettingsTelegram TriggerEntry pointUpdates: messageAI AgentLogic LayerAgent Type: ConversationalOpenAI ModelBrainsModel: gpt-4o (or preferred)Telegram SendOutputChat ID: {{ $json.message.chat.id }}Extending FunctionalityThe AI Agent node in this workflow has empty slots for Memory and Tools. You can easily add:Window Buffer Memory: To allow the bot to remember previous parts of the conversation.Calculator/Google Search Tools: To give the bot the ability to perform live tasks.

📝 LicenseThis project is licensed under the MIT License - see the LICENSE file for details.
