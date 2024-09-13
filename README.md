# 🏋🏽🔥💪🏼 AI-Driven Gym and Nutrition Workflow with CrewAI and IBM Watson

Welcome to the **AI-Driven Gym and Nutrition Workflow** project! As someone who is passionate about fitness and nutrition, I created this workflow to leverage advanced AI technologies to optimize gym routines and dietary plans. This repository demonstrates how to build an intelligent system using CrewAI, CrewAI Tools, and IBM Watson’s language models.

---

## 🌟 **Overview**

This project combines:

- **CrewAI**: A framework for creating and managing AI-driven workflows with intelligent agents. These agents are designed to perform specific tasks, such as researching gym routines or creating dietary plans.
- **CrewAI Tools**: Includes the Serper tool for internet searches, allowing agents to fetch real-time and relevant information from the web.
- **LangChain IBM**: A library that enables interaction with IBM Watson’s language models, providing advanced natural language processing capabilities to the agents.

### **Models Used**

- **LLaMA 3-70B Instruct**: A powerful language model designed to generate high-quality responses based on detailed instructions.
- **Mistral Large**: A robust model optimized for specific functions and tasks.

---

## 🔑 **Configuration**

To set up your environment and authenticate the APIs, use the following code in your Colab notebook:

```python
# Authenticate Google Colab and get stored credentials for APIs
from google.colab import userdata
import os

# Retrieve API keys from Colab's environment
serper = userdata.get('serper')
watson = userdata.get('watson')
project_id = userdata.get('project_id')

# Setting up API keys for Watson and Serper
os.environ["WATSONX_APIKEY"] = watson
os.environ["SERPER_API_KEY"] = serper
os.environ["PROJECT_ID"] = project_id
```

You can obtain the necessary API keys from the Serper and IBM Cloud websites.

---

## 🤖 **Creating Agents and Tasks**

### **Agent Overview**

- **Researcher Agent**: This agent uses language models and internet search tools to gather and analyze information on gym routines and nutrition strategies. Its goal is to find relevant studies, research papers, and expert opinions.

- **Trainer Agent**: This agent uses the gathered research to create a detailed 6-day workout split for hypertrophy, including exercises, sets, and reps. It also organizes rest times to optimize muscle growth.

- **Nutrition Researcher Agent**: This agent focuses on researching nutrition strategies for bulking and cutting. It gathers information on effective diets, meal plans, and nutritional guidelines from reliable sources.

- **Nutrition Planner Agent**: This agent uses the research findings to create a comprehensive 7-day dietary plan for either bulking or cutting. It provides specific meal plans, including breakfast, lunch, and dinner.

### **Tasks**

- **Research Gym Routines**: Find and summarize the top research on effective gym routines for hypertrophy.
- **Plan Workout Split**: Develop a 6-day workout plan based on the research findings.
- **Research Nutrition**: Gather information on nutrition strategies for bulking and cutting.
- **Create Dietary Plan**: Develop a 7-day dietary plan based on the nutrition research.

---

## 📝 **Results**

You can find the results from the four agents in the [Results Directory](https://github.com/Jesteban247/AI-Driven-Gym-and-Nutrition-Workflow-with-CrewAI-and-IBM-Watson/tree/main/Results). The directory contains four text files detailing the outputs from each agent:

1. **Researcher Agent Results**
2. **Trainer Agent Results**
3. **Nutrition Researcher Agent Results**
4. **Nutrition Planner Agent Results**

---

## 🙏 **Acknowledgments**

We would like to acknowledge IBM Technology for providing the powerful Watson language models used in this project. For an in-depth explanation of IBM’s technology, you can watch this informative video:

[**Introduction to IBM Watson**](https://youtu.be/gUrENDkPw_k?si=mwp5Qg3_WQtzG9fj)

---

## 🔍 **Conclusion**

The current setup with a token limit of 500 is effective for controlling costs and generating concise responses. However, for more comprehensive results, especially in complex research and writing tasks, increasing the token limit would be advantageous. For now, managing token usage carefully while optimizing prompts and exploring decoding methods can help maximize the efficiency and effectiveness of the AI agents.
