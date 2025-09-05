# Shahzain-s-cool-learning-machine-2.0
📖 Shahzain’s Learning Machine – Stories Saver

Welcome to Shahzain’s Learning Machine Stories Saver!

This project allows you to save, load, and display Mad Libs–style stories from a CSV file.

It’s simple, fun, and a great way to practice programming with file handling, error handling, and user interaction in Python.


---

🚀 Features

✅ Save stories with class, name, story number, and passage.

✅ Load saved stories directly from a CSV file.

✅ Friendly error messages if the file is missing.

✅ Works on Windows, macOS, and Linux.

✅ UTF-8 encoding support (so no broken characters).


---

📂 File Structure

stories_saver/
│── stories_loader.py       # Script to read and display saved stories
│── stories_saver.py        # Script to save new stories into CSV
│── Shahzain_stories.csv    # CSV file where stories are stored
│── README.md               # Documentation


---

🛠️ Installation

1. Install Python

Download Python 3.9+ (any version 3.9 or above will work).

Verify installation:

python --version

or on some systems:

python3 --version



2. Clone this repository

git clone https://github.com/YourUsername/shahzain-stories-saver.git
cd shahzain-stories-saver


3. No extra dependencies needed! 🎉

Only Python’s built-in csv library is used.




---

▶️ Usage

1. Running the Loader (to read saved stories)

python stories_loader.py

If stories are found, you’ll see something like:

✅ Saved Mad Libs Stories:

-- Story 1 --
Class: 6A, Name: Ayesha, Story Number: 1
Passage: Once upon a time in Karachi...
--------------------
-- Story 2 --
Class: 7B, Name: Ali, Story Number: 2
Passage: The dragon flew over Lahore...
--------------------

If no stories exist yet:

No stories found yet!

If the file doesn’t exist:

⚠ File 'Shahzain_stories.csv' not found. Make sure you've saved some stories first!


---

2. Running the Saver (optional)

If you want to create a story-saver script, here’s an example:

import csv

filename = "Shahzain_stories.csv"

def save_story(class_name, name, story_number, passage):
    fieldnames = ["Class", "Name", "Story Number", "Passage"]
    
    try:
        with open(filename, mode='a', encoding='utf-8', newline='') as file:
            writer = csv.DictWriter(file, fieldnames=fieldnames)

            # Write header only if file is new
            if file.tell() == 0:
                writer.writeheader()

            writer.writerow({
                "Class": class_name,
                "Name": name,
                "Story Number": story_number,
                "Passage": passage
            })

        print("✅ Story saved successfully!")

    except Exception as e:
        print(f"❌ Error saving story: {e}")

# Example use
save_story("6A", "Shahzain", 1, "This is Shahzain’s first learning machine story!")

Run it:

python stories_saver.py


---

⚡ Error Handling

FileNotFoundError → If the CSV file doesn’t exist yet.

Empty File → Prints No stories found yet!.

Corrupted File → Gracefully prints error instead of crashing.



---

🎨 Customization

Change the filename by editing:

filename = "Shahzain_stories.csv"

Add new fields (e.g., "Date", "Teacher") by updating fieldnames.

Change output style by formatting the print() section.



---

📌 Example Project Flow

1. Teacher runs stories_saver.py to save stories.


2. Students run stories_loader.py to read saved stories live in class.


3. If file is missing → message tells them no stories are available.


4. New stories keep appending, so the file grows over time.




---

🧑‍💻 Contributing

Pull requests are welcome!

If you’d like to improve formatting, add new features (like live timers ⏳ or random auto-stop stories 🎲), feel free to fork and submit PRs.


---

📜 License

This project is open-source under the MIT License – modify, and share, but is not free of copywriting.


---

✍️ Author

Shahzain Pirzada

Creator of Shahzain’s Learning Machine Stories Saver
