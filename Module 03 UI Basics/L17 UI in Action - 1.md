## Layout in Actions

Let's use what we have learned to try the following example, in order to understand these basic usage of layout and widgets.

1. Column basic (plain usage)
2. Column with weights
3. Column with weights and items with margin
4. Row basic with weights and items with margin
5. Fixed example with Column and Row



### Example 1 : Login Example

<img src="https://lh6.googleusercontent.com/PKRH0_gyH-PPOVP5k52kt58B00Os_R609hduAooNjZ6oxiEb1Sow0GUwKI_JhmCIZYlgnW3wQWD6EMIthT-FLmMIgfZ49bbCCW9Bc6M7b4g5Bi6XaHlj4jGxU5Rnl6GLFDW_f_Vl" alt="img" style="zoom: 50%;" />

Image url: https://lh3.googleusercontent.com/Gpa6FdaHNU1aTfsb7eZYTC7BSDrSspoAN8vtKlKij8ay6oerXuNzz6wh6pxUCKT0sPf-2PtJvYVTUbDZv2avI9g8dQTVhSwgAKpNJkO7K9l12N3y_zIn18fEK-HkmyAry45uJssy

Code to Example: 

```dart
Container(
  margin: EdgeInsets.fromLTRB(100, 0, 100, 0),
  child: Column(
    mainAxisAlignment: MainAxisAlignment.center,
    crossAxisAlignment: CrossAxisAlignment.center,
    children: <Widget>[
      CircleAvatar(
        radius: 100.0,
        backgroundImage: NetworkImage("https://lh3.googleusercontent.com/Gpa6FdaHNU1aTfsb7eZYTC7BSDrSspoAN8vtKlKij8ay6oerXuNzz6wh6pxUCKT0sPf-2PtJvYVTUbDZv2avI9g8dQTVhSwgAKpNJkO7K9l12N3y_zIn18fEK-HkmyAry45uJssy"),
      ),
      Text("My App", style: TextStyle(fontSize: 50),),
      Padding(
        padding: EdgeInsets.fromLTRB(0, 10, 0, 10),
        child: TextField(
          decoration: InputDecoration(
            border: OutlineInputBorder(),
            labelText: 'Username',
          ),
        ),
      ),
      TextField(
        obscureText: true,
        decoration: InputDecoration(
          border: OutlineInputBorder(),
          labelText: 'Password',
        ),
      ),
      RaisedButton(
        child: Text("Sign In"),
        onPressed: (){},
        shape: RoundedRectangleBorder(
          borderRadius: new BorderRadius.circular(18.0),
          side: BorderSide(color: Colors.teal)
        ),
      )
    ],
  ),
),
```





