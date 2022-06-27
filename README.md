# Assignment 03
## Requirements
- The application must be implemented in C++ and use layered architecture.
- Provide tests and specifications.
- Have at least 10 entities in your memory repository.
- Validate all input data.
- Handle the following situations:
    - If an entity that already exists is added, a message is shown and the entity is not stored. You must decide what makes an entity unique.
    - If the user tries to update/delete an entity that does not exist, a message will be shown and there will be no effect on the list of entities.
- Use STL vectors and algorithms.
- Store data in a text file. When the program starts, entities are read from the file. Modifications made during program execution are stored in the file. Implement this using the iostream library. Create insertion and extraction operators for your entities and use these when reading/writing to files or the console.
- Use exceptions to signal errors.
- When the application starts, the user should choose the type of file between CSV or HTML. Depending on the type, the application will save the list in the correct format.
- Add a new command, allowing the user to see the events.
- Create a graphical user interface using the Qt framework. 
- Create a graphical representation of the data in your application.
- Add multiple undo and redo functionality for the add, remove, and update operations. Implement this functionality using inheritance and polymorphism. You will have Undo and Redo buttons on the GUI, as well as a key combination to undo and redo the operations.
- Show the contents of the events using a table view. You must use the Qt View/Model components (QTableView). Create your own model – a class which inherits from QAbstractTableModel. This window will be opened from your GUI main window.

## Problem Statement
## Life After School
Lectures, seminars and labs ... school in general must be taken seriously; BUT so must be your social life and leisure time. To manage the latter and be always informed about the interesting events happening in your city you will implement a software application. The application can be used in two modes: administrator and user. When the application is started, it will offer the option to choose the mode.\
**Administrator mode:** The application will have a database which holds all the interesting events in your area. You must be able to update the database, meaning: add a new event, delete an event and update the information of an event. Each **Event** has a `title`, a `description`, a `date and time`, a `number of people` who are going and a `link` towards the online resource containing the event. The administrators will also have the option to see all the events in the database.\
**User mode:** A user can create a list with the events that he/she is interested in. The application will allow the user to:
- See the events in the database for a given month (if there is no month given, see all the events, ordered chronologically), one by one. When the user chooses this option, the data of the first event (title, description, date and time, number of people who are going) is displayed, and the event is opened in the browser (e.g. Facebook event).
- If the user wants to participate in the event he/she can choose to add it to his/her events list. When this happens, the number of people who are going to the event increases (for the event in the repository).
- If the event seems uninteresting, the user can choose not to add it to the list and continue to the next. In this case, the information corresponding to the next event is shown, and the user is again offered the possibility to add it to his/her list. This can continue as long as the user wants, as when arriving to the end of the list of events for the given month, if the user chooses next, the application will again show the first event.
- Delete an event from the list. When the user deletes an event from his/her list, the number of people who are going to the event decreases.
- See the list of events the user wants to attend.
