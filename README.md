initAV.com WebsiteThis repository contains the source code for the official website of initAV, a freelance software development startup. The website serves as a public-facing portfolio and a primary point of contact for clients, showcasing our modern and professional approach to web development.The website's design philosophy is centered on mobile-first, responsive, and minimalistic principles, ensuring a fast, accessible, and clean user experience across all devices.Project OverviewThis is a static website built with Jekyll and styled using Tailwind CSS. The site provides a comprehensive overview of initAV's services, showcases a portfolio of past projects, and includes a blog to share insights on software development and technology. The goal is to provide a clear and professional online presence that highlights our expertise and capabilities.PagesHome: The landing page that provides a brief introduction to initAV's services and core values.Services: A detailed page outlining the software development services offered, such as web application development, custom software solutions, and consulting.Portfolio: A gallery of previous projects with descriptions, technologies used, and links to live demos or repositories.About: Information about the company's background, mission, and the people behind initAV.Contact: A form for potential clients to get in touch. The form uses Formspree to handle submissions without server-side code.Blog: A page that automatically lists blog posts from the _posts folder, allowing for easy content management via Markdown.Technology StackStatic Site Generator (SSG): JekyllStyling: Tailwind CSSCSS Preprocessor: PostCSS for building TailwindHosting: GitHub PagesForm Handling: FormspreeFrontend: HTML, CSS, and optional JavaScript for interactive elementsFolder Structure.
├── _includes/
│   ├── head.html       # Head section for all pages
│   ├── header.html     # Responsive navigation header
│   ├── footer.html     # Site footer
│   └── scripts.html    # Optional JS for interactive elements
├── _layouts/
│   ├── default.html    # Main layout template
│   ├── page.html       # Layout for general pages
│   └── post.html       # Layout for blog posts
├── _posts/
│   └── 2024-05-15-example-post.md
├── assets/
│   ├── css/
│   │   └── main.css    # PostCSS output file
│   └── js/
│       └── main.js     # Custom JavaScript
├── _config.yml         # Jekyll configuration file
├── index.html          # Home page
├── services.html       # Services page
├── portfolio.html      # Portfolio page
├── about.html          # About page
├── contact.html        # Contact page
└── tailwind.config.js
Design GuidelinesMobile-First Approach: All pages should be designed and styled for small screens first. Use Tailwind's responsive prefixes (sm:, md:, lg:) to progressively enhance the layout for larger viewports.Tailwind CSS: Use Tailwind utility classes for all styling, including layout, typography, spacing, and responsiveness. Avoid writing custom CSS where possible.Responsive Header/Footer: The navigation should collapse into a hamburger menu or similar mobile-friendly format on small screens. The footer should stack elements vertically on mobile.Adaptive Grids: The portfolio and blog post listings should use responsive grid layouts (e.g., using Tailwind's grid-cols-1, sm:grid-cols-2, md:grid-cols-3) that adapt gracefully to different screen sizes.Development WorkflowLocal DevelopmentThis project uses a standard Jekyll and Tailwind workflow.Dependencies: Ensure you have Ruby, Jekyll, Node.js, and npm installed.Jekyll: Run bundle install to get the necessary Ruby gems.Tailwind: Navigate to the project root and run npm install to install Tailwind and PostCSS.AI IntegrationWe use GitHub Copilot as a primary tool to accelerate development. It is highly effective for:Generating page layouts from simple comments (e.g., <!-- A responsive portfolio grid with 3 columns -->).Suggesting _posts front-matter and content outlines.Auto-completing Tailwind CSS classes and Jekyll Liquid tags.Docker EnvironmentFor a consistent and isolated development environment, you can use Docker.Build: Ensure Docker is running and build the image with docker compose build.Run: Start the local server with docker compose up. This will make the site available at http://localhost:4000.Notes for Contributors / AI ContextReusable Layouts: Use _layouts/default.html as the base for all pages to maintain a consistent structure. Page-specific content should be placed within the {{ content }} tag.Blog Posts: Blog posts must be Markdown files located in the _posts/ directory and follow the Jekyll naming convention (YYYY-MM-DD-title.md). Front-matter is required at the top of each file to define metadata like title, author, and date.Mobile-First Design: Remember to always prioritize mobile layout and styles. This is a core tenet of this project's design.Commands# Install Node.js dependencies
npm install

# Build Tailwind CSS for production
npm run build:tailwind

# Watch for changes and recompile Tailwind
npm run watch:tailwind

# Install Ruby dependencies
bundle install

# Serve the site locally with Jekyll
bundle exec jekyll serve

# Serve the site using Docker
docker compose up

# Stop the Docker container
docker compose down
ReferencesJekyll DocumentationTailwind CSS DocumentationGitHub Pages DocumentationUsing Docker with Jekyll
