## L6: Creating Your Own Screen

Based on the provided sample, you can now learn how to create your own screen. 

The best practice is to create a new file for each new screen. For example, I will name it as `mynextscreen.dart`

![img](https://lh3.googleusercontent.com/BKwUHrZrh0mfKYm2pLx667T3sI76YP0hQz9OujXvr3QJWbDJ_prbhz6YuPC1Zc2tepVwQWKKOJoiIdOOcSWXn2Jd4t0cAf8EzVZ07qcCwb3_x2LXDdykGyuVfod7YY9G41uw3or3)



Then, let's copy the 2 classes and modify it by changing the names.

```dart
import 'package:flutter/material.dart';

class MyNextPage extends StatefulWidget {
  MyNextPage({Key key, this.title}) : super(key: key);

  final String title;

  @override
  _MyNextPageState createState() => _MyNextPageState();
}

class _MyNextPageState extends State<MyNextPage> {
  int _counter = 0;

  void _incrementCounter() {
    setState(() {
      _counter++;
    });
    print("The counter has been increased by 1. " + _counter.toString());
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text(widget.title),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            Text(
              'Welcome to My Next Screen',
            ),
            Text(
              'This is another line of text',
            ),
            Text(
              '$_counter',
              style: Theme.of(context).textTheme.display3,
            ),
          ],
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: _incrementCounter,
        tooltip: 'Increment',
        child: Icon(Icons.add),
      ),
    );
  }
}
```

Please note that you cannnot have two classes with the same name.

If you are done, please create one more page as a practice. In the future, whenever you need to create a new screen, just use the same approach - copy and paste.

I know that there are a lot of things that don't make sense right now, but we are just focusing on the structure of the app, and you will master the code soon. 