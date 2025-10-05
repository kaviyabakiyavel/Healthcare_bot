# Medical chatbot with LLM , Langchain , Pinecone , Flask , AWS 

You can automate this setup with a shell script (e.g., setup_project.sh) that runs all your commands at once.Here’s how you can create it:

1. Go to the folder where you want your project

For example, if you want it inside ~/projects/myapp:

cd ~/projects/myapp

2. Create the script file
nano setup_project.sh


(or use vim, notepad on Windows with Git Bash, or code setup_project.sh if you’re using VS Code)

3. Paste the script into it
#!/bin/bash

mkdir -p src
mkdir -p research

touch src/__init__.py
touch src/helper.py
touch src/prompt.py
touch .env
touch setup.py
touch app.py
touch research/trials.ipynb
touch requirements.txt

echo "Directory and files created successfully!."

4. Save and close

In nano: press CTRL + O, then ENTER, then CTRL + X.

5. Make the script executable
chmod +x setup_project.sh

6. Run it
./setup_project.sh


After running, you’ll see your src/, research/, and all files created in your current folder. 



Open your terminal (Anaconda Prompt on Windows, or normal terminal if Conda is installed).

Run:

conda create -n medibot python=3.10 -y


Activate the environment:

conda activate medibot


Now install your requirements (once you have them in requirements.txt):

pip install -r requirements.txt