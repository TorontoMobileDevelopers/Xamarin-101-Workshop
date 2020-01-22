# Xamarin 101 Workshop

## Exercise 2 - Creating Monkey APP

1 - Add Xamarin.FFImageLoading.Forms to all projects
====================================================

2 -- Add URL property to the Item Class
=======================================

3 -- Edit MockDataStore.cs where the list is populated:
=======================================================

new Item { Id = Guid.NewGuid().ToString(), Text = \"First item\",
Description=\"This is an item description.\", Url =
\"<http://upload.wikimedia.org/wikipedia/commons/thumb/9/96/Portrait_Of_A_Baboon.jpg/314px-Portrait_Of_A_Baboon.jpg>\"},

new Item { Id = Guid.NewGuid().ToString(), Text = \"Second item\",
Description=\"This is an item description.\", Url =
\"<http://upload.wikimedia.org/wikipedia/commons/thumb/4/40/Capuchin_Costa_Rica.jpg/200px-Capuchin_Costa_Rica.jpg>\"},

new Item { Id = Guid.NewGuid().ToString(), Text = \"Third item\",
Description=\"This is an item description.\", Url =
\"<http://upload.wikimedia.org/wikipedia/commons/thumb/8/83/BlueMonkey.jpg/220px-BlueMonkey.jpg>\"},

new Item { Id = Guid.NewGuid().ToString(), Text = \"Fourth item\",
Description=\"This is an item description.\", Url =
\"<http://upload.wikimedia.org/wikipedia/commons/thumb/2/20/Saimiri_sciureus-1_Luc_Viatour.jpg/220px-Saimiri_sciureus-1_Luc_Viatour.jpg>\"
},

new Item { Id = Guid.NewGuid().ToString(), Text = \"Fifth item\",
Description=\"This is an item description.\", Url =
\"<http://upload.wikimedia.org/wikipedia/commons/thumb/8/87/Golden_lion_tamarin_portrait3.jpg/220px-Golden_lion_tamarin_portrait3.jpg>\"
},

new Item { Id = Guid.NewGuid().ToString(), Text = \"Sixth item\",
Description=\"This is an item description.\", Url =
\"http://upload.wikimedia.org/wikipedia/commons/thumb/0/0d/Alouatta\_guariba.jpg/200px-Alouatta\_guariba.jpg\"
}

4 -- Open ItemsPage.xaml, clear ItemSource with arrays
======================================================

5 -- Import FFImageLoader to Page\
xmlns:ffimageloading=\"clr-namespace:FFImageLoading.Forms;assembly=FFImageLoading.Forms\"

6 -- Add to iOS AppDelegate\
FFImageLoading.Forms.Platform.CachedImageRenderer.Init();

Add to Android MainActivity.cs

FFImageLoading.Forms.Platform.CachedImageRenderer.Init(true);

7-- Add ffimage loader to listview and Change the Source to Bind to Item.URL
============================================================================

\<Grid\>

\<Grid.ColumnDefinitions\>

\<ColumnDefinition Width=\"100\"/\>

\<ColumnDefinition/\>

\</Grid.ColumnDefinitions\>

\<Grid.RowDefinitions\>

\<RowDefinition/\>

\<RowDefinition/\>

\</Grid.RowDefinitions\>

\<ffimageloading:CachedImage

Grid.Row=\"0\"

Grid.Column=\"0\"

Grid.RowSpan=\"2\"

Source=\"{Binding Url}\"/\>

\<Label Text=\"{Binding Text}\"

Grid.Row=\"0\"

Grid.Column=\"1\"

LineBreakMode=\"NoWrap\"

Style=\"{DynamicResource ListItemTextStyle}\"

FontSize=\"16\" /\>

\<Label Text=\"{Binding Description}\"

Grid.Row=\"1\"

Grid.Column=\"1\"

LineBreakMode=\"NoWrap\"

Style=\"{DynamicResource ListItemDetailTextStyle}\"

FontSize=\"13\" /\>

\</Grid\>

8 -- Change from a list to a CollectionView and make the list horizontal
========================================================================

9 - Extra Challenges
====================

Change the stack layout from the ItemDetailPage.xaml

-   Grid :
    <https://docs.microsoft.com/en-us/xamarin/xamarin-forms/user-interface/layouts/grid>

-   FlexLayout:
    [https://docs.microsoft.com/en-us/xamarin/xamarin-forms/user-interface/layouts/flex-layout\
    ](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/user-interface/layouts/flex-layout)
