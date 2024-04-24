# Remix Routing

## What Are Routes?

Think of routes like signposts on a road. They tell you where to go to find what you're looking for. In Remix, these signposts are organized in a particular way.

### Basic Routing

Every page on your website has a corresponding signpost in the `routes` folder.

#### Example:

- `root.tsx`: The main signpost at the entrance of your site. It's what people see when they first arrive.
  - `// Example: Represents the homepage (http://yourwebsite.com/)`
- `index.tsx`: The central signpost in a specific area of your site, like the lobby of a hotel.
  - `// Example: For blog section (http://yourwebsite.com/blog)`
- `about.tsx`: A signpost pointing to a specific spot, like the 'About Us' plaque next to an office door.
  - `// Example: Directs to About page (http://yourwebsite.com/about)`

### Layout Routes

Layout routes provide the general design that wraps around different pages, like the frame of a painting.

#### Example:

- `__layout.tsx`: The framework that holds everything in the `routes` folder together visually.
  - `// Example: Common header and footer for all pages under a path`

### Optional Segments

Optional segments are like having an open door that can be used if needed, but it's okay if it's not.

#### Example:

- `[username]?.tsx`: A path that works with or without a username.
  - `// Example: User profile page, accessible with or without specifying a username (http://yourwebsite.com/users/ or http://yourwebsite.com/users/johndoe)`

### Splat Routes

Splat routes are like catch-all baskets for when someone ends up somewhere unexpected.

#### Example:

- `$.tsx`: A generic signpost for when no specific direction fits.
  - `// Example: Custom "Page Not Found" for undefined paths (http://yourwebsite.com/anything)`

### Escape Routes

Escape routes are for when a page needs to break away from the common design, like a secret passage that bypasses the main hallway.

#### Example:

- `__about.tsx`: This page will not use the common layout even if it's nested within a path that normally would.
  - `// Example: A unique About page that doesn't share the common layout (http://yourwebsite.com/special/about)`

### Using Folders

Folders help keep things tidy, grouping related pages together like books on a shelf.

#### Example:

- `/blog/`: A folder that contains all blog-related pages, like individual posts, categories, etc.
  - `// Example: Structure for blog posts (http://yourwebsite.com/blog/post-title)`

### Special Files (Escaped Routes)

Some files are meant for downloading, not viewing. Remix makes sure these don't get mixed up with regular pages.

#### Example:

- `__download.pdf.tsx`: A PDF file that's available for download but isn't displayed like a typical page.
  - `// Example: Direct link to a PDF (http://yourwebsite.com/files/download.pdf)`

With these examples, you can see how Remix sets up the roadmap for your website, guiding users to the right destination smoothly and efficiently.

[Remix File-Based Routing Documentation](https://remix.run/docs/en/main/file-conventions/routes)
