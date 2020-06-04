### **UI Overview**

UI is an essential component of Flutter development.

UI is all about Widgets in Layout.



### Widgets

Widgets are the UI elements you can use such as Button, Text, ScrollBar, AppBar, etc.

![img](https://lh5.googleusercontent.com/YSCB26EJNLl_N1J2Qb0pN2zcaJLAmIb8d3Y_Abvdk6Z8FUnWUqSs5d5uZSgh-MImj6VvdDwBvHSCHEo2gvQsjCIf47KhcB_1Bn2tZePm-AyANW6HOHnCJ7xdxrTaZLt1Xj-fl58I)

> Find all the Flutter Widgets at https://flutter.dev/docs/development/ui/widgets



### Layout

Layout is how we position, align, arrange the widges together.

![img](https://lh5.googleusercontent.com/yseoboixlTOwKexndpEQkDjixLVJUMZbRKEwXmSKq7HRJMMKSat6l2GukI6TtZNNgmf6MVH5XIiljGw-Hz9ulGmMXuRa2HTDlb5F_6H_DRYVGN9ttJv2El7-JSDxkw5Z9ALWoUxS)



> For Flutter Layout, please see https://flutter.dev/docs/development/ui/widgets/layout



#### Widges + Layout in a Tree

Container, Row, Column shown below are called **Layout ** and there are two types of Layout Widget including **Single-Child Layout Widget** and **Multi-child Layout Widget**. Icon, Text are **Widges**. Normally, the Layout will contain Widges or other Layout in a Tree structure as shown below: 

![img](https://lh3.googleusercontent.com/FUirTDRcg9PSMq31YeYN5Mt4_g1gvk7AG0ytOMLfyYQjMTf5KJjvDOPACwXztfueCdTGoGzuqREfc_wNom8-mzhG5bLrLzzR63J6y1Gy-3xWaXUih1Vb5bXobBWo3SuQwIpx3DyW)

You can see that the Container widget have a child of Row widget and that Row have childrens of three Column widgets. 

