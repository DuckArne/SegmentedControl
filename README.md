# Segmented Control Plugin for Xamarin Forms

#### Setup
* Available on NuGet: https://www.nuget.org/packages/SegmentedControl.FormsPlugin/ [![NuGet](https://img.shields.io/nuget/v/SegmentedControl.FormsPlugin.svg?label=NuGet)](https://www.nuget.org/packages/SegmentedControl.FormsPlugin/)
* Install in your PCL project and Client projects.

**Platform Support**

|Platform|Supported|Version|Renderer|
| ------------------- | :-----------: | :-----------: | :------------------: |
|Xamarin.iOS Unified|Yes|iOS 8.1+|UISegmentedControl|
|Xamarin.Android|Yes|API 15+|RadioGroup|

#### Usage

```xml
xmlns:controls="clr-namespace:SegmentedControl.FormsPlugin.Abstractions;assembly=SegmentedControl.FormsPlugin.Abstractions"
```

```xml
<controls:SegmentedControl x:Name="SegControl" TintColor="#007AFF" SelectedSegment="0" ValueChanged="Handle_ValueChanged">
  <controls:SegmentedControl.Children>
    <controls:SegmentedControlOption Text="Tab 1" />
    <controls:SegmentedControlOption Text="Tab 2" />
    <controls:SegmentedControlOption Text="Tab 3" />
    <controls:SegmentedControlOption Text="Tab 4" />
  </controls:SegmentedControl.Children>
</controls:SegmentedControl>
<StackLayout x:Name="SegContent" Grid.Row="1" Grid.Column="0">
</StackLayout>
```

#### Event handler

```
public void Handle_ValueChanged(object o, EventArgs e)
{
	SegContent.Children.Clear();

	switch (SegControl.SelectedSegment)
	{
		case 0:
			SegContent.Children.Add(new Label() { Text="Tab 1 selected" });
			break;
		case 1:
			SegContent.Children.Add(new Label() { Text = "Tab 2 selected" });
			break;
		case 2:
			SegContent.Children.Add(new Label() { Text = "Tab 3 selected" });
			break;
		case 3:
			SegContent.Children.Add(new Label() { Text = "Tab 4 selected" });
			break;
	}
}
```

#### Contributors
* [alexrainman](https://github.com/alexrainman)

Thanks!

#### License
Licensed under repo license