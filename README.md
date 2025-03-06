# Hosting a Resume as a Static Website

## Purpose
This README file is a step-by-step instruction on the process of formatting and hosting a resume using a static website. It is intended for beginners like Marvin McLaren, the Foomatic finance manager, who have basic understanding of Markdown but no prior experience with Git, static site generators or forges. By the end of this guide Marvin should have a working static website hosting his resume using forge.

## Prerequisites
Before starting, make sure you have the following:   
- A resume
- A basic understanding of Markdown (refer to Further Resources if needed).
- A Github account (or an account on another forge like Gitlab or Codeberg).
- Git installed on your system.
- A text editor
- A static site generator installed (e.g., Pelican, Jekyll or Hugo).

## Instructions

### 1. Convert Your Resume to Markdown

- **Why Use Markdown?**   
As told by Andrew Etter in _Modern Technical Writing_, lightweight markup languages are Markdown are easy to learn, human readable and widely supported by static site generators. Markdown allows users to focus on content without having to learn complex syntax. Hence why Markdown is preferred over HTML and other document formats like Word or LaTex.

- **Steps**
    1. Open a text editor of your choice.
    2. Convert your resume using Markdown syntax. For example:
        - Use **\#** for headings. (e.g., \# Adnan)
        - Use **\**** for bold text. (e.g., \*\*bold**)
        - Use **\_** or **\*** for italic text. (e.g., \_italic_ or \*italic*)
        - Use **\***** for bold and italic text. (e.g., \*\*\*bold&italic***)
    3. Save file as **resume.md**.

### 2. Set Up Git Repository
- **Why Use Git?**   
Andrew Etter advocates for distributed version control systems like Git since Git allows for seamless collaboration, version tracking and offline work. Git works well with static site generators like Pelican, Jekyll, Hugo. Git is by the most popular system, supported by all forges and some machines come with pre installed Git. Gits like Github Pages allow for free and easy hosting, which is a huge selling point.

- **Steps**   
    1. Install Git: **https://git-scm.com/**
    2. Create an account on Github.
    3. Create a new repository. (e.g, example)
    4. Clone the repository to your local machine.

### 3. Choose a Static Site Generator
- **Why a Static Site Generator?**   
In _Modern Technical Writing_, Andrew Etter goes into detail on why he loves static websites. He says static websites are fast, simple, portable, secure and can be hosted practically anywhere. Moving a static site is extremely easy since there are no server-side application dependencies, no database and nothing to install. They also allow to separate content from design, making updates straightforward.

- **Steps**   
    1. Install Python since we are using Pelican, which is a Python based static site generator. **https://www.python.org/**
    2. Install Pelican with Markdown support.  
    `python -m pip install "pelican[markdown]"`
    3. Optional, but recommended: install make   
    Windows: **https://stackoverflow.com/q/32127524**   
    macOS: **https://stackoverflow.com/q/1469994**
    4. Initialize a new Pelican project to create a new website.   
    `pelican-quickstart`
    5. Follow the prompts to configure your site.
    6. Add your **resume.md** file to the **content** directory.
    7. Generate the HTML version of the website.   
    `pelican content`
    8. Preview the website locally.  
    `pelican --listen`
    9. Point your browser to **http://127.0.0.1:8000/**

### 4. Host the Site on a Forge
- **Why Use Forges?**
Forges like GitHub, GitLab, and Codeberg offer free static web hosting services (e.g., GitHub Pages). Andrew Etter in _Modern Technical Writing_ recommends to host documentation online for easy updates and accessibility.

- **Steps**
    1. Push your static site files to your Git repository.
    2. Enable GitHub Pages in your repository settings:
        - Go to **Settings** > **Pages**
        - Select the main branch and the docs folder (or root folder) as the               source.
    3. Visit the provided URL to see your live resume.

### 5. Write a README File
- **Why Write a README File?**  
For any project a README file is essential to guide users through your project. As William S. Pfeiffer explain in _Technical Communication_, when writing technical documentations, instructions should be clear, concise, and structured with numbered steps. The README file should include a title, set of prerequisites, set of numbered instructions, further resources/reading including links to relevant resources, a FAQ section and credits listing contributors. 

- **Steps**
    1. Create a **README.md** file.
    2. Place it in your root directory.
    3. Follow the ABC format (Abstract, Body, Conclusion) as outlined in               William S. Pfeiffer's _Technical Communication_:
        - **Abstract:** Provide an overview of the project and its purpose.
        - **Body::** Include detailed instructions, grouped under task                     headings.
        - **Conclusion:** Summarize the successful outcome and provide                     additional resources.

## Further Resourses
Following are some resources to help further your understanding of Markdown, static site generators and forges.

- [Markdown Guide](https://www.markdownguide.org/getting-started/)
- [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/) 
- [Git Documentation](https://git-scm.com/doc)
- [Pelican Documentation](https://docs.getpelican.com/en/latest/)
- [Github Pages Guide](https://pages.github.com)

## FAQ

### 1. Why is Markdown better than writing raw HTML?
Compared to HTML, Markdown is simpler and more readable. Less complex syntax allows you to focus on content, making it easier to maintain and update your documentation.

### 2. I changed the Markdown version of my resume, so why don’t I see the changes when I refresh the website in my browser?
After changes are made static site generators need to rebuild the site to apply changes. Run the generator commands, `pelican content` to rebuild the site and `pelican --listen` to preview the website locally. Now you should be able to see the changes.

### 3. Do I need to know how to code to use Markdown and static site generators? 
No, coding experience is not essential for building a static site using Markdown. Markdown is designed to be simple and human readable, with easy to learn syntax. Static site generators like Pelican, Hugo or Jekyll handle the technical parts, which allows you to focus on the content.

## Credits
- **Fawaz Saleem** and **Daniel Gorban** for in-class peer review.
- **Andrew Etter** for the principles outlined in _Modern Technical Writing_.
- **William S. Pfeiffer** for the instruction guidelines in _Technical Communication_.