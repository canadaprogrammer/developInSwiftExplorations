# Develop in Swift Explorations

## Values

### Constants and Variables

- ```swift
    // Declaring a constant
    let placeOfBirth = "New Jersey"

    // Declaring a variable
    var currentLocation = "New Jersey"

    // Assigning a new value to a variable
    currentLocation = "California"
  ```

- In most ways, constants and variables are the same:
  - Both use the same rules for names
  - Both associate a name with an assigned value
  - Both have a specific type
- The difference is:
  - The value of a constant cannot be changed after it's first assigned.
  - The value of a variable can be changed after it's first assigned.
- Values declared with let are constants, and can’t be changed once a value is assigned. These values are called immutable.
- Values declared with var are variables, and can be assigned new values over time. These values are called mutable.
- A mutable value can be used as part of an assignment statement to itself: score = score + 10.
- Compound assignment operators allow mutable values to be updated: score += 10.
- Using constants and variables in the correct places helps make your code safer and easier to understand.
- Error Indicator
  - The normal error indicator is a red circle with a white x in it.
  - But an error indicator having an idea how to fix the error on Xcode is a red circle with a white dot in it.
    - a Fix-it will fix errors in your code, but the fix might not be what you meant to do.
    - The Fix-it is trying to be helpful, but it could be suggesting that you make something mutable that you wanted to stay immutable.
- special string syntax for long text

  - ```swift
      let manyLineString =
      """
      This is a long string.
      It can be interpolated \(1) or any number of times. You don't have to escape "quote marks."

      And it can contain empty lines, like the one above.
      Just use three quotes on their own lines to open and close it.
      """
    ```

### Build a PhotoFrame App

1. Create a new Xcode project.
   1. iOS section > App > Next
   2. Product Name: PhotoFrame, Interface: Storyboard, Language: Swift > Next
   3. Select a location to save > Create
2. The simulator may appear large on your screen. You can make it smaller by choosing Window > Physical Size.
3. Xcode Workspace
   - <img src="./resources/images/xcode_workspace.png" alt="Xcode Workspace" width="400" />
   - Toolbar
     - To check the project's status
     - To hide and show the other window areas
     - To build and run your app from the big "Play" button
   - Navigator
     - To move around your project; select file to open in the editor by clicking it
   - Editor
     - To edit your project files; source code, user interface items, or app configuration
   - Inspector
     - To find out more details about the item currently selected or displayed in the editor
     - Especially to edit user interface files in Interface Builder
4. Add a Photo
   1. Select Asset on teh navigator area.
   2. Drag in image files
5. Edit the Storyboard
   1. Open the storyboard by selecting `Main` from the list of files in the project navigator.
   2. Change the Device.
      1. Click the Devices icon at the bottom of the window and select iPhone 13 Pro.
   3. Select the main view.
      1. Click anywhere in the scene to select its main view.
      2. In the Document Outline to the left, you'll notice that the View Controller Scene expands to show the items it contains, and the View item is highlighted.
   4. Show the Attributes inspector.
   5. Adjust the background color.
   6. Run you app
6. Adding a Frame
   1. Open the Object library, type `UIView`
   2. Drag `View` in the center of the view controller.
   3. Resize to make the view large enough to display your photo.
   4. In the Attributes Inspector, select the menu next to Background, select Custom, and choose a color from the color picker.
7. Adding and Configuring an Image View
   1. Open the Object library, type `image`
   2. Drag `Image View` into the frame view.
   3. Resize the image view until the frame behind it is the right width.
   4. In the Attributes Inspector
      1. Choose the image you added earlier at the top of the inspector.
      2. Select Content Mode to Aspect Fill.
         - <img src="./resources/images/photo_frame.png" alt="Photo Frame" width="200" />

### Design For People

## Algorithms

### Get Started With Algorithms

- An algorithm is a set of instructions for accomplishing a task.
- There are three essential building blocks in all algorithms: `sequencing`, `selection`, and `iteration`.
- Sequencing
  - Arranging instructions in order is called sequencing, and it's one of basic techniques for creating an algorithm.
  - Swift uses sequencing as it executes your code line by line and from top to bottom.
- Selection
  - Selection lets you describe multiple paths through your algorithm.
  - By using selection, you can examine the conditions at the time your code runs and your program will proceed along one of many possible paths.
- Functions
  - In Swift, you use functions to group instructions together and give them a name.
  - By breaking a problem into pieces, you can write functions to solve each piece independently.
  - You can combine them to solve the bigger problem.
  - The approach of grouping instructions into a unit and giving that unit a name is call `procedural abstraction`.
  - Remember, the key feature of any kind of abstraction is to hide, or encapsulate, the details of how something works.
  - After you've written and tested a function, you no longer have to think about how it works, just about what it does.
- Types
  - Swift uses the term type to describe each different kind of value.
- Parameters
  - You use parameters to define the input that goes into a function.
  - Each parameter for a function has a type.
  - By adding parameters to functions, you can make them more flexible so they can be used in a variety of situations.
- Making Decisions with Booleans
  - The yes-and-no answers are represented in Swift as "true" and "false."
  - They are known as Boolean values, named after George Boole, a 19th century mathematician.
  - The Bool type is used in Swift to represent Boolean values.

### Play with Programs

- Functions

  - Reusability is a large part of what makes functions so powerful.
  - Any identifier followed by parentheses, `()`, is a function.
  - The code between the two braces, `{...}`, is called the body of the function.
  - Nothing is displayed in the results because declaring a function only describes what the function would do if it ever run.
  - To actually run the code, you have to call the function. Typing the name of the function will call the function.
  - Decomposition: break a single long list down into multiple smaller lists.

- Types

  - String
  - Number is Int, an abbreviation of integer.
  - Swift keeps track of the type of the variable and makes sure you don't accidentally try to assign a value of a different type.
    - The value of a variable can change, but the type of the variable can't change.
  - Type Safety: Swift won't let you write code that uses types incorrectly or unexpectedly.
    - Another instance of type safety would occur if you tried to add values of different types.
  - A literal is the simplest form of expression.
  - Swift makes assumptions about what types the literals are meant to be.
    - Any value inside double quotes will be treated as a String, and a whole number will be treated as an Int.
    - Type Inference: Swift uses context clues from code to infer what type something is.
  - Check the type by holding down the `Option` key while clicking a variable.
  - You can add an extra piece of information, called a `type annotation`, to tell Swift exactly what type you want to use.
    - `let annotationDouble: Double = 20`
    - `annotationDouble` is a Double, even though there is no decimal point, because of the type annotation.
  - All type names begin with a capital letter. If there are multiple words the first letter of each word is also capitalized.
    - This is slightly different from the rules for naming constants, variables, and functions, which all begin with lower-case letters.
  - Types and capabilities can be grouped together into collections called `frameworks` or `libraries`.
    - To use a framework in your program, you have to import it like `import Foundation`.

- Parameters and Results

  - Declare: `func functionName(parameter: Type) {...}`
  - Call: `functionName(parameter: argument)`
  - Passing a value back when a function is finished is called returning a value. To declare a function that returns a value, you have to add two things to your code.
    - After your list of parameters, add a text arrow `->` and the type of value to be returned.
    - Then you have to end the body of the function with a return statement that gives that type fo value back.
    - `func functionName(parameter: Type) -> Type { ... return ...}`
    - Your function can have multiple parameters, but it can only return one value.
  - When a function does some kind of work that's unrelated to a return value, like printing to the console, the work is call a `side effect`.
    - When you name a function, it's good to somehow include the side effect in the name.
    - If a function has no return value, all of its work is considered a side effect.
    - A function that has a side effect should have a verb in the name.
  - The order that code executes in a program is called `control flow`.
  - When your code calls a function, the following line doesn't execute until after the function returns.
  - `func functionName(argumentLabel parameterName: Type) {...}`

    - ```swift
        func printHello(to name: String) {
          print("Hello " + name)
        }
        printHello(to: "Chris")
      ```

  - To declare a parameter without an argument label, you use the underscore `_` where the argument label would go.
  - In Swift, the underscore means "I don't care about this item because I'm not going to use it."

    - ```swift
        func printHelloTo(_ name: String) {
          print("Hello " + name)
        }
        printHelloTo("John")
      ```

- Making Decisions

  - Clean code
  - Conditionals are perfect opportunities to write helpful functions. If you have some decision-making code that doesn't read easily or makes things look to complicated, you can wrap it in a function and make it look like you're asking a question.

    - ```swift
        if gearWeight < totalCarryingCapacity {
            if bulkiestItemWeight < 80 {
                "Rock on."
            } else if chanceOfRain >= 0.1 {
                "Everyone quits! Looks like you've got a solo show."
            }
        } else {
            "Everyone quits! Looks like you've got a solo show."
        }
      ```

    - ```swift
        if gearWeight < totalCarryingCapacity && (chanceOfRain < 0.1 || bulkiestItemWeight < 80) {
            "Rock on."
        } else {
            "Everyone quits! Looks like you've got a solo show."
        }
      ```

    - ```swift
        func bandCanCarryGear(bandMemberCount: Int, gearWeight: Int, bulkiestItemWeight: Int, chanceOfRain: Double) -> Bool {
            let maximumTripCount = 2
            let weightPerPerson = 50
            let totalCarryingCapacity = bandMemberCount * weightPerPerson * maximumTripCount

            return gearWeight < totalCarryingCapacity && (chanceOfRain < 0.1 || bulkiestItemWeight < 80)
        }
        if bandCanCarryGear(bandMemberCount: 5, gearWeight: 650, bulkiestItemWeight: 60, chanceOfRain: 0.05) {
            "Rock on."
        } else {
            "Everyone quits! Looks like you've got a solo show."
        }
      ```

- BoogieBot

  - Functions are the way programmers group blocks of work together.
    - A function is reusable, which saves on reading and typing.
    - A function can be understood on its own, so you don't have to think of every single step.
    - If a function is changed, the changes apply everywhere the function is used.

- Data Visualization

### Build a QuestionBot App

- Rather than running the app several times as you develop your code, you can use a playground to get your question answerer up and running more quickly.
- You can see multiple results instantly, and there's no need to return.
- Once you're happy with your code, you'll use it to replace the existing code segment in QuestionBot.

#### Building Your Function

- QuestionAnswerer.playground

  - ```swift
      import Foundation
      func responseTo(question: String) -> String {
          let lowerQuestion = question.lowercased()

          if lowerQuestion.hasPrefix("hello") {
              return "Why, hello there"
          } else if lowerQuestion.hasPrefix("where are the cookies?") {
              return "In the cookie jar!"
          } else if lowerQuestion.hasPrefix("where") {
              return "To the North"
          } else if lowerQuestion.hasPrefix("can i") {
              return "Yes, you can"
          } else if lowerQuestion.contains("your name") {
              return "My name is QuestionBot."
          } else if lowerQuestion.contains("what time") {
              return "\(Calendar.current.component(.hour, from: Date())):\(Calendar.current.component(.minute, from: Date()))"
          } else {
              if lowerQuestion.count % 2 == 0 {
                  return "Thank you for asking, but I have no idea."
              } else {
                  return "Please ask it tomorrow."
              }
          }
      }

      responseTo(question: "Hello there")
      responseTo(question: "Where are the cookies?")
      responseTo(question: "Where should I go on holiday?")
      responseTo(question: "Can I have a cookie?")
      responseTo(question: "Should I go?")
      responseTo(question: "What time is it?")
    ```

#### Updating the App

- common problems:
  - **The app runs but you don't see the answers** you were expecting. This is probably because you pasted the function in the wrong place. Perhaps it was in the wrong file, or in the wrong place in the correct file.
  - The app doesn't build with an error that reads **Unexpected non-nil return value in void function**. You probably pasted the function body code from the playground into the wrong function in the project.
  - The app doesn't build with an error that reads **Invalid redeclaration of responseTo(question:)**. This means you have two functions with the same name in the same area of the code - not allowed because it isn't clear which function should run when called.
  - The app doesn't build with an error that reads **Expected declaration**. You may have inadvertently replaced the entire function, declaration and all, with only the body of the function from your playground, or you pasted the function body into the wrong place.
  - The app doesn't build with an error that reads **Missing return in a function expected to return 'String'**. You probably pasted an entire function inside another one.
  - The app doesn't build with an error that reads **Closure expression is unused** or **Expressions are not allowed at the top level**. You probably pasted the body of your function into a file without any context - with no `func` keyword.
  - The app doesn't build with an error that reads **Use of unresolved identifier 'MyQuestionAnswerer'**. You probably replaced the entire `struct MyQuestionAnswerer` with the `responseToQuestion` function or its body.

#### Customizing the Interface

- Open the Main.storyboard, and make sure the Attributes inspector is visible.
- Background Color
  - Select View under View Controller, and use the Background attribute to choose a different color.
- Robot Head
  - Select the Robot Head label under Stack View
  - Using the Text attribute in the inspector, change the emoji to a different character.
  - Press `Ctrl + CMD + Space` to bring up the emoji picker.
- Welcome Message
  - Select Response Label in the Document Outline and change the opening text.
  - Pressing `Ctrl + Return` to add a new line if you need one.

### Design an Experience

- Design isn't just about how a product looks and feels; it's also about how it works.
- A crucial step in designing successful computing innovations is understanding the people who will use the innovation.
- When your design incorporates diverse perspectives, it will improve the experience for all users.
- Apple has four key principles around designing for user privacy:
  - Request consent when your app needs personal data.
  - Be transparent about how personal data will be used.
  - Give the user control over their personal data and protect the personal data you collect.
  - Use the minimum amount of personal data required.

#### Plan

- You need to consider how your main screens will look. Refer back to your design mood board for inspiration, and sketch a few screens.
- <img src="./resources/images/initial_idea.png" alt="Initial Idea" width="500" />
- Show how a user will move through the screens - a storyboard.
  - You can create a storyboard by organizing the screens in a flowchart and indicating the graphic elements that enable users to make choices within the app.
  - <img src="./resources/images/storyboard.png" alt="Storyboard" width="500" />

#### Create a User Experience Flowchart

- Take photos or screenshots of your screens and add them to Keynote.
- The flowchart should show how a user can move through your app based on the choices they make.
- Annotate your storyboard to explain key features of the app, and highlight the accessibility features you've incorporated.
- Apple provides [resources](https://developer.apple.com/accessibility/) to support developers to build accessible apps.

#### Review and Iterate

- Simplification is a key idea in the app design process.
- If you're very clear about purpose, you can simplify your design so your app fits seamlessly into the flow of the user's activity.
- Share your storyboard with your peers or mentors.
  - As they explore your app design, encourage them to ask you How? Why? and What if? questions. You can record their responses or annotate your storyboard with their queries and ideas.
  - With a partner, take turns examining each other’s designs through the lens of someone who has a disability. (You can consider four broad categories: vision; hearing; physical and motor; and learning and literacy.)
  - Each of you should adopt a specific persona and explain your requirements when using an app. Then work through the app and give feedback from that person’s point of view. Together, identify ways you could improve the app to make it more inclusive.
- App design is an iterative process, and identifying problems and issues can be seen as an opportunity rather than a setback. If you need to, return to the brainstorming phase and use your new insights to revise your app idea. Great apps are the product of extensive ideation, exploration, testing, and revision.

## Organizing Data

### Get Started With Organizing Data

#### Instances, Methods, and Properties

- Types enable you to understand what each value in your code represents.
- Type safety in Swift ensures that you use values of the right type in the right place.
- Types can also define or describe the attributes and behaviors of a particular kind of thing - in other words, what a type is, or knows (its attributes), and what it does (its behaviors).
- In Swift, the attributes of a type are called `properties`, and its behaviors are called `methods`.
- Even though the type describes the properties and methods of a particular kind of thing, each concrete example of the type is a separate, independent instance of the type.

#### Lists and Arrays

- In Swift, such a collection is called an array.
- An array is a collection of individual instances of just one ypte.
- Each instance in the array is called an element.
- Each element in an array has a unique index, which identifies its location in the array respective to the first element, which is always located at index 0.

#### Algorithms: Iteration

- In algorithms, repeating the same swquence of steps multiple times is known as iteration.
- In Swift, as well as all other programming languages, iteration is critical building block of algorithms.
- Remeber - algorithms have three basic building blocks: sequencing, selection, and iteration.

#### Loops

- The term for iteration in most programming languages, including Swift, is a loop.
- A loop defines a code segment that will be repeated - its body - and a determination for when to exit the loop.

#### Working With Arrays - Searches

- It can be very useful to apply a function to every item in an array, but what if you just wanted to perform that function on one particular item?
- You would need to find that item's location in the array - its index - and specify that you were performing the function on the item at that location.
- Finding an item in an array (or determining that it's not there) is called searching, and there are multiple algorithms for performing a search on an array.
- Linear search
  - It isn't as efficient as binary search because it works by evaluating the items in the list one after the other - which means it might have to evaluate the entire list before it finishes.
- Binary search
  - The approach works by successively splitting finding the middle element and comparing the sought value to the middle element.
  - If the value is greater, the first half of the list can be eliminated.
  - If the value is less, the second half can be eleminated.
  - If the value is equal to the middle element, the algorithm has found the value in the list.
- Binary searches are more efficient that linear searches, especially with large amounts of data, but require that the data be in sorted order.

#### Defining Your Own Types With Structs

- In Swift, you can create types of your own that group lots of attributes together.
- A very common way to create a new type in Swift is to define a `struct`.
- When you make your own struct, you define properties that represent all the attributes of the thing they represent.
- In the definition of your struct, you'll also probably include methods to perform useful tasks.

### Play with Complex Data

#### Experiment with Organizing Your Code

##### Code - Instances, Methods, and Properties

###### Instances

- You can create and use different instances of a given type.
- Each instance has its own set of property values, and each instance can perform behavior independent of other instances.
- Creating an Instance
  - You've created almost every instance by typing a literal value directly into code.
  - The exception was in the Types playground, where you used `Date()` to create a value holding the current time.
  - `Date()` looks a lot like a function, but with an important difference: It uses a type name instead of a name beginning with a lowercase letter.
  - You use an initializer to create a new instance of a particular type.
  - Only a few types, like String, Bool, and Int, can be created using literals, but every type has at least one initializer.
  - Even types you've been creating using literals have initializers.
  - You'll often want to provide more information when you create an instance.
  - Many types have initializers with parameters to let you do this:
    - `let oneHourLater = Date(timeIntervalSinceNow: 3600)`
    - This initializer gives you a Date that is a number of seconds from the current time.
  - Initializers and functions are similar in some ways:
    - They can have parameters or no parameters at all.
    - You call them the same way, by passing in required argument values.
  - They also have differences:
    - You use the name of the type when calling an initializer.
    - An initializer returns a new instance of its type.

###### Methods

- Functions can be defined as part of a type.
- These functions are called instance methods, or just methods.
- String has many instance methods, which are used for common operations.
- It's often useful to know if a string begins with another string. The method `hasPrefix()` can answer this question.
  - The method is declared like this: `func hasPrefix(_ prefix: String) -> Bool`
  - The method `hasPrefix()` has a String parameter, which is the prefix you want to test, and returns a Bool.
  - Instance methods are called by using a period (.) after the instance, followed by the method call:
    - `introduction.hasPrefix("It was")`
    - This is known as calling a method on the instance. You've called hasPrefix() on introduction.

###### Methods and Type Safety

- Type safety still applies when you're using instance methods. hasPrefix is a String instance method, so you can't use it without an instance.
- You also can't use an instance method on an instance of the wrong type. You can only use methods that are part of, or members of, a particular type.

###### Properties

- Each instance has one or more pieces of associated information. These values are known as properties.
- It's often useful to know if a string contains any characters at all. The property `isEmpty` answers this question.
- The property is declared like this: `var isEmpty: Bool { get }`.
  - It is marked `var` because the property value could change if the string contents change.
  - The `{ get }` indicates you can only get the value of this property, but you can't set it.
  - This is also called a `read-only` property.
- Properties are called by using a period (.) after the instance, followed by the property name:
  - `something.isEmpty`
- The same type safety rules apply for properties as with methods.

###### Properties Versus Methods

- Variable Versus Function
  - The different between a method and a property is similar to the difference between a function and a variable or constant.
  - A variable is useful for **referring to a value** that you can access when required. Similarly, a property provides a way to get or set a value that's part of an instance. Each instance can have a different value for that property.
  - A function is useful for **providing behavior** that can be repeated as needed. A method works in the same way, providing behavior specific to that instance.
- Arguments
  - If the work you want to perform needs extra information, then it must be a method, since you can't pass arguments to a property.
  - That means `hasPrefix()` must be a method, because you need to pass in the prefix you're testing for.
- Side Effects
  - If the work has side effects, things that happen that aren't related to the return value, then it's a method.
  - For example, String has a method, `removeAll()`, which empties the string.
- Values
  - Properties are for getting values from an instance and for setting values on an instance. Properties don't do any additional work.
- Methods and properties help to break down the complexity of a large program by putting related pieces of information (properties) and work to be done (methods) together in a single self-contained package (an instance).
- The are significant advantages to using methods and properties over top-level functions(not contained in anything else) and variables:
  - Putting the capabilities of a type together with the type itself makes the code easier to understand.
  - Autocompletion works mach better: Autocompletion only supplies the methods that can apply at the point your're typing. If all methods were top-level functions, then whenever you started typing, every function in the system would show up.
  - Documentation is much easier to organize and find: How would you classify all the top-level functions that could do something with a string, or a number? What if a function dealt with both? How would you search this documentation?

###### APIs, Revisited

- The instance methods and properties of a String are the API(Application Programming Interface) of the String type.
- If you can sort-of-remember the name of a method or property, you can just start typing an dXcode will offer you autocompletion suggestions.
- APIs also come with documentation to help you learn about them and see how they should be used.
- One of the most important skills you'll develop as a programmer is how to find and understand things in documentation.
- Option + Click a type, method, or property and it will show you useful information.
- You can find the same information using the Quick Help inspector.
- To view this, make sure the utilities are is visible, by choosing View > Inspectors > Show Quick Help Inspector from the menu.
- Whenever your cursor is positioned, the Quick Help inspector will tell you about the code at that point.

###### Classes and Structs

- As you build apps in Swift, you'll work with instance of both structs and classes. Both provide a way to define types in Swift.
- Structs and classes have may similarities:
  - Both has instances
  - Instances are created with an initializer
  - Both can have methods
  - Both can have properties

##### Arrays and Loops

###### Arrays

- Array have two key features
  - The items in the array are all the same type.
  - The items in the array are in a specific order.
- In Swift, a list is called an array. It's an important data abstraction - a way to think about a concept, such as a list, as a unit without having to think about all its individual elements.
- Arrays, like all data abstractions, help you to simplify your code by providing solutions.
- Array literals are lists of items, separated by commas, with the whole thing inside square brackets:
  - `let devices = ["iPHone", "iPad", "iPod", "iMac"]`
- Each item in an array has an index, starting with the first item at zero. You can get the value that's stored at a particular index by putting the index in square brackets after the array name.
- If you ask for an item hat is not in the list, you can cause a serious program error.
- You can find out the number of items in array using the `count` property, which is an `Int`.
- Array is a type, but an array type in Swift also includes the type of the values in the array.

###### Array - Loops

- Swift has a built-in way to let you run code for each item in an array. It's call looping or iterating through the array.
- To run code for each item in an array, you can use a `for <variable name> in <array> { body }` loop.
- You can assign a whole different mutable array of items, but you can't change the type of items the array holds.
- To create a mutable empty array that will hold strings, do this: `var list = [String]()`.
- Once you've created the array, there are several ways to add items to it.
  - `list.append("Banana")`
  - `list.insert("Strawberry", at: 0)`
    - You can add an item at a specific index using the insert instance method. As with everywhere you use an index, it has to be within the array or the program will crash.
  - `list += ["Plum"]`
- There are also several ways to remove items from mutable arrays.
  - `let someNumber = numbers.remove(at: 2)`
    - You can remove items using the index. The index has to be within the array.
    - The `remove(at:)` method returns the item you have removed.
  - `let firstNumber = numbers.removeFirst()` and `let lastNumber = numbers.removeLast()`
    - You can remove the first item using `removeFirst()`.
    - Using `removeFirst()` or `removeLast()` on an empty array will cause an error.
  - `numbers.removeAll()`
    - You can remove everything using `removeAll()`.
    - This doesn't return anything.
- In Swift, the part of the statement [0] is called a `subscript`.
- With a mutable array, you can use the subscript to set the value at an existing index, replacing the value that is already there.
  - `flavors[0] = "Chocolate"`
- You can replace values in a mutable array using subscripts, you can't add or remove things.

##### Structures

###### Modeling Data

- In general, the types of data that an app deals with are known collectively as its model, or sometimes more verbosely, its data model.
- If you have information as arrays, you'd need to access the differnt arrays using the same index.
- It would be better to have data instead of arrays. The term for this higher-level concept is data abstraction.
- One way to create a new type in Swift is to define a structure, often called a struct.
- As a data abstraction, a struct provices some distance between the abstract properties of a data type, and its concrete representation.
  - Its name should begin with a captial letter. Property names should begin with lower case letter.
- Using data abstraction can result in a program that is easier to develop and maintain.
- An array is a kind of struct and you can make your own structs mutable or immutable.
- To make the properties of your custom structs mutable there are two things you need to do:

  - In the definition of the struct, declare any changeable properties using var.
  - Assign the struct to a variable, not a constant.

  - ```swift
      /* arrays */
      let songTitles = ["Ooh yeah", "Maybe", "No, no, no", "Makin' up your mind"]
      let artists = ["Brenda and the Del-chords", "Brenda and the Del-chords", "Fizz", "Boom!"]
      let durations = [90, 200, 150, 440]
      let song3 = "\(songTitles[2]) by \(artists[2]), duration \(durations[2])s"

      /* data */
      struct Song {
          let title: String
          let artist: String
          let duration: Int
          var rating: Int
      }
      let song = Song(title: "No, no, no", artist: "Fizz", duration: 150, rating: 0)
      song.rating = 4
    ```

###### Computed Properties

- A Song has a duration property, measured in seconds. But it would also be useful to ask a song for its duration as a string formatted in minutes and seconds.
- To solve this, you could have two properties, minutes and seconds, but then you would need to perform a calculation to find out the total duration.
- Alternatively, you could have three properties - minutes, seconds, and duration - but it would be easy to create a struct with inconsistent data, where the duration value didn't add up to the right number of minutes and seconds.
- A better approach to the problem would be to calculate the formatted string from the duration value.
- For properties that can be calculated on demand, you can add a computed property to the struct like this:

  - ```swift
      struct Song {
        let title: String
        let artist: String
        let duration: Int

        var formattedDuration: String {
          let minutes = duration / 60
          let seconds = duration % 60
          return "\(minutes)m \(seconds)s"
        }
      }
      let song = Song(title: "No, no, no", artist: "Fizz", duration: 150)
      song.formattedDuration
    ```

- A computed property is declared as a `var`, since it could change depending on the rest of the struct. The rest of the declaration consists of a name, a type annotation, and then some code in braces, which has to return a value of the correct type. You can access the computed property just like any other.
- Not that inside the definition of formattedDuration, the property duration is accessed without dot notation.
  - Within the code of a struct, you can access its own properties directly by their names, without using the dot.
- Computed properties are a further example of the power of structs to create data abstraction. Instead of using separate functions outside the struct, you can put related functionality right alongside the data it relies on.
  - Code that uses the struct can simply use these new properties without needing to know how they work.

###### Functions

- Your own types can be passed into or out of functions, just like built-in types.

  - ```swift
      struct Rectangle {
        let width: Int
        let height: Int
      }

      func inRectangle(_ rectangle: Rectangle, biggerThan rectangle2: Rectangle) -> Bool {
        let areaOne = rectangle.width * rectangle.height
        let areaTwo = rectangle2.width * rectangle2.height
        return areaOne > areaTwo
      }

      let rectangle = Rectangle(width: 10, height: 10)
      let anotherRectangle = Rectangle(width: 10, height: 30)
      isRectangle(rectangle, biggerThan: anotherRectangle)
    ```

- This works, but there are a couple of issues:
  - The two arguments to the function are a lot of code to read in one line, which makes it harder to understand.
  - The function is available everywhere is a program, but you only need it when dealing with rectangles.
  - If you don't know there is an isRectangle() function, it is difficult to find using autocompletion.

###### Instance Methods

- A instance method is written as part of the struct definition, and so it can directly access the properties witin the instance.
- Just like the methods on built-in types, the methods you define are called using the instance name, then a dot, then the name and arguments of the method.

  - ```swift
      struct Rectangle {
        let width: Int
        let height: Int

        func isBiggerThan(_ rectangle: Rectangle) -> Bool {
          let areaOne = width * height
          let areaTwo = rectangle.width * rectangle.height
          return areaOne > areaTwo
        }
      }

      let rectangle = Rectangle(width: 10, height: 10)
      let anotherRectangle = Rectangle(width: 10, height: 30)
      rectangle.isBiggerThan(anotherRectangle)
      anotherRectangle.isBiggerThan(rectangle)
    ```

##### Enums and Switch

###### Enumerations

- In Swift, you can use an enumeration to represent a group of related choices. Each choice is called a case.
- You can define your own enumeration types, just as you can define your own structs.
- An enumeration is usually called by its abbreviation, `enum`.
- The name of an enum starts with a capital letter, like all other type names.
- The name of a case starts with a lower-case letter, like the names of properties and methods.
- The name of the enum should be singular, because the value refers to only one choice, not many choices.
- One benefit of an enum is it limits the choices to one of its cases.
- If Swift already knows what type to expect, you can skip the enum name. Since you've already specified the type of an enum instance, you can leave out the enum name when assigning a value.
- Whenever you have a restricted group of related values in your code, it might be good to think about using an enum.

  - ```swift
      enum LunchChoice {
        /*
        * case pasta
        * case burger
        * case soup
        */
        case pasta, burger, soup
      }

      /* let choice = LunchChoice.soup */
      var choice: LunchChoice
      choice = .soup
    ```

###### Enums and Functions

- Enum values can be used as parameters or return values for functions, just like any other type.
- When calling a function, you know that you have to pass in an enum. Autocompletion will tell you exactly what the options are.
- You can't pass in anything that's not on the list, so you'll always get what you're looking for.

  - ```swift
      func cookLunch(_ choice: LunchChoice) -> String {
        if choice == .pasta {
          return "🍝"
        } else if choice == .burger {
          return "🍔"
        } else {
          return "🍲"
        }
      }
      chookLunch(.burger)
    ```

###### Switch

- Apparently if statements aren't great fit when dealing with enums.
- The switch statement looks very much like the enum declaration.
- Since the type of the enums is known, you can use the dot syntax and leave out the type name.
- Switch statements have a special feature: they must be exhaustive. This means a switch statement must exhaust every possibility of the value being checked. With an enum, you can use a different case to handle every possible value.

  - You're not allowed to write a switch statement that doesn't cover every case.
  - This feature prevents you from accidentally missing a value.
  - It also alerts you if you update the definition of an enum without updating any switch statements that use it.

  - ```swift
      switch choice {
      case .pasta:
          "🍝"
      case .burger:
          "🍔"
      case .soup:
          "🍲"
      }
    ```

- If you add a default case to your switch statement, you won't get an error when you add new cases to the enum.

  - ```swift
      enum Quality {
          case bad, poor, acceptable, good, great
      }

      let quality = Quality.good

      switch quality {
      case .bad:
          print("That really won't do")
      case .poor:
          print("That's not good enough")
      default:
          print("OK, I'll take it")
      }
    ```

- A default case might cause you problems later on if you add new cases to the enum.
- The switch statement will use the default case for your new value, which may not be what you wanted.
- Instead, you can match several values in the same case:

  - ```swift
      switch quality {
      case .bad:
          print("That really won't do")
      case .poor:
          print("That's not good enough")
      case .acceptable, .good, .great:
          print("OK, I'll take it")
      }
    ```

- Switch statements can work with strings and numbers. Since it's impossible to have an exhaustive list of all string and number values, switch states using these types require a default case.

  - ```swift
      let animal = "cat"

      func soundFor(animal: String) -> String {
          switch animal {
          case "cat":
              return "Meow!"
          case "dog":
              return "Woof!"
          default:
              return "I don't know that animal!"
          }
      }
      soundFor(animal: animal)
    ```

###### Enum Methods and Properties

- You can define methods and properties in an enum.

  - ```swift
      enum Suit {
          case spades, hearts, diamonds, clubs

          var rank: Int {
              switch self {
              case .spades: return 4
              case .hearts: return 3
              case .diamonds: return 2
              case .clubs: return 1
              }
          }

          func beats(_ otherSuit: Suit) -> Bool {
              return self.rank > otherSuit.rank
          }
      }

      let oneSuit = Suit.spades
      let otherSuit = Suit.clubs
      oneSuit.beats(otherSuit)
      oneSuit.beats(oneSuit)
    ```

- The `self` keyword is used in methods and computed properties and refers to the instance that is being asked for the property value.

###### Wrapping Up

- Enumerations are used when you want to represent one of a group of related values. Each possible value is called a case.
- When you create an enum, you're making a new type. Instance of that type can only have values matching one of the specified cases.
- Using enums can make our code easier to read and write, because it's always clear what the possible values are and what they mean.
- Because switch statements must be exhaustive, you must handle every possible value. To handle any values that haven't been specified, you can use a default case.

##### Testing Code

- Your code doesn't always work as you expect it to. Testing your code will help you detect errors and make sure that your functions behave predictably.

###### Limits of Integers

- What's a `UInt8`?

  - All numbers in Swift occupy a fised number of bits. The standard Int type occupies either 32 or 64 bits, depending on the computer that's running it.
  - The `UInt8` type occupies only 8 bits.
  - The "U" in `UInt8` stands for "unsigned." An unsigned integer is always positive.
  - Values of `UInt8` range from 0 to 255.
  - When tried to store 500, a number outside of the range, the console should print "Integer literal '500' overflows when stored into 'UInt8'."
    - Overflow is the result of trying to store a number that won't fit into the number of bits available.
  - Overflow can also occur when you reach the bank's limitations as your program executes. In that case, you'll see an "EXC_BAD_INSTRUCTION" or "EXC_BREAKPOINT" error in the console.

  - ```swift
      /// Represents a piggy bank that holds only pennies.
      class PiggyBank {
          private var pennies: UInt8 = 0

          init() {
              pennies = 0
          }

          /// Returns the balance of the bank.
          func balance() -> UInt8 {
              return pennies
          }

          /// Deposits pennies into the bank.
          /// - Parameter pennies: the number of pennies to deposit.
          func deposit(pennies: UInt8) {
              self.pennies += pennies
          }

          /// Withdraws pennies from the bank.
          /// - Parameter pennies: the number of pennies to withdraw.
          /// - Note:
          func withdraw(pennies: UInt8) {
              self.pennies -= pennies
          }
      }

      var bank = PiggyBank()
      /// won't fit into the numver of bits available
      //bank.deposit(pennies: 500) // Integer literal '500' overflows when stored into 'UInt8'

      /// reach the limitations
      //bank.deposit(pennies: 100)
      //bank.deposit(pennies: 100)
      //bank.deposit(pennies: 100)  // error: Execution was interrupted, reason: EXC_BREAKPOINT (code=1, subcode=...).
                                    // The process has been left at the point where it was interrupted, use "thread return -x" to return to the state before expression evaluation.

      /// assign a negative number ot a UInt8
      //bank.deposit(pennies: 50)
      //bank.withdraw(pennies: 100) // error: Execution was interrupted, reason: EXC_BREAKPOINT (code=1, subcode=...).
                                    // The process has been left at the point where it was interrupted, use "thread return -x" to return to the state before expression evaluation.
    ```

###### Documentation

- When you write functions and methods, you should document them to indicate the conditions under which they function.
- Documentation has important uses:
  - To identify appropriate values for testing
  - To make your code easier for yourself and others to read and understand
  - To serve as the basis for published documentation of an API
  - To capture your thought process as you code
- If you use the special comment format `///`, you'll get a bonus: Swift will automatically create and format documentation that you can access by Option-clicking the item - just as you do for internal types.
- There are `/// - Note:`, `/// - Parameter` as the above

###### Testing

- When you test a function, you should choose a range of values - including some that extend beyond the limits that the function expects.
- Make some test cases below by creating instances of PiggyBank and calling the two methods with values that should produce valid results - as well as some tests that should cause it to crash.
- Verify valid results by comparing the method call to the expected output as demonstrated. (You'll have to comment out the tests that crash your code in order to have them alongside other tests.)

  - ```swift
      // Test a legal deposit amount
      var bank1 = PiggyBank()
      bank1.deposit(pennies: 100)
      bank1.balance() == 100 // this should be true
    ```

###### Limitations of Floats

- Like Int and UInt8, Swift floating point types are represented in a fixed amount of space - a Double occupies 64 bits.
- As a result, some floating point numbers can't be represented exactly; they can only be approximated.
- The problem is that Doubles don't always work the way you expect them to.
- Some strange behavior is going on. Due to the limitations of the Double type, the Dobule literal 8.95 isn't acutally that value when it's represented in the computer.
- So when you multiply it by 100, the result isn't 985.0, but 894.000....
- Doubles have other limitations as well, such as those that only crop up in addition operations.
- A quick solution is to multiply the value by 100, then round to the nearest cent - before converting it to an Int.

  - ```swift
      let price = 8.95
      let priceInPennies = price * 100
      let roundedPriceInPennies = priceInPennies.rounded() // Produces a new Double
      let integerPriceInPennies = Int(roundedPriceInPennies) // Produces an Int
    ```

##### Processing Data

- Outside the confines of their code, developers have to contend with the real world in all its messiness. When it comes to data, you'll often find that what you get isn't what you expect. Sometimes the data is incomplete, or needs to be combined with other data sources to present a complete picture. Even when a data set is complete, sometimes it has to be cleaned in order to use it properly. Cleaning data can take several forms depending on its nature. (And knowing how to code makes it possible to clean data much more efficiently than if you had to do it by hand.)
- Cleaning data is one way to transform it—to make it more suitable to the task at hand, or more accurate. Beyond transformation, you can translate data by putting it into new contexts or deriving extra information from it.
- You've also learned the value of using third-party code and the proper way to cite it. If you hadn't paid attention before, you'll surely notice now that the license on this page (and on the final page of all the playgrounds in this course) is identical to the license for the third-party code you used.

#### Creatively Apply Your Thinking

##### Pixel Art

- All the pages in this playgournd have a `display` instance whose type is `PixelDisplay`. The properties and methods of PixelDisplay provide the interface to your low-resolution graphics display.
- The display on this page has 64 pixels in an 8-by-8 grid. Pixel coordinates are zero-indexed, just like arrays.
- The `setPixel(x:y:color)` method addresses an individual pixel at the specified x and y location. The Color type has several predefined values, as shown below.
  - display.setPixel(x: 5, y: 2, color: .purple)
- You can also create any color you want. The Color type has three initializers. You can use autocompletion to discover them.
  - `display.setPixel(x: 7, y: 7, color: Color(red: 0.8, green: 0.2, blue: 0.7))`
- The `backgroundColor` property of PixelDisplay controls the display color.
  - `display.backgroundColor = .cyan`
- Create functions to make horizontal and vertical lines.

  - ```swift
      func hline(x: Int, y: Int, length: Int, color: Color) {
          for i in 0 ... length - 1 {
              display.setPixel(x: x + i, y: y, color: color)
          }
      }
      func vline(x: Int, y: Int, length: Int, color: Color) {
          for i in 0 ... length - 1 {
              display.setPixel(x: x, y: y + i, color: color)
          }
      }
      /* rectangular block */
      hline(x: 1, y: 1, length: 5, color: .purple)
      hline(x: 1, y: 4, length: 5, color: .purple)
      vline(x: 1, y: 1, length: 4, color: .purple)
      vline(x: 6, y: 1, length: 4, color: .purple)
    ```

- Create a block function to create a rectangular block of color.

  - ```swift
      func block(x: Int, y: Int, width: Int, height: Int, color: Color) {
          for i in 0 ... height - 1 {
              hline(x: x, y: y + i, length: width, color: color)
          }
      }
      block(x: 1, y: 1, width: 12, height: 4, color: .purple)
    ```

- Fill Speed
  - If you created a large enough block, you might observe the playground reaching its speed limit.
  - `batchSetPixels` takes an array of Pixels rather than just one. By passing in many pixels as an array, you're setting them all at one - rather than one at a time.
  - But that would only partially solve the problem - you'd still have to draw your lines one after the other.
  - A better solution is to modify your block function to use a nested loop.
- Composition

  - In computer graphics, it's common to repeat graphic elements.

  - ```swift
      func block(x: Int, y: Int, width: Int, height: Int, color: Color) -> [Pixel] {
          var pixels = [Pixel]()
          for x in x ... x + width - 1 {
              for y in y ... y + height - 1 {
                  pixels.append(Pixel(x: x, y: y, color: color))
              }
          }
          return pixels
      }
      display.batchSetPixels(block(x: 18, y: 10, width: 2, height: 4, color: .blue))
    ```

- `wait()` method pauses the display for a given period of time before continuing to the next drawing operation.
- Along with the `clear()` method, `wait()` enables you to create animations by drawing something, pausing for a beat, clearing the screen, and updating the drawing.

  - ```swift
      var frameTime = 1.0 / 30.0

      for i in 0...39 {
        display.setPixel(x: i, y: 5, color: .purple)
        display.wait(time: frameTime)
        display.clear()
      }
    ```

##### Password Security

- Develop an algorithm that rejects insecure passwords.
- The first step is to ensure that the user hasn't chosen one of the most commonly used passwords, which hackers are sure to try first.
  - It's the easiest way to get into somebody's account, since it doesn't require a sophisticated algorithm to make a guess.
  - Use the `contains()` method of Array to make sure the use hasn't chosen one of common passwords.
    - `commonPasswordsArray.contains("password")`
  - Display a message informing the user whether or not they've chosen a secure password.
- If you require the user to include nonalphabetic characters, there'll be some amount of randomness even if the password includes dictionary words.
- You might also require passwords be a minimum length.
  - The longer a password, the longer it takes for a hacker to try all possibilities.
- Use the following rules:
  - At least 16 characters
  - At least one regular letter
  - At least one digit
  - At least one punctuation character
- Even though `String` and `Array` are different types, they're both sequences - that is, they arrange their elements in a particular order.
  - The `for...in` loop has a special superpower: It works on any sequence, not just an arrays.
  - Use the `contains()` method to check each character against the predefined arrays above to see whether they satisfy one of the rules.
  - After checking all the characters in the password, write a final conditional statement to check whether you found at least one of each type of required character.
- You could also verify that a password contains at least one uppercase letter and one lowercase letter.
  - To detect whether a character is uppercase, use the `isUppercase` property.
- Another useful check is making sure that the password doesn't contain the username

###### Brute-Force Guessing

- A brute force attack is a hacking method that uses trial and error to crack passwords, login credentials, and encryption keys.
- The `passwordIsCorrect(_:)` function acts as the login form for a hypothetical web service, returning true when the correct password is entered.
- The `guessPasswordOfThreeCharacters(containing:)` function uses a brute-force algorithm to try all possible combinations of the characters passed in.
- This function is used below to guess a purely numeric password. Looking at the results bar on the right, you'll notice it guesses the correct password on the 124th try.

  - ```swift
      import Foundation

      func passwordIsCorrect(_ password: String) -> Bool {
        return password = "123"
      }

      let digits = "0123456789"
      let punctuation = "!@#$%^&*(),.<>;'`~[]{}\\|/?_-+= "
      let lowercaseAlphas = "abcdefghijklmnopqrstuvwxyz"
      let uppercaseAlphas = lowercaseAlphas.uppercased()

      func guessPasswordOfThreeCharacters(containing characters: String) {
        var password: String = ""

        for a in characters {
          for b in characters {
            for c in characters {
              password = String(a) + String(b) + String(c)
              if passwordIsCorrect(password) {
                print("Found password: \(password)")
                // The return statement below means that the function exits
                // early when the password is guessed, rather than executing
                // all loops to completion.
                return
              }
            }
          }
        }
      }

      guessPasswordOfThreeCharacters(containing: digits)
    ```

- Because the algorithm contains a loop within a loop within a loop, you have to multiple the iterations of each loop to calculate the number of times the innermost statement.
- As a result, the algorithm is exponential. It operates as a function of the power of the number of possible characters.
- Exponential algorithms are said to run in unreasonable time because the time for them to run grows very quickly as the problem size increases.

##### Visualization Revisited

- The API you'll learn now will strip away that layer so you can work directly with the items underneath.

###### Pie Charts, Revisited

- The new API for pie charts exposes two new types: PieWedge and PieChartView.
- The `PieWedge` struct gives you several ways to create visual effects with pie charts. It has the following properties:
  - `proportion`: The percentage of the pie occupied by the wedge, expressed as a Double.
  - `color`: The color of the wedge. You can use any one of the following values.
    - .black, .blue, .brown, .cyan, .darkGray, .gray, green, .lightGray, .magenta, .orange, .purple, .red, .yellow
  - `scale`: The radius of the wedge relative to the pie's natural radius, expressed as a Double.
    - Less than 1.0 will make the wedge smaller than normal-sized wedges, and greater than 1.0 will make the wedge larger (typically the desired effect).
  - `offset`: The distance a wedge lies from the center of the pie, relative to the size of the wedge.
    - An offset of 0 keeps the wedge at the center of the pie. An offset of 1.0 moves the center point of the wedge to where its outer edge would be.
- The `makePieChart()` function creates an instance of a `PieChartView` named `pieChartView`.
  - `PieChartView` has one property named `wedges`, which is an array of PieWedge instances.
  - Assign an array of wedges to this property, or use the `append()` method of Array to add them one at a time.
  - `PieChartView` also has a property named `labelDisplayStyle`, how labels are displayed, expressed as a `WedgeLabelDisplayStyle`.
    - `WedgeLabelDisplayStyle` is an enum with the following cases:
      - `interior`: Labels are displayed inside wedges.
      - `exterior`: Labels are displayed just outside wedges.
      - `none`: Wedges aren't labeled.
- `makePieChart()` also creates a `key` named `keyView`.
  - It's an instance of `ChartKeyView`, which has a `keyItems` property.
  - `keyItems` is an array of `ChartKeyItem` instances.
  - `ChartKeyItem` has the following properties:
    - `color`: The color swatch displayed in the key. You can use any of the color of the wedge.
    - `name`: The text to display expressed as a String.
- Until now, you've specified colors, each starting with a period, from a fixed list. But that list represents a very small view into a full-featured type named Color.
- For fine-grained color control, Color has several useful initializers that take arguments of type Double.
  - init(red:green:blue:alpha:) takes Double arguments, each ranging from 0 to 1, indicating the amount of red, green, blue, and alpha that make up the color. Alpha is the transparency level: An item with partial transparency (any alpha less than 1.0), will blend its color with the colors of items underneath it.
  - init(hue:saturation:brightness:alpha:) also takes Double arguments. Instead of mixing the red, green, and blue primary colors, this initializer defines a color by its hue, saturation, and brightness, as well as its transparency. Hue ranges from red, at 0.0, through the rainbow spectrum of orange, yellow, and so on, until wrapping back to red at 1.0. Saturation, from 0.0 to 1.0, describes how much "color" is in the color. (Imagine the difference between a bucket of pure red paint versus a bucket of white paint with one drop of red paint added to it.) Brightness is the relative darkness or lightness of a starting color, from black at 0.0 (no brightness) to white at 1.0 (full brightness).
  - init(white:alpha:) is a quick way to create grayscale colors with just two Double arguments.
- All of the color names you've been using, such as .red and .black, are just properties of the Color type.
- They're special properties called class properties because they're part of the type itself, not part of its instances.
- So instead of creating a new Color and then referring to its black property, you just refer to the black property of Color itself, like this: Color.black.
  - Because Swift is good at type inference, you can leave out the Color part of this expression when using it in a place where a Color is expected.
  - For example, the color property of both PieWedge and ChartKeyItem is actually a Color.

###### Bar Charts, Revisited

- The new API exposes an instance of `BarChartView` named `barChart`.
- There's also a `ChartBar` struct which is used to specify the bars themselves.
- `ChartBar` has the following properties:
  - `length`: The size of the bar, expressed as a `Double`.
  - `color`: The color of the bar, expressed as a `Color`.
- `BarChartView` has several properties:
  - `bars`: An Array of ChartBars.
  - `yAxisMinimum`: The minimum value of the Y axis, expressed as a `Double`.
  - `yAxisMaximum`: The maximum value of the Y axis, expressed as a `Double`.
  - `seriesLabels`: An Array of Strings to display labels along the X axis with equal spacing.
- As with the pie chart, you'll also get an instance of `ChartKeyView` called `keyView`.
- You also have three new enums that control the look of horizontal axis labels on your bar charts. They are:
  - `AxisLabelGravity`
    - `top`: Axis labels will align to the top of the axis label area.
    - `bottom`: Axis labels will align to the bottom of the axis label area.
  - `AxisLabelAttachment`
    - `beginning`: Axis labels will attach at the beginning of the text.
    - `end`: Axis labels will attach at the end of the text.
  - `AxisLabelDistributionStyle`
    - `endToEnd`: Axis labels will be distributed evenly, with the first and last labels aligning with the beginning and end of the axis, respectively.
    - `centeredIntervals`: Axis labels will be distributed evenly with equal amounts of space around them.
  - Three new properties of BarChartView let you control the look of the series labels:
    - `seriesLabelGravity`, of type AxisLabelGravity
    - `seriesLabelAttachment`, of type AxisLabelAttachment
    - `seriesLabelDistributionStyle`, of type AxisLabelDistributionStyle

###### Plots, Revisited

- This version of the API also exposes some new types to help you create better scatter plots.
- `PlotView` displays your plot data. `makePlot()` creates an instance named `plotView`.
- The plot data is a series of `PlotPoint` - instances, stored as an array in the points property.
- `PlotView` has the following properties:
  - `points`: An Array of PlotPoints.
  - `yAxisMinimum`: The minimum value of the Y axis, expressed as a Double.
  - `yAxisMaximum`: The maximum value of the Y axis, expressed as a Double.
  - `xAxisMinimum`: The minimum value of the X axis, expressed as a Double.
  - `xAxisMaximum`: The maximum value of the X axis, expressed as a Double.
- `PlotPoint` has the following properties:
  - `x`: The X coordinate of the point, expressed as a Double.
  - `y`: The Y coordinate of the point, expressed as a Double.
  - `color`: The color of the point, expressed as a Color.
  - `size`: The size of the point, expressed as a Double.
- You can use several initializers to create a PlotPoint instance.
- The color will default to .black and the size to 5: `init(x:y:f)`
- The size will default to 5: `init(x:y:color:)`
- You specify all properties: `init(x:y:color:size:)`
- As with pie charts and bar charts, you'll also get an instance of `ChartKeyView` called `keyView`.
- How do you want the data points on your scatter plots to display? PlotPoint actually has one final property, named symbol, of type Symbol.
- `Symbol` is an enum with the following cases:
  - `circle`
  - `square`
  - `diamond`
  - `triangle`
  - `x`
  - `plus`
- You can use these new properties by calling a new initializer for PlotPoint: 'init(x:y:color:size:symbol:)'
- PlotView itself gains the capability to draw lines with a new property named mode of type PlotMode. The PlotMode enum has the following cases:
  - `pointsOnly`
  - `linesOnly`
  - `pointsAndLines`
- The `pointsOnly` mode is the default. If you use either of the other two modes, the PlotView will make groups of all points that have the same color and symbol, sort each group by increasing x value, and draw lines between points in each group.
- `ChartKeyItem` also gains a symbol property and a new initializer, `init(color:name:symbol:)`, so you can display symbols in the chart key to match those in your plot.

### Build a BouncyBall App

#### Putting Shapes on the Screen

- You'll build the entire game from simple elements—flat shapes that can interact with user touches and a physics simulation. The code that implements the game engine is written in the Shape and ShapeScene files. (In turn, the game engine is written on top of the standard iOS SpriteKit API, which is much more complex and powerful.)
- Open GameCode.swift.

  - This is the only file you'll need to modify as you create the game.
  - The setup function is called once when the app launches—without it, your app won't compile.
  - Below import Foundation, add `let circle = OvalShape(width: 150, height: 150)`
    - `OvalShape` is a type that describes an oval with a width and a height.
  - Inside the `setup()` function

    - ```swift
        setup() {
          circle.position = Point(x: 250, y: 400)
          scene.add(circle)
        }
      ```

    - It defined its location on the screen using x and y coordinates.
    - The position of any shape in the scene is the location of its center.
    - The `scene` instance represents the white area on the screen where the game takes place.
