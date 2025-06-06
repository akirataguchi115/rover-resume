<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="/img/Rover-black-bg.png">
    <img alt="Daytona logo" src="/img/Rover-white-bg.jpg" width="60%">
  </picture>
</div>

This repository offers a collection of simple yet effective résumé templates built using basic LaTeX commands. The BASE ROVER template, for instance, requires only about 10 lines of code to set up a clean and minimal résumé format. Unlike other templates that rely on custom résumé classes — forcing you to learn new commands and options — these templates are designed to be straightforward and easy to use.


## Motivation

Creating a one-page résumé shouldn't require 500+ lines of code filled with custom commands that are difficult to modify or troubleshoot. Frustrated by the complexity and lack of simplicity in existing templates, I set out to design a clean and intuitive solution. This template is built with basic design principles in mind like *Hierarchy*, *Repetition*, and *Alignment* to ensure a professional and visually appealing result without unnecessary complexity. 

The following code block serves as the foundational structure for each entry in your résumé.

```latex
\subsection{Designation, Duration}
\subsubsection{Company, Location}
\begin{itemize}
  \item Bullet points  
  \item tailored to the
  \item job description.
\end{itemize}
```

## Screenshots

| [![Base Rover](/img/base-rover.jpg)](/templates/base%20rover/) | [![Star Rover](/img/star-rover.jpg)](/templates/star%20rover/) | 
|:----:|:-----:|
| Base Rover Template | Star Rover Template |

| [![Week Rover](/img/monday.jpg)](/templates/week%20rover/main-rover.tex) | [![Week Rover](/img/office-rover.jpg)](/templates/office%20rover/office-rover.tex) | 
|:----:|:-----:|
| Monday - Week Rover | Office Rover |

| [![Milky Rover](/img/milky-rover.jpg)](/templates/milky%20rover/) | [![Fancy Rover](/img/fancy-rover.jpg)](/templates/fancy%20rover/) | 
|:----:|:-----:|
| Milky Rover Template | Fancy Rover Template |

*Milky Rover Template is a recreation of [Butterick’s practical typography](https://practicaltypography.com/resumes.html) résumé template.



## Features
- Single or Double lined title option.
- Multiple ways to format the Name & Contact info banner.
- ATS friendly.
- Works with pre-installed LaTeX fonts. 
- Uses `article` class. No need to learn the working of any custom class.
- Uses typographic best practices. 
- Your content looks clean and structured.


## Quick start
[Edit on Overleaf](https://www.overleaf.com/latex/templates/rover-resume/bpzqtssvfgsn). Or just copy paste the code into your favorite LaTeX editor.

## Getting Started
1. **Get the Repository**: Fork or Download this repository to your local machine.   
2. **Select a Template**: Choose a template from the available options.
3. **Fill in Your Details**: Personalize the template by filling in your information.


### Tips for Using LaTeX Commands
- **Sectioning**: Use `\section` for major sections like Education, Experience, Certifications, Awards, Skills & Interests, etc.
- **Subsectioning**: Employ `\subsection{}` and `\subsubsection` for primary and secondary titles such as Institution Name, Position Title, Duration, etc.
- **Bullet Points**: Use `itemize` lists for creating bullet points.


## Known Issue

<details>

<summary>Package hyperref Warning:</summary>

This occurs because `hyperref` package creates clickable texts for both internal and external links. When generating a PDF, certain elements like bookmarks, metadata, and hyperlinks are encoded as **PDF strings**. Since `\section{}`, `\subsection{}` etc. are used in the *Table of contents* (i.e. bookmarks), certain LaTeX commands (like `\hfill`) or control sequences doesn't make sense in this context.

When `hyperref` encounters the `\hfill` command while processing a piece of text that needs to be converted into a PDF string, it cannot include this command in the output PDF string. As a result, it removes the command and issues a warning to notify you of this action. 

We can circumvents this issue by disabling the creation of bookmarks as shown below.


```latex
    \usepackage[bookmarks=false]{hyperref}
```

</details>


> [!CAUTION]
> To avoid generating warnings, the `bookmarks` option in the `hyperref` package must be set during package loading with `\usepackage[bookmarks=false]{hyperref}`. You can use `\hypersetup{}` for everything else.


## Support

For inquiries or assistance, visit the [Discussions](https://github.com/subidit/rover-resume/discussions) tab.

Feel free to contribute to the project or provide feedback by opening an issue or submitting a pull request. 

Happy job hunting!


## License

<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"><br><a property="dct:title" rel="cc:attributionURL" href="https://github.com/subidit/rover-resume">Rover Resume</a> by <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://github.com/subidit/">Subidit</a> is licensed under <a href="http://creativecommons.org/licenses/by/4.0/" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY 4.0</a></p>
