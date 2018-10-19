

Application Type: iOS Mobile App

------------------------------------------------------------------------------------------------------------------------------------------

Technology Used: Xcode, Swift

Xcode is an integrated development environment for macOS containing a suite of software development tools developed by Apple for developing software for macOS, iOS, watchOS, and tvOS. We will use it to build an iOS App alone.

Swift is a general-purpose, multi-paradigm, compiled programming language developed by Apple Inc. for iOS, macOS, watchOS, tvOS, and Linux. Swift is designed to work with Apple's Cocoa and Cocoa Touch frameworks and the large body of existing Objective-C code written for Apple products. We will be using the Swift language to develop our app in the Xcode IDE. We could have used Objective C but Swift is preferred since its style conventions allow it to be read out loud as plain English. Communicating Swift code to peers is linguistically easier and it is very similar to Python in terms of cleanliness.

------------------------------------------------------------------------------------------------------------------------------------------

How To Run & Compile

Step 1) Own a Mac! Native iOS Mobile Applications are built in the XCode IDE using
either Swift or Objective-C as the language to code the app. XCode can be found
under the Mac App Store. Native iOS Mobile Applications cannot be executed/tested
on any other operating system except macOS.

If you do not own a Mac, check out the
following video link for a mini demo: https://www.youtube.com/watch?v=h4fEwhGbicY&feature=youtu.be


Step 2) Open Xcode and Select "Open Existing Project".

Step 3) Go to this project's directory titled Productivity and click on Productivity.xcodeproj
because a project in Xcode is a .xcodeproj folder

Step 4) Now the project is open in Xcode! Run the app by clicking the play button at the top
left corner of Xcode!

------------------------------------------------------------------------------------------------------------------------------------------

What Features Were Implemented?

•    Add, delete a to-do item.
•    Click on any to do item to see all details.
•    Edit a currrent to do item.
•    History page of old completed/uncompleted items to save deleted to do's.
•    History of old items cannot be edit. This page serves as a back log.
•    Marking items as completed as opposed to only removing them.
•    When an item is marked as completed, it moves to the History page.
•    When an item is deleted, consider it an uncompleted item. This item also moves to the History page.
•    History page marks completed items in blue text and uncompleted in red text
•    If an item in History is set to completed, but user sets this item to uncompleted, move this item back to the Current To Do’s Page for convenience
•    Sorts current To Do items by Start Date in ascending order
•    Persistence: if you close and re-open the application, your current list and history list come back. Data is stored locally on iPhone!
•    Single user. No database.

------------------------------------------------------------------------------------------------------------------------------------------

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

Why A Class? Classes allow us to make our data representation more abstract. Classes also allow us to make many instances of the same type while maintaining different states across these instances.
    This allows for an array of type class toDoItem.

------------------------------------------------------------------------------------------------------------------------------------------

Specifics:
How many views/screens?

Home view to see all Current To-Do’s
Buttons? Add and Edit
Swipe left on item to delete it, swipe right to mark as completed

Add View to insert new To Do’s
Add allows user to fill in item fields and confirm/reject action.
Verify that all required fields are filled! Only name and dates are required.
Add Button to complete process and Back Button to return without adding anything

Edit View
Edit an existing item and confirm the changes.
Verify that all required fields are filled! Only name and dates are required.
Update item’s new position in Current To-Do list
Edit Button to complete process and Back Button to return without editing anything

History View
See all past items. Completed are in Blue, incompleted in Red.
None of these items can be edited!
These items can also be clicked on to view their details

To Do Details View
View all fields for a given To Do Item
Allow for an Edit button to segue to Edit View
Back Button to return to previous screen







