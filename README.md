Image Cache for Android
=======================

Image Cache for Android is an standalone library based on BitmapFun.zip from
Displaying Bitmaps Efficiently lesson.

**http://developer.android.com/training/displaying-bitmaps/index.html**

Memory and disk is used for caching images. Most important class is ImageFetcher, which
is used for loading images into ImageView. Don't forget to call setExitTasksEarly(false)
during onResume(). In onPause call setExitTasksEarly(true) and flushCache().

Changes against BitmapFun
-------------------------

There were several issues with ImageFetcher from BitmapFun project, when I used two
image fetcher for two ImageViews, so I have synchronized some parts to work more
reliable.

Disk image cache was not used if 10MB were not free, so I managed to changed this to
use usable space at least for disk image cache, because image loading stopped working
otherwise.



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
