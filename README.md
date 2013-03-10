Image Cache for Android
=======================

Image Cache for Android is standalone library based on BitmapFun.zip from
Displaying Bitmaps Efficiently lesson.

**http://developer.android.com/training/displaying-bitmaps/index.html**

Memory and disk is used for caching images. Most important class is ImageFetcher, which
is used for loading images into ImageView. Don't forget to call setExitTasksEarly(false)
during onResume(). In onPause call setExitTasksEarly(true) and flushCache().

Changes against BitmapFun
-------------------------

There were several issues with ImageFetcher from BitmapFun project, when there were used
two ImageFetchers and two ImageViews. Now more ImageFetchers with more ImageViews works
well.

Disk image cache was not used if 10MB were not free. Now is used usable space at least,
because image loading stopped working otherwise.



Developed By
============

* Android Team


Fixed and Modified By
---------------------

Ondřej Kroupa - <ondra@generify.io>



License
=======

    Copyright (C) 2012 The Android Open Source Project
    Copyright 2012 Ondřej Kroupa

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
