# easyFileManager
Android FileManager that can easily be integerated with your application's activity as a fragment;

## Features
Add filters to include only certain file and folder extentions

Add filters to exclude certain file and folder extentions

Basic file managment operations like copy, cut, delete, new folder

Add new operations to options bar or override the existing file managment operations

Add custom icons for certain file extentions

## Download
source:

aar library file:

## Setup

1.download the easyfilemanager.aar file

2.put the easyFileManager.aar file inside the lib directory of your project

3.configure you module's "build.gradle" to include the library file and its dependencies like below:

```

allprojects {
    repositories {
        jcenter()
        flatDir {
            dirs 'libs'
        }
    }
}
dependencies {
//feel free to update these to the latest versions
    implementation (name:'easyfilemanager',ext:'aar')
    implementation fileTree(dir: 'libs', include: ['*.jar'])
    implementation 'androidx.appcompat:appcompat:1.1.0'
    implementation 'androidx.recyclerview:recyclerview:1.0.0'
    implementation 'androidx.constraintlayout:constraintlayout:1.1.3'
}

```

4.easyFileManager needs Write access permission to external storage; If the permission doesn't exist exception will occur when easyFileManager is being instantiated; Declare the permission in manifest and ask for it on runtime if the target api level is above or equal 23;
