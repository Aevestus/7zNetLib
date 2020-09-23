# 7z.NET
A wrapper for 7za.exe for manipulating 7z archives
Based on NuGet packageid="7z.NET" version="1.0.3", made 2 modifications:

1. Extraction would not work when the DLL was used in a desktop application, that was ran from a shortcut, due to the fact of the way the path was read in
SevenZipBase.cs, in the Path7za property. It was changed to get the location where the app was running.
2. Removed the File.Exists check in SevenZipExtractor constructor, because it was failing on existing files.
