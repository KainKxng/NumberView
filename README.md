#NumberView

A simple number tweener.

![First frame](design/frame1.png)&nbsp;&nbsp;&nbsp;&nbsp;![Transitioning to the next time](design/frame2.png)&nbsp;&nbsp;&nbsp;&nbsp;![A completed loop cycle](design/frame3.png)


---
###What is it?
NumberView is mean to be a take on [Timely][1]'s beatiful and tasteful number tweening animations. Despite looking like it draws actual numbers in it, the numbers drawn are represented as Bèzier curve paths, meticulously calculated with control points and anchors.

---
###Usage
Using [NumberView][2] in your project is simple. It is a standalone class, no resource files required. It can be added in programatically into your layouts, or be included as a tag in resource files:

```
<com.deange.numberview.NumberView
        android:layout_height="wrap_content"
        android:layout_width="wrap_content" />
```

---
###Dependencies
No dependencies. Works on all versions of Android, all the way back to 1.0!

---
###Known Issues

I've seen some lag on the Nexus 5 running on ART. Not sure if this is specific to my device, all Nexus 5s, or ART entirely.

NumberView has a built-in auto-advancing timing system that automatically tweens to the next value, but it isn't a perfect system, since it must be coupled with other view drawing events. It is recommended that you turn off auto-advancing using the `setAutoAdvance(boolean)` method), and manually call `advance()` when necessary. The [Timer][3] class is perfect for this sort of behaviour, especially if you will be using this for any fixed-rate mechanism. See the example activity class for a quick implementation.

---
###Developed By
- Christian De Angelis - <christiandeange@gmail.com>

---
###License
```
Copyright 2013 Christian De Angelis

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

[1]: https://play.google.com/store/apps/details?id=ch.bitspin.timely&hl=en
[2]: https://github.com/cdeange/NumberView/blob/master/NumberView/src/main/java/com/deange/numberview/NumberView.java
[3]: http://developer.android.com/reference/java/util/Timer.html
