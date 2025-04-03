Project: Personal Journal App

import datetime

journal_entries = []

def add_entry(title, content): timestamp = datetime.datetime.now().strftime("%Y-%m-%d %H:%M:%S") entry = {"title": title, "content": content, "timestamp": timestamp} journal_entries.append(entry) return f"Entry '{title}' added successfully."

def view_entries(): if not journal_entries: return "No journal entries available." return "\n".join([f"[{entry['timestamp']}] {entry['title']}: {entry['content']}" for entry in journal_entries])

def delete_entry(title): global journal_entries journal_entries = [entry for entry in journal_entries if entry["title"] != title] return f"Entry '{title}' deleted successfully."

Example Usage

if name == "main": print(add_entry("First Entry", "Today was a good day!")) print(add_entry("Second Entry", "I learned something new.")) print("\nJournal Entries:\n", view_entries()) print(delete_entry("First Entry")) print("\nUpdated Journal Entries:\n", view_entries())# NEW-Project
