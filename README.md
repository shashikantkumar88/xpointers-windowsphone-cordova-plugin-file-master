<!---
 license: Licensed to the Apache Software Foundation (ASF) under one
         or more contributor license agreements.  See the NOTICE file
         distributed with this work for additional information
         regarding copyright ownership.  The ASF licenses this file
         to you under the Apache License, Version 2.0 (the
         "License"); you may not use this file except in compliance
         with the License.  You may obtain a copy of the License at

           http://www.apache.org/licenses/LICENSE-2.0

         Unless required by applicable law or agreed to in writing,
         software distributed under the License is distributed on an
         "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
         KIND, either express or implied.  See the License for the
         specific language governing permissions and limitations
         under the License.
-->

# Modifyed org.apache.cordova.file
---------------
**You can download modifyed plugin using --**
---------------
cordova plugin add https://github.com/shashikantkumar88/xpointers-windowsphone-cordova-plugin-file-master.git

**If you are using file plugin you need to install org.apache.cordova.file-transfer plugin. With out file transfer plugin it will not work.**
---------------
**Take a look --**
---------------
        window.requestFileSystem(LocalFileSystem.PERSISTENT, 0, function(fileSystem) {
            fileSystem.root.getFile("readme.txt", {
                create: true,
                exclusive: false
            }, function(fileEntry) {
                fileEntry.createWriter(function(writer) {
                   //saving image from server to windows phone isolated storage
                   writer.saveImageIsolated('http://pah.stratawizdev.com/PHNewsImages/tree.jpg');
                }, null);
            }, null);
        }, null);

**For Displaying image in view-**
---------------
```html
<img src="../tree.jpg" width='100%'>
```
