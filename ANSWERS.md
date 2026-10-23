REPOSITORY LINK:

LAST THREE BUILD CALLED LINES:
build() called: 4 glasses
build() called: 5 glasses
build() called: 6 glasses

OBSERVATIONS FROM THE EXPERIMENT:
Activity 2: mo error if ipagawas ang _glasses++
Activity 3: mo error if tanggalon ang 'Expanded'
Activity 5: dili mo error, naa lang medyo diff sa radius if e run na

ANSWERS:
1. What is the difference between a StatelessWidget and a StatefulWidget? Give one example of each
from this lab.
- StatelessWidget never changes after it is drawn, while the StatefulWidget can change while the app is running. Example for StatelessWidget is the Activity No.1 and for the StatefulWidget is Activity No.2

2. Why is a StatefulWidget written as two classes? What does each class do?
- To separate the widget structure from the changing data. The StatefulWidget class creates the State object, while the State class stores the changing data and updates the UI using setState()

3. In Activity 2, what happened when you changed _glasses outside setState()? Why?
- error, because it is expected to find ";" and it also says it is unnecessary empty statement

4. Looking at the Debug Console in Activity 2, when is build() called?
- The build() method is called when the screen is first displayed and whenever setState() notifies Flutter that the UI needs to update, such as when adding, removing, or resetting a glass of water

5. Explain the main axis and the cross axis of a Row and of a Column.
- In a Row, the main axis is horizontal and the cross axis is vertical. In a Column, the main axis is vertical and the cross axis is horizontal

6. In Activity 3, what happened when you removed Expanded from a StatBox? What does Expanded do?
- Error. Without Expanded, the StatBoxes no longer shared the available width equally and could cause a layout overflow. Expanded makes each box use a proportional share of the available space

7. Why do we use GridView.builder for the menu instead of a Column with many children?
- GridView.builder arranges menu items in a grid and supports scrolling. It also builds items as needed, making it more efficient for menus with many items than placing everything inside a Column

8. How do Stack and Positioned create the Best seller badge in Activity 4?
- Stack places widgets on top of one another. Positioned places the Best seller badge at a specific location, such as the top-left corner of the menu card

9. What is the difference between customizing with ThemeData and with a style on one widget? Give one example of each from Activity 5.
- ThemeData customizes the appearance of multiple widgets throughout the app, while a widget-specific style changes only one particular widget. In Activity 5, buildTheme() customizes the app theme, while RoundedRectangleBorder sets the shape of the ElevatedButton

10. When you flip the dark-mode switch in Activity 5, which widget holds the state, and how does the change reach MaterialApp?
- ThemeDemoApp holds the state through _ThemeDemoAppState and its _isDark variable. When the switch changes, _setDark() calls setState(), updating _isDark. This causes MaterialApp to rebuild and select the appropriate theme through themeMode