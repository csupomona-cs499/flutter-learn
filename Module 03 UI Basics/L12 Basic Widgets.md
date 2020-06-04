## Widget Control



### Using a Widget



#### 1. Text

```dart
Text("Hello World");
```
#### 2. Button
There are many types of button widgets in Material Design such as ButtonBar, DropdownButton, FlatButton, RaisedButton, etc. 

This is just an example to add a RaisedButton widget.

```dart
RaisedButton(
  onPressed: () {},
  child: const Text(
    'Button',
    style: TextStyle(fontSize: 20),
  );
```
#### 3. Image with URL

```dart
Image.network('https://designshack.net/wp-content/uploads/placeholder-image.png');
```

#### 4. TextField

```` dart
TextField(
  obscureText: true,
  decoration: InputDecoration(
    border: OutlineInputBorder(),
    labelText: 'Password',
  ),
)
````





> For all the other Flutter widgets, please go to https://flutter.dev/docs/development/ui/widgets to check out.

> In the beginning, it is often good to use Material design widgets: https://flutter.dev/docs/development/ui/widgets/material



### Control the Size of a Widget

We use `Container`. You can use `width` and `height` to control the size with the exact dimension.

```dart
Container(
  child: Text("Hello World"),
  width: 100,
  height: 100,
  color: Colors.blue,
)
```
#### **Output**
![img](https://lh5.googleusercontent.com/-RrNCBx67bBsuZ-LVltZqqWC9Ety8E3qR3dZWEa6p3u1Ssoc8PV3Yze1tkDPHCmUPg7-Fl7HD3qpskSp0IUfqGDsrAWwQVnG474DOmQniNyu9CWnoSSUnlbo3MUDCJaUK3q2NEnF)




### Control the Margin/Padding of a Widget

#### **Understanding Padding vs Margin** 

![img](https://lh5.googleusercontent.com/Z9YyrtYLpq5SubNaYvMDWY3P4n_QBMEwcj94tsgQGCSeg4xoyibZXkz6_vP0GQ5JpFY4rnQ5ZdW0yWJ-xr4bXXAHdLO56y8MepGBAh5cG3lnCDZasSl6jxuRu1k0li1tZJeVGD4Y)

#### **Before Adding Padding**



![img](https://lh3.googleusercontent.com/BLze9Z25Lqd0OAxoyCol7MoVxnTyW8STXE3JlKj9e6WdCJL8woUwf374BDjBqF4AKWLGqDNbip3pU9-NppZ3DzxXzJBIejW3Jm_Iv0DL6zeawyBMUJq0tb4BAqG55x8L68R04_EV)

#### **After Adding Padding**

```dart
Container(
  child: Text(
    "Hello World",
    style: TextStyle(fontWeight: FontWeight.bold , fontSize: 50)
  ),
  color: Colors.blue,
  width: 100,
  height: 100,
  padding: EdgeInsets.all(50.0),  //New code added
)
```

![img](https://lh3.googleusercontent.com/D2LaBPhaKpy7G-vp0oWlikxDU9sLNeYl8x5Wu2c0n1z2N9xLaR-J_qtGCjgQikLuhLjv3wCzhWfWoCJGSdz6A23BD9Wo_mbpdsnkU6uv3nXKzDW_1bz3gS4BT3o0dbGmOPoeco4C)



#### **Before Adding Margin**

![img](https://lh4.googleusercontent.com/kJ48fUsdU8s4TvrSTc0nj7P93v9ugdDa4QxpUZgIOo1YirYkXVXPtwjt8OO0vJfoYquuzeU2PVHxMR2lvQsqGcHRAVD5kadxF_g-5f1PesMO-dfVQYf7eGijfvRipa8EF4Ho0lKq)

#### **After Adding Margin**

```dart
Scaffold(
  body: Container(
    child: Text(
      "Hello World",
      style: TextStyle(fontWeight: FontWeight.bold , fontSize:50) 
    ),
    color: Colors.blue,
    padding: EdgeInsets.all(50),
    margin: EdgeInsets.all(50), //New code added
  ),
  backgroundColor: Colors.black, 
);
```

![img](https://lh6.googleusercontent.com/g1Padhd8_S33JPpBxUAFM5NI_c4UsTNK45g4sdktYjbY3YOHaVJ09yoR7nWMW502fwJCoGxntYYXkqORLnCxGwnB9eKwyD9hxj-lhUHyDSr0Y-rXRkhZd6oiAMMs0ObW_j3IYGQU)

#### Adding Magin and Padding to Certain Edges

```dart
Scaffold(
  backgroundColor: Colors.black,
  body: Container(
    child: Text(
      "Hello World",
      style: TextStyle(fontWeight: FontWeight.bold , fontSize:50) 
    ),
    color: Colors.blue,
    padding: EdgeInsets.all(50),
    margin: EdgeInsets.only(left:100,right:100)
    //You can choose which edges you want to put a margin on 
  ),
);
```



### **General Layout**

This is the layout to understand exactly how margin and padding are different where margin is inside the border and margin is outside the border. 

![img](https://lh3.googleusercontent.com/IGC2EK8w0vRthBdrqyrV-a7GLfSL3PtweOGV_ixlFBQFTUWSK9pJA_Jty1-cXMdqSNqZqZnik9YAClo_2REgW0GIaXrgKgCl7hTEZuv8A8dIKdksd5hvLICY1rSkWjeNG_ZF45yL)




### **Control the Alignment/Gravity of the a Widget**

Alignment of a container takes two parameter (x, y) or your can use pre-define Alignment Class.

x = 0 and y= 0 will be the center of the interface. 

Pre-defined Alignment class:

1. Alignment.bottomCenter ` The center point along the bottom edge same as  `Alignment(0.0, 1.0)

2. Alignment.bottomLeft` The bottom left corner same as `Alignment(-1.0, 1.0)

3. Alignment.bottomRight` The bottom right corner same as `Alignment(1.0, 1.0)

4. Alignment.center` The center point, both horizontally and vertically same as `Alignment(0.0, 0.0)

5. Alignment.centerLeft` The center point along the left edge same as `Alignment(-1.0, 0.0)

6. Alignment.centerRight` The center point along the right edge same as `Alignment(1.0, 0.0)

7. Alignment.topCenter` The center point along the top edge same as `Alignment(0.0, -1.0)

8. Alignment.topLeft` The top left corner same as `Alignment(-1.0, -1.0)

9. Alignment.topRight` The top right corner same as `Alignment(1.0, -1.0)

   

<img src="https://lh3.googleusercontent.com/NDfJT3DpnZDFGalSgEwiGhvXOdyZ7L_dB7gSLoXPHYac6fCIvCyToJnqHICe_l7-v5P59s4QXfFAj9X2j2paZpoCTgy9tjECtZGpwUJO8o62R6RWugGsPSwGFBBBWa4r8czLJ5fK" alt="img" style="zoom:33%;" />

Example of code:

```` dart
Container(
  child: Text(
    "Hello World",
  )
  alignment: Alignment.center,
  //alignment: Alignment(0,0),
)
  //Assume that our background is green
````

![img](https://lh6.googleusercontent.com/CzaWjJGKHs8nJFbNh1PxOT04MLMPr3zHGd_pO-683ZpKhkZrt63hJEj97JBjJRY_aAVwdbHT7nj-IpsagBZcIAqyd4FmigbTyd1TWjV7ouilCz4CKOblzd2JQcqYPrpcSdChl78V)



### **Where to Find Out the Widget Reference and Resources**

Layout widget: https://flutter.dev/docs/development/ui/widgets/layout

Text Widget: https://flutter.dev/docs/development/ui/widgets/text

Image Widget: https://api.flutter.dev/flutter/widgets/Image-class.html

Container Widget: https://api.flutter.dev/flutter/widgets/Container-class.html



