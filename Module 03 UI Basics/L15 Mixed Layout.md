## L2-5: Mixed Layout with Column and Row

You can mix the Column and Row together, and here is one example:

Example how to make a card using Column and Row.

<img src="https://lh5.googleusercontent.com/SCRZ1cxzMZVeOfxEfdRcZPOHXiSovCqtTphC-wmdsd2AHF4-NyxadQ-91rkkB7B9f2oJJ236AEW5CWQ2M6oML2RKhYAELj_vCohyfvruGAJZiNzGH_K5AyyhbEdIixQWFIKRachj" alt="img"  />

**Flutter image link**: https://lh4.googleusercontent.com/dgPwnzPmPnq_qjPug57-I78OZzRgQZZoeZrr45ZhIgbFKJRcQDbTH38Mbmp7KzKQm4nslWe75T0yUIw7y0WNWVz9weBOCHIXKNmA6efomJumUQUD5wKjNj5qQAwnJfoSdWc-guCv

**Text Description**: Flutter is an open-source UI software development kit created by Google. It is used to develop applications for Android, iOS, Windows, Mac, Linux, Google Fuchsia and the web. The first version of Flutter was known as codename \"Sky\" and ran on the Android operating",textAlign: TextAlign.center,)

### Widget Tree:

![img](https://lh6.googleusercontent.com/hlXSMUY3_jp-XoGBk2rYVcqVhkNlK-s_9NRduujQCHDrUmiHMnuzNXTN3vUzqSxOkhbdjko-2fA-lJW_Od0pFyvMegxfRRAUHIwRcJWwvewGAHoGRMA8-ryJfRFNVdJXunl8uWNi)

Code to the above example:

````dart
Container(
  color: Colors.white,
  margin: EdgeInsets.all(10),
  height: 300,
  child: Row(
    children: <Widget>[
      Expanded(
        flex: 5,
        child: Column(
          children: <Widget>[
            Text("Flutter"),
            SizedBox(height: 10,),
            Flexible(
              child: Text(
                "Flutter is an open-source UI software development kit 	created by Google. It is used to develop applications for Android, iOS, Windows, Mac, Linux, Google Fuchsia and the web. The first version of Flutter was known as codename \"Sky\" and ran on the Android operating",textAlign: TextAlign.center,)
            ),
            SizedBox(height: 10,),
            Row(
              mainAxisAlignment: MainAxisAlignment.spaceBetween,
              children: <Widget>[
                Row(
                  children: <Widget>[
                    Icon(Icons.star, size: 10,),
                    Icon(Icons.star, size: 10,),
                    Icon(Icons.star, size: 10,),
                    Icon(Icons.star, size: 10,),
                  ],
                ),

                Flexible(child: Text("170 Reviews")),
              ],
            )
          ],
        ),
      ),
      Expanded(
        flex: 8,
        child: Image(
          image: NetworkImage("https://lh4.googleusercontent.com/dgPwnzPmPnq_qjPug57-I78OZzRgQZZoeZrr45ZhIgbFKJRcQDbTH38Mbmp7KzKQm4nslWe75T0yUIw7y0WNWVz9weBOCHIXKNmA6efomJumUQUD5wKjNj5qQAwnJfoSdWc-guCv"),

        ),
      )
    ],
  ),
),
````





