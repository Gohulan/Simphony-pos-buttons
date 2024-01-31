# Simphony UI Button Styles

This XAML code defines a set of custom button styles for Oracle Micros Simphony POS applications.

## Resource Dictionary

The Resource Dictionary serves as a container for styles and converters. It sets up XML namespaces for various assemblies, making them accessible throughout the XAML code.

```xml
<ResourceDictionary
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    xmlns:mcontrol="clr-namespace:Micros.OpsUI.Controls;assembly=OpsUI"
    xmlns:mconverters="clr-namespace:Micros.OpsUI.Converters;assembly=OpsUI"
    xmlns:systemWindows="clr-namespace:System.Windows;assembly=PresentationFramework"
    xmlns:system="clr-namespace:System;assembly=mscorlib"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    xmlns:wtk="clr-namespace:System.Windows;assembly=WPFToolkit">
```
## Converters
The following converters are defined:

BindableStringToResourceConverter: Converts a bindable string to a resource.
ButtonCornerTypeToCornerRadiusConverter: Converts button corner type to corner radius.
BoolToVisibilityConverter: Converts a boolean to visibility.
NullToVisibilityConverter: Converts null to visibility.
```xml
<mconverters:BindableStringToResourceConverter x:Key="bindableStringToResourceConverter" />
<mconverters:ButtonCornerTypeToCornerRadiusConverter x:Key="buttonCornerTypeToCornerRadiusConverter"/>
<mconverters:BoolToVisibilityConverter x:Key="boolToVisibilityConverter"/>
<mconverters:NullToVisibilityConverter x:Key="nullToVisibilityConverter"/>
```
Color Definitions
A set of colors is defined to be used in the content below.

```xml
<!--This section is used to define the colors you want to use in the below content.-->
<Color x:Key="ButtonColor_01">#312D2A</Color>
<Color x:Key="ButtonColor_02">#C74634</Color>
<!--... (colors 03 to 17) ...-->
```
Button Styles
A style for a button (Simphony-Buttons-Gohulan-01) is defined, and additional styles are based on this initial style.
```xml
<Style x:Key="Simphony-Buttons-Gohulan-01" TargetType="{x:Type mcontrol:Button}" BasedOn="{StaticResource MicrosBlue}">
    <!-- Style definition -->
</Style>

<!-- Simphony-Buttons-Gohulan-02, Simphony-Buttons-Gohulan-03, ... -->
<Style TargetType="mcontrol:Button" x:Key="Simphony-Buttons-Gohulan-02" BasedOn="{StaticResource Simphony-Buttons-Gohulan-01}">
    <!-- Style definition -->
</Style>
```
The x:Key attribute uniquely identifies each style, TargetType specifies the type of control (mcontrol:Button), and BasedOn indicates that a style is based on another.
