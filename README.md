# WhatsApp-Web-Auto-Messenger
This Python script automates sending a WhatsApp message to a specific contact using WhatsApp Web. It launches WhatsApp in your browser, searches for the contact, and sends a message automatically using pyautogui.
🧠 Description
This script simplifies messaging by automating basic actions on WhatsApp Web:

Opens WhatsApp Web in your browser.

Searches for a given contact by name.

Sends a user-defined message to that contact.

It uses:

webbrowser to open WhatsApp Web.

time for timed pauses between steps (allowing pages to load).

pyautogui to simulate mouse and keyboard actions.

⚙️ Requirements
Make sure you have the following installed:

bash
pip install pyautogui
Python Version: 3.6 or higher
Operating System: Windows / macOS / Linux

🚀 How to Use
Open your terminal or command prompt.

Run the Python script:

bash
python whatsapp_auto.py
Enter:

The contact name as saved in your WhatsApp.

The message you want to send.

The program will automatically:

Open WhatsApp Web.

Locate the contact.

Type and send your message.

🧩 Code Overview
python
import time
import pyautogui
import webbrowser

contacts = str(input('enter contact name : '))
message = str(input("enter message : "))

print('opening whatsapp')
time.sleep(2)
webbrowser.open('https://web.whatsapp.com/')
time.sleep(10)

x1, y1 = (189, 158)
pyautogui.moveTo(x1, y1)
time.sleep(0.5)
pyautogui.click()
pyautogui.typewrite(contacts)
pyautogui.press('enter')
time.sleep(1)

x2, y2 = (759, 842)
pyautogui.moveTo(x2, y2)
time.sleep(0.5)
pyautogui.click()
pyautogui.typewrite(message)
pyautogui.press('enter')
⚠️ Notes
Ensure you’re logged into WhatsApp Web before running the script.

Adjust the mouse coordinates (x1, y1 and x2, y2) based on your screen resolution.

This script simulates keyboard and mouse input — do not move your cursor or type during execution.

🛠️ Future Improvements
Replace hardcoded coordinates with image recognition (pyautogui.locateOnScreen).

Add error handling for missing contacts or network issues.

Enable sending multiple messages or group messages.
