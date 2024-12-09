<p>
  Artificial Intelligence is the primary skill that all developers should spend time learning as soon as possible.
  AI agents are the way to unleash the full power of AI capabilities. 
  
  This AI Agents n8n Starter Kit will help you use AI agents to transform projects, tasks, and businesses
  to create potent AI-powered software. 
</p>

<p align="center" style="margin-top: 25px">
  <a href="#what-are-ai-agents"><strong>What are AI Agents?</strong></a> ·
  <a href="#how-this-repo-works"><strong>How this Repo Works</strong></a> ·
  <a href="#instructions-to-follow-along"><strong>Instructions to Follow Along</strong></a>
</p>
<br/>

# Virtual Private Server Installation
<p>
<ul>
<li>1. Visit DigitalOceen.com and create a Droplet.</li>
<li>2. Login to your droplet.</li>
<li>3. Install docker and docker compose following these steps: https://medium.com/@tomer.klein/step-by-step-tutorial-installing-docker-and-docker-compose-on-ubuntu-a98a1b7aaed0</li>
<li>4. Clone this repo using the following commands</li>
<li>   # git clone https://github.com/pottertech/ai-agent-n8n-starter-kit.git</li>
<li>   # cd ai-agent-n8n-starter-kit</li>
<li>6. Configure the environment following these steps</li>
<li>   # cd local-ai-packaged</li>
<li>   # cp .env.example .env</li>
    nano .env
    Change all of the information to your desired settings for all of these entries:
       POSTGRES_USER=root
       POSTGRES_PASSWORD=password
       POSTGRES_DB=n8n
       N8N_ENCRYPTION_KEY=super-secret-key
       N8N_USER_MANAGEMENT_JWT_SECRET=even-more-secret
    Save the .env file by pressing ctrl+x
<li>Install apache2 using the following command: apt install apache2</li>
<li>If you are going to use SSL Install certbot following these steps: https://www.inmotionhosting.com/support/website/ssl/lets-encrypt-ssl-ubuntu-with-certbot </li>
  
<li>7. Install and run the kit using this step</li>
<li>   # docker compose --profile cpu pull</li>
<li>   # docker compose create && docker compose --profile cpu up</li>
   
Give it a few minutes and everything should be online for you to access.   
</p>
## What are AI Agents?

AI agents are Large Language Models, aka LLMs, that have been given the ability to interact with the outside world. They
can do things like draft emails, book appointments in your CRM, create tasks in your task management software, and
do almost anything you can think of. I hope that everything I show here can help you dream big
and create incredible things with AI!

AI agents can be very powerful without having to create a lot of code. That doesn't mean there isn't room though
to create more complex applications by tying things together with many different agents to accomplish
amazing things. 

Below is a basic diagram to get an idea of what an AI agent looks like:

<div align="center" style="margin-top: 25px;margin-bottom:25px">
<img width="700" alt="Trainers Ally LangGraph graph" src="https://i.imgur.com/ChRoV8W.png">
</div>

<br/>

## How this Repo Works

Each week there will be a new video for my AI Agents Masterclass! Each video will have its own folder
in this repo, starting with [/1-first-agent/](/1-first-agent) for the first video in the masterclass
where I create our very first AI agent! 

Any folder that starts with a number is for a masterclass video. The other folders are for other content
on my YouTube channel. The other content goes very well with the masterclass series (think of it as
supplemental material) which is why it is here too!

The code in each folder will be exactly what I used/created in the accompanying masterclass video.

<br/>

## Instructions to Follow Along

The below instructions assume you already have Git, Python, and Pip installed. If you do not, you can install
[Python + Pip from here](https://www.python.org/downloads/) and [Git from here](https://git-scm.com/).

To follow along with any of my videos, first clone this GitHub repository, open up a terminal,
and change your directory to the folder for the current video you are watching (for example: 1st video is [/1-first-agent/](/1-first-agent)).

The below instructions work on any OS - Windows, Linux, or Mac!

You will need to use the environment variables defined in the .env.example file in the folder (example for the first video: [`1-first-agent/.env.example`](/1-first-agent/.env.example)) to set up your API keys and other configuration. Turn the .env.example file into a `.env` file, and supply the necessary environment variables.

After setting up the .env file, run the below commands to create a Python virtual environment and install the necessary Python packages to run the code from the masterclass. Creating a virtual environment is optional but recommended! Creating a virtual environment for the entire masterclass is a one-time thing. Make sure to run the pip install for each video though!

```bash
python -m venv ai-agents-masterclass

# On Windows:
.\ai-agents-masterclass\Scripts\activate

# On MacOS/Linux: 
source ai-agents-masterclass/bin/activate

cd 1-first-agent (or whichever folder)
pip install -r requirements.txt
```

Then, you can execute the code in the folder with:

```bash
python [script name].py
```
