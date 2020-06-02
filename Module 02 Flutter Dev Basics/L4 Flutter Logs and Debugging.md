## L4: Watch the Logs 

Different from a regular programming language, mobile development has a lot of output. For Flutter development, you need to watch the **Run** tab very often to see errors or message.

![img](https://lh3.googleusercontent.com/aEYvwSm_-nJRikwASHuhiLFMHzB8SDG1RS9HVDbhwzk9kLgLO6u2qMm1cBj6KAiy1-Dvf1-kh2nrDR6agB-32vbr2SSONJy9-1vI21Ywf0Xm7HEcX-MCeeD2Bv7a2x_l0qErtfLn)

This log window is your friend. It helps you to debug. 

In order to show sometime here, you can use the `print` statement. For instance, you can add one line of code in the `_incrementCounter` method in `main.dart` file:

```dart
void _incrementCounter() {
    setState(() {
      // This call to setState tells the Flutter framework that something has
      // changed in this State, which causes it to rerun the build method below
      // so that the display can reflect the updated values. If we changed
      // _counter without calling setState(), then the build method would not be
      // called again, and so nothing would appear to happen.
      _counter++;
    });
    print("Counter is increased by 1");
  }
```

Then, run the app and click on the floating button to see if you can find the log printed. 

![img](https://lh5.googleusercontent.com/60l45GlLTi33QiEN0IUhoPT6NXPFkg96XpEOI3QaU-kChc5lBsrtd0_ISBUJFCi9KVALUTyYQNZvj3GDzF-bwwq1HSVF7EUYaK3slHftIHB-cXxGiShavfF_XvEJPiw6lk81dXy6)

In the future, you can always use `print()` to debug.



