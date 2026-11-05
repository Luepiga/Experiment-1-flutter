
EXPERIMENT 1 – WORKING WITH WIDGETS AND LAYOUTS
Aim
To develop a Flutter application using basic widgets and layout widgets such as
Container, Row, Column, Expanded, Card, and ListView.
Step 1 – Check Flutter installation
Open Terminal:
flutter doctor
Check whether Flutter is installed correctly.
Then check the available devices:
flutter devices
Step 2 – Create a Flutter project
flutter create widget_layout
Move into the project:
cd widget_layout
Open in VS Code:
code .
Step 3 – Run the default application
flutter run
Step 4 – Open lib/main.dart
Delete the existing code.

Create the basic Flutter application:
import 'package:flutter/material.dart';
void main() {
runApp(const MyApp());
}
class MyApp extends StatelessWidget {
const MyApp({super.key});
@override
Widget build(BuildContext context) {
return MaterialApp(
debugShowCheckedModeBanner: false,
home: Scaffold(
appBar: AppBar(
title: const Text('Student Profile'),
),
body: const Center(
child: Text('Welcome to Flutter'),
),
),
);
}
}
Step 5 – Add a Column
Replace the body with:
body: Column(
children: [
const Text('Student Name'),
const Text('Computer Science and Engineering'),
const Text('Flutter Laboratory'),
],
),
Step 6 – Add a Container
body: Column(
children: [
Container(
padding: const EdgeInsets.all(20),
margin: const EdgeInsets.all(10),
child: const Text('Student Profile'),
),
const Text('Raj'),
const Text('CSE'),
],
),

Step 7 – Add a Row
Row(
mainAxisAlignment: MainAxisAlignment.spaceEvenly,
children: const [
Icon(Icons.home),
Icon(Icons.person),
Icon(Icons.settings),
],
),
Step 8 – Add Cards
Card(
child: ListTile(
leading: const Icon(Icons.book),
title: const Text('Flutter'),
subtitle: const Text('Mobile Application Development'),
),
),
Step 9 – Add multiple items using ListView
ListView(
children: const [
ListTile(
leading: Icon(Icons.book),
title: Text('Flutter'),
),
ListTile(
leading: Icon(Icons.cloud),
title: Text('Cloud Computing'),
),
ListTile(
leading: Icon(Icons.code),
title: Text('Programming'),
),
],
),
Step 10 – Run
flutter run


Step 1 – Check Flutter installation
1. Open VS Code.
2. Click Terminal → New Terminal.
3. Select PowerShell.
4. Run:
flutter doctor


Then check available devices:
flutter devices


Step 2 – Create Flutter project
Run:
flutter create widget_layout


Move into the project:
cd widget_layout


Open in VS Code:
code .


Step 3 – Run default application
flutter run


If you want to run in Chrome:
flutter run -d chrome


Step 4 – Open main.dart
In VS Code Explorer:
1. Open the lib folder.
2. Click main.dart.
3. Delete the existing code.
4. Paste the complete code below.
Step 5 – Complete Flutter code
Copy and paste this code
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        appBar: AppBar(
          title: const Text('Student Profile'),
          backgroundColor: Colors.blue,
        ),
        body: Column(
          children: [
            Container(
              padding: const EdgeInsets.all(20),
              margin: const EdgeInsets.all(10),
              width: double.infinity,
              color: Colors.blue.shade100,
              child: const Text(
                'Student Profile',
                textAlign: TextAlign.center,
                style: TextStyle(fontSize: 20),
              ),
            ),

            const Text(
              'Raj',
              style: TextStyle(fontSize: 18),
            ),

            const Text('Computer Science and Engineering'),
            const Text('Flutter Laboratory'),

            const SizedBox(height: 20),

            Row(
              mainAxisAlignment: MainAxisAlignment.spaceEvenly,
              children: const [
                Icon(Icons.home, size: 30),
                Icon(Icons.person, size: 30),
                Icon(Icons.settings, size: 30),
              ],
            ),

            const SizedBox(height: 20),

            const Card(
              child: ListTile(
                leading: Icon(Icons.book),
                title: Text('Flutter'),
                subtitle: Text('Mobile Application Development'),
              ),
            ),

            const Card(
              child: ListTile(
                leading: Icon(Icons.cloud),
                title: Text('Cloud Computing'),
              ),
            ),

            const Text(
              'My Subjects',
              style: TextStyle(
                fontSize: 20,
                fontWeight: FontWeight.bold,
              ),
            ),

            Expanded(
              child: ListView(
                children: const [
                  ListTile(
                    leading: Icon(Icons.book),
                    title: Text('Flutter'),
                  ),
                  ListTile(
                    leading: Icon(Icons.cloud),
                    title: Text('Cloud Computing'),
                  ),
                  ListTile(
                    leading: Icon(Icons.code),
                    title: Text('Programming'),
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}


Step 6 – Save and run
Save the code:
Ctrl + S


Run the application:
flutter run -d chrome


Or use:
flutter run
