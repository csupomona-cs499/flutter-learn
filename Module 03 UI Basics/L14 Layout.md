## L14: Layout: Column and Row



### **App UI: Layout First**

Using different widgets is not hard. The harder part is managing the layout.

![img](https://lh3.googleusercontent.com/92y7xitlVKDyDOQV8akN3FytbfzOBaXrmQ0xsGKBQUc90vl_fUYw0jZmr5N-NpczmhtyjIByA-nbz8X8s1ftVyQGLOkpDoOEUt7RhUIKsO0KF54JQK9TrmAhsDtBxn1iov4N2ixG)



### Row (Horizontal Arrangement)

#### Basic usage

```dart
Row(
  children: [
    Icon(Icons.stars, size: 50.0),
    Icon(Icons.stars, size: 50.0),
    Icon(Icons.stars, size: 50.0),
  ],
)
```

#### Row - mainAxisAlignment

```` dart
Row(
  mainAxisAlignment: MainAxisAlignment.start, //modified this line of code as needed
  children: [
    Icon(Icons.stars, size: 50.0),
    Icon(Icons.stars, size: 50.0),
    Icon(Icons.stars, size: 50.0),
  ],
)
````



![img](https://lh3.googleusercontent.com/a7IFgkp-OMNcx7rdiEjbyhNfAibItOcrj7H3bE9gkaDpWfSodWUjjZVPM3QQPzFE7KWiusCFpVc-oci3tu03AaMOetdSPE21WVT3Gzwbxlq1BEo_3Kcw7XBzIf3L66IrJdrcxqAa)

#### Row - mainAxisSize

```dart
Row(
  mainAxisAlignment: MainAxisAlignment.start, 
  mainAxisSize: MainAxisSize.max, //modified this line of code as needed
  children: [
    Icon(Icons.stars, size: 50.0),
    Icon(Icons.stars, size: 50.0),
    Icon(Icons.stars, size: 50.0),
  ],
)
```



**MainAxisSIze.max** will expand the entire row on your phone from edge to edge. See below example

![img](https://lh4.googleusercontent.com/Zk-j7LrauAHLQMuG84ESrSPE2beIyevI5VFWAckouB1dGVUSZO2JxIVG4qkGCJfhfOmdiJBcNsQiY6BcG1zcWEEVK6OHDzUTseZd7dV1EOmigG_BehoJlBQXrP162rF5ugHGzNuO)

**MainAxisSIze.min** wii look like below which it will cut out all the remaining space.

![img](https://lh6.googleusercontent.com/gEgCmgL5hzOvncyE_PLiHrWir_TFDnwIoGBNOuLZBhZqXg9B6PwX1VQVK4RjapWxmcikqIxCfwC__k_I-ggOKVeeM_UNt8jETuoPtdFvtfWiol4bdN5slS8S29vjbOYfuHxwQnQE)

#### Row - crossAxisAlignment

```` dart
Row(
  mainAxisAlignment: MainAxisAlignment.spaceEvenly,
  crossAxisAlignment:CrossAxisAlignment.start,//Modified this line of code as needed
  children: [
    Icon(Icons.stars, size: 50.0),
    Icon(Icons.stars, size: 100.0),
    Icon(Icons.stars, size: 50.0),
  ],
)
````

![img](https://lh4.googleusercontent.com/Pp63hCM4r2e3INcDZx4MsBx29uzTnV9SpHLrf_Ce0xyUWiiMigqkGujMToKgDrOTBt1j0vnJLugaXo5W4EgFgY6SEVY4Qam_5m8xmjWzPNO94Q1m0aRj_8qsHA8_Navbilkk8pmt)



### Column (Horizontal Arrangement)

#### Basic usage

```dart
Column(
  children: [
    Icon(Icons.stars, size: 50.0),
    Icon(Icons.stars, size: 50.0),
    Icon(Icons.stars, size: 50.0),
  ],
)
```

#### Column - crossAxisAlignment

``` dart
Column(
  mainAxisAlignment: MainAxisAlignment.spaceEvenly,
  crossAxisAlignment: CrossAxisAlignment.start,
  children: [
    Icon(Icons.stars, size: 50.0),
    Icon(Icons.stars, size: 50.0),
    Icon(Icons.stars, size: 50.0),
  ],
)
```

![img](https://lh4.googleusercontent.com/cDxYV4XQBbo-HVpkLkgO40bq634VrbCE3rGfuHPq1DgIe8IV-mA-QSkCaWxA15wK11Tsz8wi6Ms1QqmwnELC8-ji9Hu1rdG_eHHgk0H68SgWOQt60YuQJs6UwyTJ6xHQMpdrQnv8)

#### Column - mainAxisAlignment

``` dart
Column(
  mainAxisAlignment: MainAxisAlignment.start, //modified this line of code as needed
  mainAxisSize: MainAxisSize.max,
  children: [
    Icon(Icons.stars, size: 50.0),
    Icon(Icons.stars, size: 50.0),
    Icon(Icons.stars, size: 50.0),
  ],
)
```

![img](https://lh6.googleusercontent.com/LMwP1rcxk3zYQcm6-0P7nMxcxjw0X5F_3tmO9NrnRTwpY7iNq8WeogrvVPzSlaqbtbbh94COYbN2w1LbHmgR_D6xnIfdyEVoDDIvKmKwQB5IDAJJLFpIIkIM_yfkAZFdzqqsxHxY)



### Layout Weights (Expanded)

#### Row with Expanded Widget

```` dart
Row(
  crossAxisAlignment: CrossAxisAlignment.stretch,
  children: [
    Expanded(
      flex: 1,
      child: Container(
        color: Colors.yellow,
        child: Center(child: Text('flex: 1')),
      ),
    ),
    Expanded(
      flex: 2,
      child: Container(
        color: Colors.orange,
        child: Center(child: Text('flex: 2')),
      ),
    ),
    Expanded(
      flex: 3,
      child: Container(
        color: Colors.cyan,
        child: Center(child: Text('flex: 3')),
      ),
    ),
  ],
)
````

![img](https://lh6.googleusercontent.com/8ZHTlp9OPyQ89b1-8nKmdMIHgxHyoSdrfdJ0G3aPVvT9KGk0eC4lSRHAOP6HP-5XEZ8jzIAObeW4LYaH0XRU9ZVlb4toGf63Rv4ACuNKUxDe1xwqfj44Gtr2OrntpODfC_rru0o7)



#### Column with Expanded Widgets

```` dart
Column(
  crossAxisAlignment: CrossAxisAlignment.stretch,
  children: [
    Expanded(
      flex: 1,
      child: Container(
        color: Colors.yellow,
        child: Center(child: Text('flex: 1')),
      ),
    ),
    Expanded(
      flex: 2,
      child: Container(
        color: Colors.orange,
        child: Center(child: Text('flex: 2')),
      ),
    ),
    Expanded(
      flex: 3,
      child: Container(
        color: Colors.cyan,
        child: Center(child: Text('flex: 3')),
      ),
    ),
  ],
)
````

![img](https://lh5.googleusercontent.com/jLuNlfhEGIjQFrb_f_69YxLebClmsXFAoXZIUCZZJMEnhkDyrqeHQZIya8Yc9rJnl8moFIUOMUrdE7B5mSm3XB_BYhqyIgvLLzYseo5I7bcbG1kRlCURagzoq3BDc2vTegbwLxol)