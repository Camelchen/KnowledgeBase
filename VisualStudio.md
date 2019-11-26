#### Code coverage
* open coverage report is the feature only for Enterprise edition.
* step to bring back on Professional
  * edit **devenv.exe.config** file
    * %USERPROFILE%\AppData\Local\Microsoft\VisualStudio\16.0_somehash\devenv.exe.config
    * add `;Extensions\TestPlatform` at the end of `<probing privatePath=""/>`
  * copy files 
    > Common7/IDE/Extensions/TestPlatform/Microsoft.VisualStudio.Coverage.Analysis.dll
    > Common7/IDE/Extensions/TestPlatform/Microsoft.VisualStudio.Coverage.Interop.dll 
    >
    to
    > Common7/IDE/PrivateAssemblies
