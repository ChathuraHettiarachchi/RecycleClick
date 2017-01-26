# RecycleClick [ ![Download](https://api.bintray.com/packages/chathurahettiarachchi/maven/RecycleClick/images/download.svg) ](https://bintray.com/chathurahettiarachchi/maven/RecycleClick/_latestVersion)
Android recycler view not supports for onItemClickListner event. This library helps to wrap up and gain the missing recycle view item click and item long click functions. This library is a project carried by Lakitha, give a visit https://github.com/LakithaRav

Anyway... when talk about Android ListView and RecycleView, in old times through the development i preffer Android ListView. It already have click suport inbuilt.
with the development I got to know using Android RecycleView is more efficient and memory saving.

![recycleclick](https://cloud.githubusercontent.com/assets/13764097/22052145/93de135a-dd6e-11e6-85db-fc78d4220e95.jpg)

This library contains mainly two functions,

* RecycleClick - OnItemClickListener
* RecycleClick - OnItemLongClickListener

  
####Let's take a look how to add this to your project

For the android project just include the following dependency inside you build.gradle's depedency list.

Gradle
------
```
repositories {
  jcenter()
}

dependencies {
    ...
    compile 'com.chootdev:recycleclick:1.0.0'
}
```

if you using maven use following
Maven
------
```
<dependency>
  <groupId>com.chootdev</groupId>
  <artifactId>recycleclick</artifactId>
  <version>1.0.0</version>
  <type>pom</type>
</dependency>
```

After setup installing lib to your project you just need only to call it using just few lines of code. It will return you a string with the results.

Usage
-----
To add item click support
```java
RecycleClick.addTo(YOUR_RECYCLEVIEW).setOnItemClickListener(new RecycleClick.OnItemClickListener() {
            @Override
            public void onItemClicked(RecyclerView recyclerView, int position, View v) {
                // YOUR CODE
            }
        });
```

To change item click to long click,
```java
RecycleClick.addTo(YOUR_RECYCLEVIEW).setOnItemLongClickListener(new RecycleClick.OnItemLongClickListener() {
            @Override
            public boolean onItemLongClicked(RecyclerView recyclerView, int position, View v) {
                // YOUR CODE
                return true;
            }
        });
```

Both of these functions are providing all necessary information you need to get from an item selection in RecycleView.

i.e :
```java
RecyclerView recyclerView :- current recycleView
int position :- selected positoin of populated data set
View v :- selected view
```
With the "View" you can manupulate any view associate with selected item.

Limitations
-----------
* Currently min SDK is set to 16

Output Generated
----------------
![ezgif com-video-to-gif](https://cloud.githubusercontent.com/assets/13764097/22053273/92c2c23e-dd75-11e6-80cf-01ca35ad0f25.gif)

Changelog
---------
* **1.0.0**
    * Stable the release with sample code
* **0.1.1**
    * Support for click events
* **0.1.0**
    * Initial release
    

## Authors

Chathura Hettiarachchi, chathura93@yahoo.com

Lakitha Samarasinghe, lakitharav@gmail.com

# License
Copyright 2016 Chathura Hettiarachchi

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
