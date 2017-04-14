# Carousel
A sample project to test UWP Carousel Control

Found issue:

If Carousel.ItemDepth was not set manually, following exception occurs: 

System.InvalidCastException: Unable to cast object of type 'System.Double' to type 'System.Int32'.
   at Microsoft.Toolkit.Uwp.UI.Controls.Carousel.get_ItemDepth()
   at Microsoft.Toolkit.Uwp.UI.Controls.CarouselPanel.GetProjectionFromSelectedIndex(Int32 childIndex)
   at Microsoft.Toolkit.Uwp.UI.Controls.CarouselPanel.ArrangeOverride(Size finalSize)

if Carousel has been put in a auto-sized Row or Column, following exception occurs:

COMException: Error HRESULT E_FAIL has been returned from a call to a COM component.

StackTrace:
   at Windows.UI.Xaml.UIElement.UpdateLayout()
   at Microsoft.VisualStudio.DesignTools.UwpDesigner.Views.ViewObjects.WindowsUIXamlViewVisual.UpdateLayout()
   at Microsoft.VisualStudio.DesignTools.UwpDesigner.Views.WindowsXamlSceneView.UpdateLayoutInternal()
   at Microsoft.VisualStudio.DesignTools.Designer.Views.SceneView.UpdateLayout()

InnerException: None
