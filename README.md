# 🧵 TailorAI – Build a Crew to Tailor Job Applications  
**AI Agent Crew for crafting job-specific resumes and profiles**

---

## 📘 Project Overview

**TailorAI** is an AI-powered multi-agent system designed to help job seekers generate custom-tailored job applications using CrewAI.  
This system coordinates intelligent agents that analyze job descriptions, extract relevant criteria, and personalize user resumes and profiles to better match open positions.

**Built with:**
- `CrewAI` for orchestrating AI agents  
- `LangChain` + `OpenAI` for language understanding  
- Custom scraping and semantic tools for data gathering and resume enhancement

---

## 🧠 How It Works

TailorAI consists of three main agents:

- **🕵️ Tech Job Researcher**  
  Scrapes and analyzes job descriptions, highlighting key requirements, responsibilities, and desired skills.

- **🧬 Personal Profiler**  
  Examines user resumes and background to extract strengths, skills, and relevant accomplishments.

- **🪄 Resume Tailor**  
  Uses insights from the other agents to rewrite and enhance the resume so it aligns perfectly with the job.

These agents collaborate as a **Crew**, each assigned a specific `Task` that contributes to the final personalized output.

---

## 🧰 Installation & Setup

1. **Clone the Repository**

    ```bash
    git clone <your-repo-url>
    cd tailorAI


2. **Install dependencies manually**
    
    ```bash
    pip install -r requirements.txt
    ```
## OR

2. **(Optional but faster) Use Setup Script for Faster Installation**

    To automate installation and launch:

    - **For Linux/Mac/Git Bash users:**
      ```bash
      bash scripts/setup_and_launch.sh
      ```

    - **For Windows users:**
      - Double-click `scripts/setup_and_launch.bat`
      - Or run manually:
        ```bash
        scripts\setup_and_launch.bat
        ```


3. **Set up your environment variables**

    - Create a `.env` file in the project root directory.
    - Get your OpenAI API KEY ($5) @ <https://platform.openai.com/settings/organization/billing/overview> and  SERPER API KEY (free credits available) @ <https://serper.dev/api-key>
    - Add your OpenAI and Serper API key:
    
    ```
    OPENAI_API_KEY=your-openai-api-key
    SERPER_API_KEY=your-serper-api-key

    ```


## 🚀 Usage

Launch the notebook after setup:

  ```
  jupyter lab AI_Crew.ipynb

  ```
Follow the notebook to:

  1. Set up all three agents

  2. Provide a sample job description and resume

  3. Run the crew to generate tailored application content


Example execution snippet:
  ```python
  crew = Crew(
    agents=[researcher, profiler, tailor],
    tasks=[research_task, profile_task, tailoring_task],
    verbose=True
)
result = crew.kickoff()
print(result)

  ```

## Dependencies

All dependencies are listed in requirements.txt. Key libraries include:

  - crewai==0.28.8

  - crewai_tools==0.1.6

  - langchain_community==0.0.29

  - openai

  - python-dotenv

  - graphviz


**Install them with:** 

```
pip install -r requirements.txt

```

## 📊 Visual Flow (Optional)

TailorAI also includes agent graph visualization if you're curious about the execution flow.
You can render agent relationships using tools like graphviz and pydot.


## 📜 License
This project is licensed under the MIT License.
You are free to use, modify, and distribute this code with proper attribution.
