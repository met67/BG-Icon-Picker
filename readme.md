# BG: Icon Picker
Icon picker for Umbraco 7.4.0+
- - -
Inspired by the [Iconator package](https://our.umbraco.com/projects/backoffice-extensions/iconator/). Since the creator of that package doesn't respond to pull requests, I took matters into my own hands and redesigned it from the ground up with better functionality and styling.
- - -

## Installation
1. Install the package
2. Configure the data type

   **Location:** Developer > Data Types > BG: Picker


## Configuring the Data Type:

**Path to stylesheet:**
Stand-alone stylesheet for the icons is required.
```
/css/icons.min.css
```

**Class name regex:**
It's recommended to _not use_ "icon" as class identifier so it won't interfere with the umbraco icons.
```
(icn-[^:]*?):before
```

**Icon pattern:**
"{0}" will be replaced with the icon regex.
```
<i class="{0}"></i>
```

## Retrieving data from the icon picker:
The icon picker returns a string with the icon name so it's really simple to work with.
```
<i class="@Model.Content.GetPropertyValue<string>("icon")"></i>
```