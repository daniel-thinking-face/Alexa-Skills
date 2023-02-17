# Alexa-Skills
Repository containing some code for simple Alexa skills

A small Alexa skill and corresponding API I built to track the contents of my Mother-in-law's freezer!

The outline of the app is simply to know where one can find certain items of food in the freezer.  

With the app you can:

1. **locate** items by say asking if you have any pizza. 
2. Find the **Oldest Items** in the freezer
3. **Add** an item to the freezer
4. **Remove** an item from the freezer
5. **Move** an item from one drawer to another
6. **Update** an item.  e.g. Update a packet of sausages from 6 to 3
7. **Check for Vegetarian** items.  Quickly search for those items which may be vegetarian

## The Alexa Skill Model

The Alexa Skill model consists of 2 parts.

### Interaction Model

This is where the voice commands are set with sample utterances. 

In these utterances we can leave space for *slots* which are entities we are looking to extract and act on E.g. An item of food or a freezer drawer in this case.

### Lambda Function

This is the python code that perfoms the tasks and builds the spoken response.

I had to build methods for each of the 7 operations described above.
Also had to build code to handle ambiguous situations - more than one type of item in a freezer drawer that you want to move for example.

There was also some correction code to resolve confusion when naming food - i.e. ensuring the drawer name wasn't considered part of the food name

