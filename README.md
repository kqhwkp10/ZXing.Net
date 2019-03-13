ZXing.Net
ZXing.Net.Mobile Logo

Project Description
A library which supports decoding and generating of barcodes (like QR Code, PDF 417, EAN, UPC, Aztec, Data Matrix, Codabar) within images.

The project is a port of the java based barcode reader and generator library ZXing.
https://github.com/zxing/zxing
It has been ported by hand with a lot of optimizations and improvements.

The following barcodes are supported by the decoder: UPC-A, UPC-E, EAN-8, EAN-13, Code 39, Code 93, Code 128, ITF, Codabar, MSI, RSS-14 (all variants), QR Code, Data Matrix, Aztec and PDF-417. The encoder supports the following formats: UPC-A, EAN-8, EAN-13, Code 39, Code 128, ITF, Codabar, Plessey, MSI, QR Code, PDF-417, Aztec, Data Matrix

Assemblies are available for the following platforms:
.Net 2.0, 3.5, 4.0, 4.5, 4.6 and 4.7
Silverlight 4 and 5
Windows Phone 7.0, 7.1 and 8.0
Windows CE
Windows RT Class Library and Runtime Components (winmd)
.NET Standard / .NET Core / UWP
Portable Class Library
Unity3D (.Net 2.0 built without System.Drawing reference)
Xamarin.Android (formerly Mono for Android)
bindings to CoreCompat.System.Drawing, ImageSharp, SkiaSharp, OpenCVSharp, Magick, Kinect V1 and V2
support COM interop, can be used with VBA
The library is available in the release section release section and as NuGet package, too.

N|NuGet Build status

Additional platform support without pre-built binaries
The library can be built for Xamarin.iOS (formerly MonoTouch). The project file and solution are available in the source code repository.

A special version for the .Net Micro Framework can be found in a separate branch in the source code repository.

The following demo clients are available:
decoder for the command line
encoder for the command line
Windows Forms demo (demonstrates decoding and encoding of static images and from a camera)
Windows Phone demo (demonstrates decoding of static images and from a camera)
Windows Service demo (demonstrates decoding of static images)
Windows Presentation Framework demo (demonstrates decoding of static images)
Windows CE demo (demonstrates decoding of static images)
Windows RT demo (demonstrates decoding of static images)
Windows Store App with HTML5/JS (demonstrates decoding of static images)
Unity3D and Vuforia demo (demonstrates encoding of barcodes and decoding of images from a camera with Unity3D)
Silverlight demo (demonstrates decoding and encoding of static images)
EmguCV demo (demonstrates decoding of images from a camera and uses the EmguCV framework)
OpenCV demo (demonstrates decoding of images from a camera and uses the OpenCVSharp framework)
AForge demo (demonstrates decoding of images from a camera and uses the AForge framework)
Thanks
Many thanks to the team of the zxing project for their great work. ZXing.Net would not be possible without your work!

Usage examples
The source code repository includes small examples for Windows Forms, Silverlight, Windows Phone and other project types.

small example decoding a barcode inside a bitmap (.Net 2.0/3.5/4.x)
// create a barcode reader instance
IBarcodeReader reader = new BarcodeReader();
// load a bitmap
var barcodeBitmap = (Bitmap)Image.LoadFrom("C:\\sample-barcode-image.png");
// detect and decode the barcode inside the bitmap
var result = reader.Decode(barcodeBitmap);
// do something with the result
if (result != null)
{
   txtDecoderType.Text = result.BarcodeFormat.ToString();
   txtDecoderContent.Text = result.Text;
}
