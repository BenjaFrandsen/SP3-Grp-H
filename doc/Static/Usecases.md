UC1 StartProgram:
The system loads Users from the user file and Media from the data files, then shows the start menu (UC2 UserHandler)

Rainy day:
The user file does not exist: The system starts with an empty list of Users.
An error occurs while loading data/content. The system tells the user the content cannot be loaded and ends the program.

UC2 UserHandler:
A prompt is shown consisting of two options: Login or create user 
If login is selected, the system prompts for a username and a password. If they match a User, the system sets the current user. 
If create user is selected, The system prompts for a username and a password and creates the User, saves it to the file and shows the main menu (UC3).

Rainy day:
The username is taken or a field is empty/wrong username/password. The system shows a message and prompts again.

UC3 MainMenu:
The system shows the options: search by title (> UC4), SearchByCategory (> UC5), ShowWatched (> UC6), ShowSaved (> UC7), LogOut (> UC12).

Rainy day:
Invalid input, the system shows “Invalid choice” and shows the menu again.

UC4 SearchByTitle:
The user types a title. The system shows a numbered list of matching Media, and the user chooses one (> UC8).

Rainy day:
No matches: The system shows “No results found” and returns to the main menu.

UC5 SearchByCategory:
The system shows all Categories, and the user chooses one. The system shows all Media in that Category, and the user chooses one (> UC8).

Rainy day:
The Category is empty: The system shows a message and returns to the list of Categories.

UC6 ShowWatched:
The system shows the current User’s watched list, and the user chooses a Media (> UC8)

Rainy day:
The list is empty: The system shows a message and returns to the main menu.

UC7 ShowSaved:
The system shows the current User’s saved list, and the user chooses a Media (> UC8).

Rainy day:
The list is empty: The system shows a message and returns to the main menu.

UC8 ChooseMedia:
The system shows the Media details and the options: play (> UC9), save (> UC10), remove (> UC10) or back (> UC3).

Rainy day:
Invalid number, the system shows “Invalid choice” and prompts again.

UC9 PlayMedia:
The system shows "Title is now playing...” and adds the Media to the watched list.

Rainy day:
??? hvad sker der her? altså hvis Media er en series - Media not found

UC10 MediaSaveHandler:
Based on user input, the system either adds the Media to the saved list and confirms with a message.
or the system removes the Media from the saved list and confirms with a message.

Rainy day:
The Media is already on the list: The system shows a message, and nothing is added.
The Media is not on the list: The system shows a message, and nothing is removed.

UC12 Logout:
The system stores the User data and closes the program.

Rainy day:
The system tells the user that the data was not saved.



flyt userhandler og main menu