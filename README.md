# Birthday Card Website

A simple and elegant website for creating and sharing digital birthday cards.

## Features

- Create personalized birthday cards
- Responsive design for all devices
- Easy-to-use interface
- Customizable templates

## Getting Started

### Prerequisites

- Web browser
- Text editor (optional for customization)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/web-dev-scrim/birthday-card-website.git
```

2. Navigate to the project directory:
```bash
cd birthday-card-website
```

3. Open `index.html` in your web browser

## Deployment

### Deploy to Netlify

1. Push your code to a GitHub repository
2. Go to [Netlify](https://netlify.com) and sign up/login
3. Click "New site from Git"
4. Choose "GitHub" as your Git provider
5. Select your repository
6. Configure build settings:
  - Build command: (leave empty for static sites)
  - Publish directory: `/` (or the folder containing your index.html)
7. Click "Deploy site"
8. Your site will be available at a Netlify URL (e.g., `https://your-site-name.netlify.app`)


### Automatic deploys after PR merge (GitHub Actions → Netlify)

This repo includes a GitHub Actions workflow that builds with Vite and deploys to Netlify on pushes to `main`.

Setup steps:

1. In Netlify, create a new site and grab the following:
  - Site ID: Site settings → General → Site details → Site ID
  - Personal access token: User settings → Applications → New access token
2. In your GitHub repo, go to Settings → Secrets and variables → Actions → New repository secret, and add:
  - `NETLIFY_SITE_ID` = your Netlify Site ID
  - `NETLIFY_AUTH_TOKEN` = your Netlify personal access token
3. Ensure your default branch is `main`. When a PR is merged to `main`, the workflow will:
  - Install deps
  - Build the site (`npm run build`)
  - Deploy the contents of `dist` to Netlify production

Notes:
- The workflow file is at `.github/workflows/deploy-netlify.yml`.
- `netlify.toml` is included to mirror the same build and publish settings on Netlify.
- If you use a different Node version or build output directory, update the workflow accordingly.

### Custom Domain (Optional)

1. In your Netlify dashboard, go to "Domain settings"
2. Click "Add custom domain"
3. Follow the instructions to configure your DNS

## Usage

1. Open the website in your browser
2. Choose a card template
3. Customize the message and design
4. Share your birthday card

## Contributing

1. Fork the project
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## License

This project is licensed under the MIT License.