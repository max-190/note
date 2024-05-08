# note - a terminal based note-taking application
Take notes and retrieve them on the fly with an easy-to-use syntax.

## Installation
Clone git repository and copy the `note` file to `~/.local/bin`. Use 
`chmod +x note` to give the program execution rights.

## Usage
### Retrieving notes
There are multiple ways to display the notes currently stored in the application.

Use `note`, without any arguments, to display a list of all groups with its corresponding notes.

Use `note [index]`, where `[index]` is the number given to a group, to display the notes only in the aforementioned group.

Use `note groups` to show a list of only the groups, and the number of notes contained within each group.

### Adding groups
To add a new group to the list of groups, use `note group [group_name]`. The group will be appended to the end of the list.

### Removing groups
To remove a group, use `note rm [group_index]`, where `[group_index]` is the number given to the group. This will remove the group with all its notes. This command will prompt the user with a warning, since this action cannot be undone.

Note that using this command on *other notes*, it is not removed; the list of notes is simply emptied.

### Adding notes
To add a note to an existing group, use `note [group_index] [message]`, where `group_index` is the number of the group and `[message]` the note to be added to the group. The note need not be enclosed in single or double quotes.

By default, a note is appended to *other notes*, a list of notes that are not linked to any group. To do this, use `note [message]`, so without `[group_index]`.

### Removing notes
To remove a note, use `note rm [group_index].[note_index]`, where the specified note may look like `2.3`. This example means that the third note will be removed from the second group. Note that a group will not be removed when all notes are individually removed from the group.

This action will **not** prompt the user with a warning.

## TODO
- Make better parser
- Add config to json to select preferences, such as bypassing checks.