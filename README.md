# 实验二Android_Layout                                   
>                                                                               软工（1）班 黄磊 123012016005
## 一.实验内容
掌握Android的 线性布局、约束布局和表格布局，并会运用以学只是设计布局界面。


## 二.相关概念
1.线性布局：
一种使用单个水平行或垂直行来组织子项的布局。它会在窗口长度超出屏幕长度时创建一个滚动条。 

![线性布局](https://developer.android.google.cn/images/ui/linearlayout.png)    
**图1 线性布局**

2.Constraint布局：
让您能够指定子对象彼此之间的相对位置（子对象 A 在子对象 B 左侧）或子对象与父对象的相对位置（与父对象顶部对齐）。

![线性布局](https://developer.android.google.cn/images/ui/relativelayout.png)              
**图2 约束布局**

3.Constraint布局：
让您能够指定子对象彼此之间的相对位置（子对象 A 在子对象 B 左侧）或子对象与父对象的相对位置（与父对象顶部对齐）。

![表格布局](https://developer.android.google.cn/images/ui/gridview-small.png)              
**图3 表格布局**


## 三.实验关键/核心代码
1.线性布局：
<LinearLayout
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:orientation="vertical">

        <Button
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:text="one one"
            android:textAppearance="@style/TextAppearance.AppCompat.Button" />

        <Button
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:text="two one"
            android:textAppearance="@style/TextAppearance.AppCompat.Button" />

        <Button
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:text="three one"
            android:textAppearance="@style/TextAppearance.AppCompat.Button" />

        <Button
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:layout_column="0"
            android:text="four one"
            android:textAppearance="@style/TextAppearance.AppCompat.Button" />
    </LinearLayout>

    <LinearLayout
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:orientation="vertical">

        <Button
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:text="one two"
            android:textAppearance="@style/TextAppearance.AppCompat.Button" />

        <Button
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:text="two two"
            android:textAppearance="@style/TextAppearance.AppCompat.Button" />

        <Button
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:text="three two"
            android:textAppearance="@style/TextAppearance.AppCompat.Button" />

        <Button
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:text="four two"
            android:textAppearance="@style/TextAppearance.AppCompat.Button" />
    </LinearLayout>

    <LinearLayout
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:orientation="vertical">

        <Button
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:text="one three"
            android:textAppearance="@style/TextAppearance.AppCompat.Button" />

        <Button
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:text="two three"
            android:textAppearance="@style/TextAppearance.AppCompat.Button" />

        <Button
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:text="three three"
            android:textAppearance="@style/TextAppearance.AppCompat.Button" />

        <Button
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:layout_column="0"
            android:text="four three"
            android:textAppearance="@style/TextAppearance.AppCompat.Button" />
    </LinearLayout>

    <LinearLayout
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:orientation="vertical">

        <Button
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:text="one four"
            android:textAppearance="@style/TextAppearance.AppCompat.Button" />

        <Button
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:text="two four"
            android:textAppearance="@style/TextAppearance.AppCompat.Button" />

        <Button
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:text="three four"
            android:textAppearance="@style/TextAppearance.AppCompat.Button" />

        <Button
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:layout_column="0"
            android:text="four four"
            android:textAppearance="@style/TextAppearance.AppCompat.Button" />
</LinearLayout>

2.Constraint布局：

<TextView
        android:id="@+id/TextView1"
        android:layout_width="80dp"
        android:layout_height="80dp"
        android:background="@android:color/holo_red_light"
        android:gravity="center"
        android:text="RED"
        android:textSize="20dp"
        android:layout_alignParentTop="true"/>

    <TextView
        android:id="@+id/textView2"
        android:layout_width="120dp"
        android:layout_height="80dp"
        android:background="@android:color/holo_orange_dark"
        android:gravity="center"
        android:layout_centerHorizontal="true"
        android:text="ORANGE"
        android:textSize="20dp"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintLeft_toRightOf="@id/TextView1"
        android:layout_marginLeft="50dp"/>

    <TextView
        android:id="@+id/textView3"
        android:layout_width="120dp"
        android:layout_height="80dp"
        android:background="@android:color/holo_orange_light"
        android:gravity="center"
        android:text="YELLOW"
        android:textSize="20dp"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintLeft_toRightOf="@id/textView2"
        android:layout_marginLeft="40dp"/>

    <TextView
        android:id="@+id/textView4"
        android:layout_width="120dp"
        android:layout_height="80dp"
        android:background="@android:color/holo_green_light"
        android:gravity="center"
        android:text="GREEN"
        android:textSize="20dp"
        app:layout_constraintTop_toBottomOf="@id/TextView1"
        app:layout_constraintLeft_toLeftOf="parent"
        android:layout_marginLeft="25dp"/>
    <TextView
        android:id="@+id/textView5"
        android:layout_width="80dp"
        android:layout_height="80dp"
        android:background="@android:color/holo_blue_light"
        android:gravity="center"
        android:text="BLUE"
        android:textSize="20dp"
        app:layout_constraintTop_toBottomOf="@id/textView2"
        app:layout_constraintLeft_toRightOf="@id/textView4"
        android:layout_marginLeft="20dp"/>
    <TextView
        android:id="@+id/textView6"
        android:layout_width="120dp"
        android:layout_height="80dp"
        android:background="@android:color/holo_purple"
        android:gravity="center"
        android:text="INDIGO"
        android:textSize="20dp"
        app:layout_constraintTop_toBottomOf="@id/TextView1"
        app:layout_constraintLeft_toRightOf="@id/textView5"
        android:layout_marginLeft="20dp"/>
    <TextView
        android:id="@+id/textView7"
        android:layout_width="match_parent"
        android:layout_height="80dp"
        android:background="@android:color/darker_gray"
        android:gravity="center"
        android:text="VIOLET"
        android:textSize="20dp"
        app:layout_constraintBottom_toBottomOf="parent"/>
        
3.Constraint布局：

    <TableRow>
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="      Open..."
            android:gravity="left"
            android:textColor="@android:color/white"
            android:layout_column="0"/>
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Ctrl-O "
            android:gravity="right"
            android:textColor="@android:color/white"
            android:layout_column="3"/>
    </TableRow>
    <TableRow>
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="      Save..."
            android:gravity="left"
            android:textColor="@android:color/white"
            android:layout_column="0"/>
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Ctrl-S "
            android:gravity="right"
            android:textColor="@android:color/white"
            android:layout_column="3"/>
    </TableRow>
    <TableRow>
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="      Save As..."
            android:gravity="left"
            android:textColor="@android:color/white"
            android:layout_column="0"/>
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Ctrl-Shift-S "
            android:gravity="right"
            android:textColor="@android:color/white"
            android:layout_column="3"/>
    </TableRow>

    <View android:layout_height="1dp" android:background="#ffffff" android:layout_width="fill_parent"></View>

    <TableRow>

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="X    Import..."
            android:gravity="left"
            android:textColor="@android:color/white"
            android:layout_weight="5"
            android:layout_column="0"/>
    </TableRow>
    <TableRow>

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="X    Export..."
            android:gravity="left"
            android:textColor="@android:color/white"
            android:layout_weight="5"
            android:layout_column="0"/>
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Ctrl-E "
            android:gravity="right"
            android:textColor="@android:color/white"
            android:layout_weight="2"
            android:layout_column="3"/>
    </TableRow>

    <View android:layout_height="1dp" android:background="#ffffff" android:layout_width="fill_parent"></View>

    <TableRow>
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="       Quit "
            android:textColor="@android:color/white"
            android:layout_column="0"/>
    </TableRow>

## 4.实验运行截图

![线性布局](https://github.com/Huanglei666/Android_Layout/blob/master/%E8%BF%90%E8%A1%8C%E6%88%AA%E5%9B%BE/%E7%BA%BF%E6%80%A7%E5%B8%83%E5%B1%80.png)

**图4 线性布局**
                         
![约束布局](https://github.com/Huanglei666/Android_Layout/blob/master/%E8%BF%90%E8%A1%8C%E6%88%AA%E5%9B%BE/Constraint%E5%B8%83%E5%B1%80.png)

**图5 约束布局**

![表格布局](https://github.com/Huanglei666/Android_Layout/blob/master/%E8%BF%90%E8%A1%8C%E6%88%AA%E5%9B%BE/%E8%A1%A8%E6%A0%BC%E5%B8%83%E5%B1%80.png)

**图6 线性布局**
