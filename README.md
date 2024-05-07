# note - a terminal based note-taking application
Take notes and retrieve them on the fly with an easy-to-use syntax.

## Installation
Clone git repository and copy the `note` file to `~/.local/bin`. Use 
`chmod +x note` to give the program execution rights.

## Usage
To get a list of all currently stored notes, use the command `note` without
any arguments.

To only get a list of notes in a certain group, use `note [group_name]`, where
`[group_name]` is the name of an already existing group.

To add a group, use `note group [group_name]`, where `[group_name]` is the desired name of the new group. 

To add a new note, use `note [note_text]`, where `[note_text]` contains the string to be added. By default, a note is added to *other notes*. To add it to a group, use `note [index] [note_text]`, where `[index]` specifies the number given to a group when notes are printed.

To remove a note, use `note rm [index]`, where `[index]` specifies the number given to a note. For example, use `note rm 2.3` to remove the third note from the second group.

To remove an entire group, use `note -[index]`, where `[index]` specifies the number given to a group.

## TODO
- Change the way *other notes* are stored, so that checks are easier.
- Add check to verify deleting groups (or individual notes).
- Add config to json to select preferences, such as bypassing checks.