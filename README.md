# Staff42 Community Website
Welcome to the official repository for the Staff42 community website. This site is built with Hugo, a fast and modern static site generator, and is designed to serve as a platform for French staff-plus engineers to share knowledge, insights, and experiences through blogging articles.

## Requirements

[Install hugo](https://gohugo.io/installation/) on your laptop:
```bash
# macos
brew install hugo

# using snap
sudo snap install hugo
```

## Quickstart with Hugo
To get started with Hugo and contribute to the Staff42 website, you'll need to have Hugo installed on your machine. If you haven't already, you can follow the instructions on the Hugo installation page.

Once Hugo is installed, you can clone the repository and start the Hugo server:

```bash
# Clone the repository
git clone --recursive git@github.com:staffeng42/staffeng42.github.io.git

# Navigate to the repository folder
cd staffeng42.github.io

# Start the Hugo server
hugo server
```

You should now be able to see the site running locally on `http://localhost:1313/`.

## Contributing
We welcome contributions from all members of the Staff42 community. Here's how you can contribute:

### Reporting Issues
If you find any bugs or have a feature request, please use the Issues section of this repository to let us know.

### Submitting Articles
To submit an article:

1. Fork the repository.
2. Create a new branch for your article.
3. Add your article as a new markdown file in the `content/posts` directory.
4. Commit your changes with a clear message describing the article.
5. Push your changes to your fork.
6. Submit a pull request to the main repository.
7. Please ensure your article follows the content guidelines:

- Write in French, as it is the primary language of the Staff42 community.
- Keep your content relevant to staff-plus engineers.
- Provide valuable insights or information.
- Maintain a professional tone.

### Review Process
All submissions will go through a review process by the Staff42 editorial team. We aim to provide feedback or merge your contributions quickly.

## Directory Structure
Here's a brief overview of the key directories in this Hugo project:

`content/`: Contains the markdown files for the blog posts.
`themes/`: Contains the Hugo theme used for the site.
`static/`: Contains static files such as images and CSS.
`config.toml`: The main configuration file for the Hugo site.
Building the Site
To build the static pages for the website, run:

```bash
hugo -D
```

The generated HTML and assets will be in the public/ directory, ready to be deployed.

# Deployment
The Staff42 website is automatically deployed when changes are merged into the main branch. Our CI/CD pipeline handles the build and deployment processes.

# Support
If you need help or have questions about using Hugo or contributing to the website, please reach out to the community maintainers or open a discussion in the Discussions section of this repository.

# License
This project is licensed under the MIT License - see the LICENSE.md file for details.

Thank you for being a part of the Staff42 community and for your interest in contributing to our website. Together, we can make this a valuable resource for all staff-plus engineers.