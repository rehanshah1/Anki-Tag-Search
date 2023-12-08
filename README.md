# Anki-Tag-Search
The Python script utilizes the AnkiConnect API to interact with the Anki application. AnkiConnect is a remote API that enables communication with Anki through HTTP requests.
Constants:

ANKI_CONNECT_URL: The URL for AnkiConnect, typically set to "http://127.0.0.1:8765", assuming Anki is running locally.
Function: invoke_anki_connect

Parameters: action (AnkiConnect action), **params (additional parameters for the specified action).
Sends a POST request to AnkiConnect with the specified action and parameters.
Returns the JSON response from AnkiConnect.
Function: list_tags_in_deck

Parameters: deck_name (name of the Anki deck to analyze).
Retrieves all notes in the specified deck using the AnkiConnect action "findNotes".
Iterates through the notes and extracts their tags using the "notesInfo" action.
Prints out the unique tags found in the specified deck.
Script Execution:

The script is designed to be executed from the command line.
Replace the placeholder 'Your_Deck_Name' with the actual name of the Anki deck you want to analyze.
The list_tags_in_deck function is then called with the specified deck name.
Output:

The script outputs the list of unique tags present in the specified Anki deck.
Tags are extracted from the notes using the AnkiConnect actions, and the final list is printed to the console.
Note:

Ensure that Anki is running and AnkiConnect is installed and configured properly for the script to communicate with the Anki application.
Instructions for Use:
Save the script as a Python file (e.g., anki_tag_list.py).
Replace 'Your_Deck_Name' with the actual name of your Anki deck.
Run the script using a Python interpreter.
Review the console output to see the list of tags in the specified Anki deck.
