DjvuNet
=======

DjvuNet is a fully managed Djvu reader in C#. This was created to support my commercial activities as Djvu is a superior format for certain document types. This is a faithful reimplementation of the Java Djvu Viewer. It is totally usable, but probably needs to be optimized a bit as Djvu is complicated.

**Usage**
`````c#
DjvuDocument doc = new DjvuDocument(@"Mcguffey's_Primer.djvu");

var page = doc.Pages[0];

page
    .BuildPageImage()
    .Save("TestImage1.png", ImageFormat.Png);

page.IsInverted = true;

page
    .BuildPageImage()
    .Save("TestImage2.png", ImageFormat.Png);
`````
