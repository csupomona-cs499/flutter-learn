## L8: Screen Navigation



Now that you have a new screen, how do we get to the new screen? You will need to know how to navigate the app using Navigator. The official document can be found at here:

[https://flutter.dev/docs/cookbook/navigation/navigation-basics](https://flutter.dev/docs/cookbook/navigation/navigation-basics)

This is a great example about the Navigation. The main code you need is:

```dart
Navigator.push(
    context,
    MaterialPageRoute(builder: (context) => NewScreenPage()),
);
```

You need to replace the `NewScreenPage` with the screen name you want to use. In addition, please make sure to add the `title` attribute. Thus, your code might be like this:

```dart
Navigator.push(
    context,
    MaterialPageRoute(builder: (context) => MyNextPage(title: 'My Next Page')),
);
```

For instance, if you want to click on the Floating Button and go to the next screen, the code will be:

```dart
floatingActionButton: FloatingActionButton(
        onPressed: () {
          print("The floating button is clicked.");
          // open a new screen page (page)
          Navigator.push(
            context,
            MaterialPageRoute(builder: (context) => MyNextPage(title: 'My Next Page')),
          );
        },
        tooltip: 'Increment',
        child: Icon(Icons.add),
), // This trailing comma makes auto-formatting nicer for build methods.
```

If you want to try to get a new Button to trigger it, let's add a new Button first.

A simple form of Button in Flutter is called FlatButton, you can find the details at: [https://api.flutter.dev/flutter/material/FlatButton-class.html](https://api.flutter.dev/flutter/material/FlatButton-class.html)

Here is an example of the FlatButton:

```dart
FlatButton(
  onPressed: () {
    /*...*/
  },
  child: Text(
    "Flat Button",
  ),
)
```

You can put this into the MyHomePage class, just like:

```dart
  @override
  Widget build(BuildContext context) {
    // This method is rerun every time setState is called, for instance as done
    // by the _incrementCounter method above.
    //
    // The Flutter framework has been optimized to make rerunning build methods
    // fast, so that you can just rebuild anything that needs updating rather
    // than having to individually change instances of widgets.
    return Scaffold(
      appBar: AppBar(
        // Here we take the value from the MyHomePage object that was created by
        // the App.build method, and use it to set our appbar title.
        title: Text(widget.title),
      ),
      body: Center(
        // Center is a layout widget. It takes a single child and positions it
        // in the middle of the parent.
        child: Column(
          // Column is also a layout widget. It takes a list of children and
          // arranges them vertically. By default, it sizes itself to fit its
          // children horizontally, and tries to be as tall as its parent.
          //
          // Invoke "debug painting" (press "p" in the console, choose the
          // "Toggle Debug Paint" action from the Flutter Inspector in Android
          // Studio, or the "Toggle Debug Paint" command in Visual Studio Code)
          // to see the wireframe for each widget.
          //
          // Column has various properties to control how it sizes itself and
          // how it positions its children. Here we use mainAxisAlignment to
          // center the children vertically; the main axis here is the vertical
          // axis because Columns are vertical (the cross axis would be
          // horizontal).
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            Text(
              'You have clicked the button this many times!!!',
            ),
            Text(
              'This is another line of text',
            ),
            FlatButton(
              onPressed: () {

              },
              child: Text(
                "Click on Me",
              ),
            ),
            Text(
              '$_counter',
              style: Theme.of(context).textTheme.display3,
            ),
          ],
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: () {
          print("The floating button is clicked.");
          // open a new screen page (page)
          Navigator.push(
            context,
            MaterialPageRoute(builder: (context) => MyNextPage(title: 'My Next Page')),
          );
        },
        tooltip: 'Increment',
        child: Icon(Icons.add),
      ), // This trailing comma makes auto-formatting nicer for build methods.
    );
  }
```

Then, you can try to put the same navigator code to the `onPressed` method, and see what happens. The final code will look like this:

```dart
  @override
  Widget build(BuildContext context) {
    // This method is rerun every time setState is called, for instance as done
    // by the _incrementCounter method above.
    //
    // The Flutter framework has been optimized to make rerunning build methods
    // fast, so that you can just rebuild anything that needs updating rather
    // than having to individually change instances of widgets.
    return Scaffold(
      appBar: AppBar(
        // Here we take the value from the MyHomePage object that was created by
        // the App.build method, and use it to set our appbar title.
        title: Text(widget.title),
      ),
      body: Center(
        // Center is a layout widget. It takes a single child and positions it
        // in the middle of the parent.
        child: Column(
          // Column is also a layout widget. It takes a list of children and
          // arranges them vertically. By default, it sizes itself to fit its
          // children horizontally, and tries to be as tall as its parent.
          //
          // Invoke "debug painting" (press "p" in the console, choose the
          // "Toggle Debug Paint" action from the Flutter Inspector in Android
          // Studio, or the "Toggle Debug Paint" command in Visual Studio Code)
          // to see the wireframe for each widget.
          //
          // Column has various properties to control how it sizes itself and
          // how it positions its children. Here we use mainAxisAlignment to
          // center the children vertically; the main axis here is the vertical
          // axis because Columns are vertical (the cross axis would be
          // horizontal).
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            Text(
              'You have clicked the button this many times!!!',
            ),
            Text(
              'This is another line of text',
            ),
            FlatButton(
              onPressed: () {
                Navigator.push(
                  context,
                  MaterialPageRoute(builder: (context) => MyNextPage(title: 'My Next Page')),
                );
              },
              child: Text(
                "Click on Me",
              ),
            ),
            Text(
              '$_counter',
              style: Theme.of(context).textTheme.display3,
            ),
          ],
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: () {
          print("The floating button is clicked.");
          // open a new screen page (page)
          Navigator.push(
            context,
            MaterialPageRoute(builder: (context) => MyNextPage(title: 'My Next Page')),
          );
        },
        tooltip: 'Increment',
        child: Icon(Icons.add),
      ), // This trailing comma makes auto-formatting nicer for build methods.
    );
  }
```

If you are done, please Google and try to add the following UI elements to your screens:

1. TextField
2. RaisedButton
3. Icon

