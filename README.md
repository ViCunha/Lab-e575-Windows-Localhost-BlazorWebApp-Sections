
### Overview
---
Control the content in a Razor component from a child Razor component.
   
### Key Aspects
---
- Blazor
  - Blazor-Sections

### Environment
---
- Microsoft Visual Studio 2022
  - DNET 8

### Actions
---
Import the namespaces
  - Import the namespace: Microsoft.AspNetCore.Components.Sections
```
@using Microsoft.AspNetCore.Components.Sections
```
  - Make the public objects from BlazorWebApp_Sections.Components.Layout accessable for all
```
@using BlazorWebApp_Sections.Components.Layout
```

Define Content placeholder
- Define SectionOutlet tags in MainLayout.razor
```
<SectionOutlet SectionId="GUID_e96086ae15e1442fb441eeb571dff754">
</SectionOutlet>
```
- Define the SectionOutlet object
```
@code 
{
    public static SectionOutlet GUID_e96086ae15e1442fb441eeb571dff754 = new();
}
```

Define the content to replace the placeholder
- Define the content to replace the placeholder
```
<SectionContent SectionId="MainLayout.GUID_e96086ae15e1442fb441eeb571dff754">
    <span>Weather SectionContent</span>
</SectionContent>
```
- Insert in Home.razor the SectionContent pointing to the SectionOutlet defined in MainLayout.razor
```
<SectionContent SectionId="MainLayout.GUID_e96086ae15e1442fb441eeb571dff754">
    <span>Home SectionContent</span>
</SectionContent>
```

### Media
---
![image](https://github.com/user-attachments/assets/ecf14a8c-68aa-49b2-b488-cdc3ae1adb0e)
---
![image](https://github.com/user-attachments/assets/49b06bc7-c475-4734-a3e0-62b0a9183643)
---
![image](https://github.com/user-attachments/assets/be6570d5-9501-446e-a920-21f3cf5d1a2c)


### References
---
- [[ASP.NET Core Blazor sections](https://#)](https://github.com/ViCunha/e575-Lab-Windows-Localhost-BlazorWebApp-Sections)
