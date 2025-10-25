## About this Project

This project is a personal academic website built with the [Academic Pages Jekyll theme](https://github.com/academicpages/academicpages.github.io). It is a static site hosted on GitHub Pages. The content is written in Markdown, and the structure is defined by Jekyll's conventions and the theme's specific layout.

### Key Architectural Concepts

*   **Jekyll Static Site:** The entire site is compiled into static HTML, CSS, and JavaScript. There is no server-side code running in production.
*   **Content as Data:** The site's content (publications, talks, portfolio items) is managed in collections within directories like `_publications`, `_talks`, and `_posts`. Each item is a Markdown file with extensive YAML front matter that provides structured metadata.
*   **Configuration-driven:** The site's appearance, navigation, and metadata are heavily controlled by YAML configuration files. The main configuration is in `_config.yml`, with navigation defined in `_data/navigation.yml`.
*   **Layouts and Includes:** The HTML structure is modular. `_layouts` define the main page templates (e.g., `single.html` for a single post), and `_includes` contain reusable components like the footer (`footer.html`) and author profile (`author-profile.html`).

### Development Workflow

**Local Development (Docker Recommended):**

The easiest way to run the site locally is with Docker, which avoids Ruby and Jekyll dependency issues.

1.  Make sure Docker is running.
2.  Run the following command in the terminal:
    ```bash
    docker compose up
    ```
3.  The site will be available at `http://localhost:4000` and will automatically reload when you make changes to content files.

**Adding and Modifying Content:**

*   **Create New Content:** To add a new publication, talk, or blog post, create a new Markdown file in the appropriate collection directory (e.g., `_publications/2023-10-27-my-new-paper.md`).
*   **YAML Front Matter is Crucial:** The block at the top of each Markdown file (between the `---` lines) is critical. It defines all the metadata for the content item. For example, a publication requires fields like `title`, `collection`, `permalink`, `date`, `venue`, and `citation`. Refer to existing files in the collections for examples.
    *Example from `_publications/2024-02-17-paper-title-number-4.md`:*
    ```yaml
    ---
    title: "Paper Title Number 4"
    collection: publications
    category: conferences
    permalink: /publication/2024-02-17-paper-title-number-4
    excerpt: 'This paper is about fixing template issue #693.'
    date: 2024-02-17
    venue: 'GitHub Journal of Bugs'
    paperurl: 'https://academicpages.github.io/files/paper3.pdf'
    citation: 'Your Name, You. (2024). &quot;Paper Title Number 3.&quot; <i>GitHub Journal of Bugs</i>. 1(3).'
    ---
    ```
*   **Site Configuration:**
    *   To change your name, bio, social media links, or profile picture, edit `_config.yml`.
    *   To change the top navigation bar, edit `_data/navigation.yml`.

### Important Files and Directories

*   `_config.yml`: The main Jekyll configuration file. Contains site-wide settings, author information, and collection definitions.
*   `_data/`: Contains structured data files, most importantly `navigation.yml`.
*   `_pages/`: Standalone pages like the "About" or "CV" page.
*   `_posts/`, `_publications/`, `_talks/`, `_teaching/`, `_portfolio/`: These directories hold the collections of content for the site.
*   `assets/`: Contains static assets like CSS, JavaScript, and images.
*   `docker-compose.yaml` & `Dockerfile`: Used to create a consistent, containerized development environment.
*   `Gemfile`: Lists the Ruby dependencies (Jekyll plugins) for the project.
