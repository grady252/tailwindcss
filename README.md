# tailwindcss

Use tailwindcss v4 with ASP.NET Core.

Note: This project is **not** affiliated with the official tailwindcss project.

## Install

```bash
dotnet add package tailwindcss
```

This package will automatically run the tailwind standalone cli on build and output a `{ASSEMBLY NAME}.tailwind.css`, similar to ASP.NET core's css isolation.
Add the following to your html file, with 'ASSEMBLY NAME' replaced with the name of your project.

```html
<link rel="stylesheet" href="{ASSEMBLY NAME}.tailwind.css" />
```

## Customize

The default css file that is used just contains the import tailwind directive.

```css
/* input.css */
@import "tailwindcss";
```

You can provide your own input file to customize tailwind specify the `TailwindInputFile` paramater in your project file. You can also customize the output path with the `TailwindOutputFile` paramater in your project file

```xml
<!-- example.csproj -->
<PropertyGroup>
  <TailwindInputFile>example.css</TailwindInputFile>
  <TailwindOutputFile>site.css</TailwindOutputFile>
</PropertyGroup>
```

```css
/* example.css */
@import "tailwindcss";
```
