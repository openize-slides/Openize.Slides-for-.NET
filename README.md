# Openize.Slides for .NET | Free C# PowerPoint API
[Openize.Slides for .NET](https://github.com/openize-slides/Openize.Slides-for-.NET) - An open-source library offered by [openize.com](https://www.openize.com/) that can help beginners create, open, and edit PowerPoint files.

## Contents
- [Overview](#net-powerpoint-api-for-presentation-manipulation)
- [System Requirements](#system-requirements)
- [Get Started](#quick-start)
- [How To?](#how-to)
- [Find More](#find-more)

## .NET PowerPoint API for Presentation Manipulation 

[Openize.Slides](https://github.com/openize-slides/Openize.Slides-for-.NET) is a freely available .NET library crafted for MS PowerPoint presentation manipulation and management. Whether you're a novice or an expert, this API is straightforward to set up and utilize. Its strength lies in the powerful OpenXML engine, which serves as the backbone of Openize.Slides. By incorporating this C# library, you can easily generate and control PowerPoint files programmatically. Once integrated, you won't require any additional third-party tools to automate the creation or modification of PowerPoint presentations.

## System Requirements
- .NET Core 3.1 and above
  
## Quick Start
  > ```Install-Package Openize.Slides```
```
// Open a presentation
Presentation presentation = Presentation.Open("sample.pptx");

// Get 1st slides
Slide slide = presentation.GetSlides()[0];

// Get text shape count
var shapeCount = slide.TextShapes.Count;
```


## How to?
> **Create Presentation:**
```
// Create instance of presentation
Presentation presentation = Presentation.Create("sample.pptx");
//Create instances of text shapes and set their texts.
TextShape shape = new TextShape();
shape.Text = "Title: Here is my first title From FF";
TextShape shape2 = new TextShape();
shape2.Text = "Body : Here is my first title From FF";    
// Set yAxis of 2nd text shape
shape2.Y = 25.9;
// Create slide
Slide slide = new Slide();
// Add text shapes.
slide.AddTextShapes(shape);
slide.AddTextShapes(shape2);               
// Adding slides
presentation.AppendSlide(slide); 
// Save presentation
presentation.Save();
```
## Find More
> **More Samples:**
  Check out the [examples](https://github.com/openize-slides-gists/Openize.Slides-for-.NET/) for sample code snippets to begin with.

> **Usage:**
- Explore the [documentation](https://openize-slides.github.io/Openize.Slides-for-.NET/index.html).
- Read out [API References](https://openize-slides.github.io/Openize.Slides-for-.NET/api/Openize.Slides.html) to get In-depth information about available classes and methods.
- [Openize](https://www.openize.com/) offers you to find comprehensive [blog posts](https://blog.openize.com/) on commonly trending PowerPoint presentation manipulation topics 

  
> **Contribution:**
If you find issues or have improvements, feel free to open a [GitHub issue](https://github.com/openize-slides/Openize.Slides-for-.NET/issues) or submit a [pull request](https://github.com/openize-slides/Openize.Slides-for-.NET/pulls).
> **License:**
This project is licensed under the MIT License - see the [LICENSE file](https://github.com/openize-slides/Openize.Slides-for-.NET/blob/main/LICENSE) for details.




