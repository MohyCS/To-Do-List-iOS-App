
How To Run & Compile

Step 1) Own a Mac! Native iOS Mobile Applications are built in the XCode IDE using
either Swift or Objective-C as the language to build the app. XCode can be found
under the Mac App Store. Native iOS Mobile Applications cannot be executed/tested
on any other operating system except macOS.

If you do not own a Mac, check out the
following video link for a mini demo: https://www.youtube.com/watch?v=h4fEwhGbicY&feature=youtu.be


Step 2) Open Xcode and Select "Open Existing Project".

Step 3) Go the the project's directory titled Productivity and click on Productivity.xcodeproj
because a project in Xcode is a .xcodeproj folder

Step 4) Now the project is open in Xcode! Run the app by clicking the play button at the top
left corner of Xcode!


What Features Were Implemented?

•    Add, delete a to-do item.
•    Click on any to do item to see all details.
•    Edit a currrent to do item.
•    History of old completed/uncompleted items to save deleted to do's.
•    History of old items cannot be edit. This page serves as a back log.
•    Marking items as completed as opposed to only removing them.
•    When an item is marked as completed, it moves to the History page.
•    When an item is deleted, consider it an uncompleted item. This item also moves to the History page.
•    History page marks completed items in blue text and uncompleted in red text
•    If an item in History is set to completed, but user sets this item to uncompleted, move this item back to the Current To Do’s Page for convenience
•    Sorts current To Do items by Start Date
•    Persistence: if you close and re-open the application, should your current list and history list come back. Data is stored locally on iPhone!
•    Single user. No database.

How Was A To Do Item Represented?

A class with the following attributes:

class toDoItem {
    var startDate: String
    var endDate: String
    var name: String
    var place: String?
    var note: String?
    var startTime: String  //start and end times -> military time format
    var endTime: String
    var completed: Bool

    init(startDate: String, endDate: String, name: String, place: String, note: String, startTime: String, endTime: String) {
    self.startDate = startDate
    self.endDate = endDate
    self.name = name
    self.place = place
    self.note = note
    self.startTime = startTime
    self.endTime = endTime
    self.completed = false
}

Why A Class? Classes allow us to make our data representation more abstract. Classes also allow to make many instances of the same type while maintaining different states across these instanes.
    This allows for an array of type class toDoItem.

Specifics:
How many views/screens?

Home view to see all future/pending To-Do’s
Buttons? Add and Edit
Swipe left on item to delete it, swipe right to mark as completed

Add View to insert new To Do’s
Add allows user to fill in item fields and confirm/reject action.
Verify that all required fields are filled! Only name and dates are required.

Edit View

Edit an existing item and confirm the changes.
Verify that all required fields are filled! Only name and dates are required.
Update item’s new position in To-Do list


History View
See all past items. Completed are in Blue, incompleted in Red

To Do Details View
View all fields for a given To Do Item
Allow for an Edit button to segue to Edit View







