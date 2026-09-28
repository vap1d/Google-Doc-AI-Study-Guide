# Google-Doc-AI-Study-Guide
AI Generated Study Guide Notes from files in your Google Drive

Setting up the program: Create a new Google Doc to store the program (do not use an existing doc; if you want to use information from a specific doc, upload it to a designated folder for this project). Once you're in the new Doc, click on Extensions and then click Apps Script. Delete all the code in Code.gs and paste in the script. Click Ctrl+S to save the program (or manually click the floppy disk in the Toolbar). Then, click on the Triggers tab (the alarm clock) and click the blue "Add Trigger" button in the bottom right. Once you've clicked it, copy these settings (or adjust them to your needs):

Choose which function to run: syncFolderToStudyGuide
Choose which deployment should run: Head (should be only option)
Select event source: Time-driven
Select type of time-based trigger: Day timer (be careful with shortening the time in between events; you might get rate limited)
Select time of day: Whenever you don't think you'll need it (I have multiple Docs running this so I stagger the times when they run)
Failure notification settings: Notify me daily

After you've set it up, click save

You will need to create your own Gemini API Key for this to work. To do so, go to https://aistudio.google.com, click the "Get API Key" button near the bottom left of your screen (it's a key icon above where your email is). Once you're there, click the grey "Create API Key" in the top right. Name your key whatever you want (leave it as a Default Gemeni Product), and create your API key. Copy and paste this into the YOUR_API_KEY_HERE constant.

You will also need to obtain your Google Drive folder ID, but the proccess to obtain it is a lot more trivial. First, open up Google Drive in your browser and navigate to the folder where all of your information is. The script will run through ALL of the files in the folder, so create a separate folder if need be. Look at the URL of the folder and find the string of numbers and characters (drive.google.com/drive/folders/"LOOK HERE"). Anything else after the ? is junk, do not copy it. After that, copy the ID into the YOUR_ID_HERE constant. Save that as well.

If you want to test the code at any time, click the "Run" button in the Toolbar

Supports Google Docs, .pdf, and .txt files.

Note: The initial prompt is currently catered towards math classes with the demands, but feel free to change the prompt to fit your needs.
The program  will not combine elements in a folder together, it checks each seperate document and generates notes based off of that. If I decide to make functionality for that, this repo will be updated

This project is still very early on in development, so bear with me as I fix/improve certain aspects of the program