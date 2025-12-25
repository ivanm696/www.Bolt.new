
Navigation Menu
bolt.new

Code
Pull requests
bolt.new
/CONTRIBUTING.md
kKaskak
kKaskak
last year
110 lines (69 loc) · 5.26 KB

Preview

Code

Blame
Bolt Open Source Codebase

Welcome to the Bolt open-source codebase! This repo contains a simple example app using the core components from bolt.new to help you get started building AI-powered software development tools powered by StackBlitz’s WebContainer API.

Why Build with Bolt + WebContainer API
By building with the Bolt + WebContainer API you can create browser-based applications that let users prompt, run, edit, and deploy full-stack web apps directly in the browser, without the need for virtual machines. With WebContainer API, you can build apps that give AI direct access and full control over a Node.js server, filesystem, package manager and dev terminal inside your users browser tab. This powerful combination allows you to create a new class of development tools that support all major JavaScript libraries and Node packages right out of the box, all without remote environments or local installs.

What’s the Difference Between Bolt (This Repo) and Bolt.new?
Bolt.new: This is the commercial product from StackBlitz—a hosted, browser-based AI development tool that enables users to prompt, run, edit, and deploy full-stack web applications directly in the browser. Built on top of the Bolt open-source repo and powered by the StackBlitz WebContainer API.

Bolt (This Repo): This open-source repository provides the core components used to make Bolt.new. This repo contains the UI interface for Bolt as well as the server components, built using Remix Run. By leveraging this repo and StackBlitz’s WebContainer API, you can create your own AI-powered development tools and full-stack applications that run entirely in the browser.

Get Started Building with Bolt
Bolt combines the capabilities of AI with sandboxed development environments to create a collaborative experience where code can be developed by the assistant and the programmer together. Bolt combines WebContainer API with Claude Sonnet 3.5 using Remix and the AI SDK.

WebContainer API
Bolt uses WebContainers to run generated code in the browser. WebContainers provide Bolt with a full-stack sandbox environment using WebContainer API. WebContainers run full-stack applications directly in the browser without the cost and security concerns of cloud hosted AI agents. WebContainers are interactive and editable, and enables Bolt's AI to run code and understand any changes from the user.

The WebContainer API is free for personal and open source usage. If you're building an application for commercial usage, you can learn more about our WebContainer API commercial usage pricing here.

Remix App
Bolt is built with Remix and deployed using CloudFlare Pages and CloudFlare Workers.

AI SDK Integration
Bolt uses the AI SDK to integrate with AI models. At this time, Bolt supports using Anthropic's Claude Sonnet 3.5. You can get an API key from the Anthropic API Console to use with Bolt. Take a look at how Bolt uses the AI SDK

Prerequisites
Before you begin, ensure you have the following installed:

Node.js (v20.15.1)
pnpm (v9.4.0)
Setup
Clone the repository (if you haven't already):
git clone https://github.com/stackblitz/bolt.new.git
Install dependencies:
pnpm install
Create a .env.local file in the root directory and add your Anthropic API key:
ANTHROPIC_API_KEY=XXX
Optionally, you can set the debug level:

VITE_LOG_LEVEL=debug
Important: Never commit your .env.local file to version control. It's already included in .gitignore.

Available Scripts
pnpm run dev: Starts the development server.
pnpm run build: Builds the project.
pnpm run start: Runs the built application locally using Wrangler Pages. This script uses bindings.sh to set up necessary bindings so you don't have to duplicate environment variables.
pnpm run preview: Builds the project and then starts it locally, useful for testing the production build. Note, HTTP streaming currently doesn't work as expected with wrangler pages dev.
pnpm test: Runs the test suite using Vitest.
pnpm run typecheck: Runs TypeScript type checking.
pnpm run typegen: Generates TypeScript types using Wrangler.
pnpm run deploy: Builds the project and deploys it to Cloudflare Pages.
Development
To start the development server:

pnpm run dev
This will start the Remix Vite development server.

Testing
Run the test suite with:

pnpm test
Deployment
To deploy the application to Cloudflare Pages:

pnpm run deploy
Make sure you have the necessary permissions and Wrangler is correctly configured for your Cloudflare account.
