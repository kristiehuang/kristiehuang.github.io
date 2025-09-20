# kristiehuang.github.io

Personal website and blog built with Jekyll and hosted on GitHub Pages.

## Prerequisites

Before you begin, ensure you have the following installed on your system:

1. **Ruby** (version 2.5.0 or higher)

   - Check your version: `ruby -v`
   - Install Ruby: [ruby-lang.org](https://www.ruby-lang.org/en/documentation/installation/)

2. **RubyGems** (usually comes with Ruby)

   - Check your version: `gem -v`

3. **Bundler** (Ruby package manager)
   - Install: `gem install bundler`

## Installation

1. **Clone the repository** (or navigate to your local copy):

   ```bash
   git clone https://github.com/kristiehuang/kristiehuang.github.io.git
   cd kristiehuang.github.io
   ```

2. **Install dependencies**:

   ```bash
   bundle install
   ```

   This will install Jekyll and all required gems specified in the Gemfile.

## Running the Site Locally

1. **Start the Jekyll development server**:

   ```bash
   bundle exec jekyll serve
   ```

   Or with live reload enabled:

   ```bash
   bundle exec jekyll serve --livereload
   ```

2. **View the site**:

   - Open your browser and navigate to: `http://localhost:4000`
   - The site will automatically rebuild when you make changes to files

3. **Stop the server**:
   - Press `Ctrl + C` in the terminal

## Common Commands

### Build the site

Generate the static site without serving it:

```bash
bundle exec jekyll build
```

### Serve with drafts

Include draft posts from the `_drafts` folder:

```bash
bundle exec jekyll serve --drafts
```

### Update dependencies

Update all gems to their latest versions:

```bash
bundle update
```

### Check for errors

Build the site and check for any errors:

```bash
bundle exec jekyll build --verbose
```

## Project Structure

```
.
├── _config.yml          # Site configuration
├── _posts/             # Blog posts (YYYY-MM-DD-title.markdown)
├── _layouts/           # Page layouts
├── _includes/          # Reusable components
├── _site/              # Generated static site (git ignored)
├── assets/             # Images, CSS, and other assets
├── images/             # Additional images
├── blog.markdown       # Blog listing page
├── index.markdown      # Home page
├── work.markdown       # Work/portfolio page
├── resume.markdown     # Resume page
├── more-on-me.markdown # About page
├── Gemfile            # Ruby dependencies
└── Gemfile.lock       # Locked dependency versions
```

## Creating New Posts

1. Create a new file in the `_posts` directory
2. Name it following the format: `YYYY-MM-DD-title.markdown`
3. Add front matter at the top:

   ```markdown
   ---
   layout: post
   title: "Your Post Title"
   date: YYYY-MM-DD HH:MM:SS -0500
   categories: blog
   ---

   Your content here...
   ```

## Configuration

Site settings can be modified in `_config.yml`. Common settings include:

- `title`: Site title
- `description`: Site description
- `baseurl`: Subpath if not serving from root
- `url`: Production URL

**Note**: After changing `_config.yml`, you need to restart the Jekyll server for changes to take effect.

## Deployment

This site is configured for GitHub Pages deployment:

1. **Automatic deployment**: Push changes to the `master` branch
2. **GitHub Pages will automatically build and deploy the site**
3. **Custom domain**: Configured via the `CNAME` file

## Troubleshooting

### Common Issues

1. **Port already in use**:

   ```bash
   bundle exec jekyll serve --port 4001
   ```

2. **Dependency issues**:

   ```bash
   bundle install
   bundle update
   ```

3. **Build errors**:

   - Check for syntax errors in markdown files
   - Ensure front matter is properly formatted
   - Run `bundle exec jekyll build --trace` for detailed error messages

4. **macOS specific issues**:
   If you encounter issues with native extensions on macOS, try:
   ```bash
   bundle config build.nokogiri --use-system-libraries
   bundle install
   ```

## Additional Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Minima Theme Documentation](https://github.com/jekyll/minima)

## License

© Kristie Huang. All rights reserved.
