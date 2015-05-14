#NumberView

A simple number tweener.

![gif](design/output.gif)

---
###What is it?
NumberView is mean to be a take on [Timely][1]'s beatiful and tasteful number tweening animations. Despite looking like it draws actual numbers in it, the numbers drawn are represented as Bèzier curve paths, meticulously calculated with control points and anchors.

---
###Usage
Using [NumberView][2] to show a single digit in your project is simple. You can drop it into your XML files as a regular custom view:

    <com.deange.numberview.NumberView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content" />


    final NumberView view = findViewById(...);
    view.advance(1);
    postDelayed(() -> { view.advance(2) }, 1000);
    postDelayed(() -> { view.advance(3) }, 2000);
    ...

However, typically you'll want to show more than one digit at a time. For that you can use [NumberViewGroup][3], which automatically takes care of adding new digits as you need them.

    <com.deange.numberview.NumberViewGroup
            android:layout_height="wrap_content"
            android:layout_width="wrap_content" />


    final NumberViewGroup view = findViewById(...);
    view.advance(1);
    postDelayed(() -> { view.advance(20) }, 1000);
    postDelayed(() -> { view.advance(300) }, 2000);
    ...

You can always view the sample application code for more usage demos.

---
###Dependencies
No dependencies. Works on all versions of Android, all the way back to API level 1!

---
###Download

    repositories {
        maven {
            url "https://jitpack.io"
        }
    }

    dependencies {
        compile 'com.github.cdeange:NumberView:1.0.0'
    }

---
###Developed By
- Christian De Angelis - <de@ngelis.com>

---
###License

    Copyright 2015 Christian De Angelis

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.


[1]: https://play.google.com/store/apps/details?id=ch.bitspin.timely
[2]: https://github.com/cdeange/NumberView/blob/master/library/src/main/java/com/deange/numberview/NumberView.java
[3]: https://github.com/cdeange/NumberView/blob/master/library/src/main/java/com/deange/numberview/NumberViewGroup.java
