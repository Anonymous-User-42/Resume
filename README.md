# Resume LaTeX Template Guide

This LaTeX resume template is based on [Jake Ryan Gutierrez's work](https://github.com/jakegut/resume), customized to suit a professional resume format. It allows easy customization through predefined sections and commands, simplifying the process of adding and maintaining resume content.

## File Structure

- **main.tex**: The main LaTeX file containing the entire resume content, formatting, and custom commands.
- **README.md**: This guide explains the usage of the LaTeX commands defined in the template and the format of the resume.

## Prerequisites

To compile this LaTeX template, ensure you have the following packages installed:

- `fullpage`
- `titlesec`
- `marvosym`
- `color`
- `enumitem`
- `hyperref`
- `fancyhdr`
- `tabularx`

You can install these using your LaTeX distribution or package manager.

## Resume Format

The resume template follows a clean and modern format, with sections including:

- **Personal Information**: Your name, contact details, and LinkedIn or GitHub links.
- **Experience**: List of your past jobs, internships, and the responsibilities or accomplishments in those roles.
- **Education**: Degrees, universities, and years attended.
- **Skills**: Technical skills and tools you are proficient in.
- **Projects**: Detailed descriptions of relevant personal or professional projects.

## Custom LaTeX Commands

The resume template introduces several custom LaTeX commands to simplify content management. Below is a breakdown of each command, its purpose, and an example of usage.

### `\resumeItem{Title}{Description}`

- **Description**: Adds a bullet point under a specific job or project description, where you can list specific tasks or achievements.
- **Usage**:
  ```latex
  \resumeItem{Implemented REST APIs}{Developed and deployed RESTful APIs using Flask, improving data access speed by 30%.}
  ```
- This command takes two parameters: the title of the task and a brief description of it.

### `\resumeSection{Section Title}`

- **Description**: Creates a new section in the resume, such as "Experience" or "Education."
- **Usage**:

  ```latex
  \resumeSection{Experience}
  ```

- The section will be underlined and styled uniformly for consistency.

### `\resumeSubheading{Title}{Organization}{Location}{Date}`

- **Description**: Creates a subheading for a job, degree, or project. It displays the role or degree title, the organization or university, the location, and the time period.
- **Usage**:
  ```latex
  \resumeSubheading{Software Engineer Intern}{XYZ Corporation}{San Francisco, CA}{June 2023 - August 2023}
  ```
- Parameters:

  - #1: Job or degree title
  - #2: Organization or university name
  - #3: Location
  - #4: Dates

### `\resumeSubItem{Description}`

- **Description**: Adds an indented bullet point under a subheading to describe detailed tasks or achievements related to a job or project.
- **Usage**:
  ```latex
  \resumeSubItem{Optimized SQL queries to reduce report generation time by 50%.}
  ```

### `\resumeSubHeadingListStart` and `\resumeSubHeadingListEnd`

- **Description**: Used to create a list of subitems under a subheading, grouping multiple tasks or achievements together.
- **Usage**:
  ```latex
  \resumeSubHeadingListStart
  \resumeSubItem{Created a user authentication system using JWT.}
  \resumeSubItem{Collaborated with a team of 4 engineers to integrate microservices.}
  \resumeSubHeadingListEnd
  ```
- This defines the start and end of the list for organizing the description points.

## Example Section Using Custom Commands

- Here’s an example of how to create a full "Experience" section using the custom commands:

  ```latex
  \resumeSection{Experience}

  \resumeSubheading{Software Engineer Intern}{XYZ Corporation}{San Francisco, CA}{June 2023 - August 2023}
  \resumeSubHeadingListStart
  \resumeSubItem{Developed and maintained RESTful APIs using Python and Flask.}
  \resumeSubItem{Increased system efficiency by 20% by optimizing database queries.}
  \resumeSubItem{Collaborated with a team of engineers to implement cloud-based microservices.}
  \resumeSubHeadingListEnd

  \resumeSubheading{Web Developer}{Freelance}{Remote}{January 2022 - May 2023}
  \resumeSubHeadingListStart
  \resumeSubItem{Built responsive websites using HTML, CSS, and JavaScript for small businesses.}
  \resumeSubItem{Integrated e-commerce functionalities and payment gateways.}
  \resumeSubHeadingListEnd
  ```

- This example will create a section for work experience, listing two jobs and the relevant tasks performed.

## Additional Notes

### Adjusting Page Layout

- The template adjusts margins and page size for a clean, single-page resume. You can modify these settings by editing the following commands in the preamble of the LaTeX file:

  ```latex
  \addtolength{\oddsidemargin}{-0.5in}
  \addtolength{\textwidth}{1in}
  ```

- These lines tweak the side margins and text width. You can further customize the layout if necessary.
