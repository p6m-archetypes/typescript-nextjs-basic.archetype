# TypeScript Next.js Application Archetype

![Latest Release](https://img.shields.io/github/v/release/p6m-archetypes/typescript-nextjs-basic.archetype?style=flat-square&label=Latest%20Release&color=blue)

Modern Next.js application archetype with TypeScript, App Router, Server Components, and Kubernetes deployment configuration.

## 🎯 What This Generates

This archetype creates a Next.js application with:

- **⚡ Next.js 14+**: React framework with App Router and Server Components
- **🎨 TypeScript**: Full type safety across the application
- **🚀 Rendering Strategies**: SSR, SSG, and ISR support for optimal performance
- **🐳 Container-Ready**: Docker and Kubernetes deployment manifests
- **🧪 Testing Setup**: Jest and React Testing Library configured
- **🎯 ESLint & Prettier**: Code quality and formatting tools
- **📦 Modern Tooling**: Turbopack for fast development builds

## 📦 Generated Project Structure

```
my-customer-frontend/
├── app/                    # Next.js App Router pages and layouts
├── components/             # React components
├── lib/                    # Utility functions and shared logic
├── public/                 # Static assets
├── styles/                 # CSS modules and global styles
├── tests/                  # Test files
├── k8s/                    # Kubernetes manifests
├── Dockerfile
├── next.config.js
└── package.json
```

## 🚀 Quick Start

### Prerequisites

- [Archetect](https://archetect.github.io/) CLI tool
- Node.js 18+ and npm
- Docker (optional, for containerized deployment)

### Generate a New Application

```bash
archetect render https://github.com/p6m-archetypes/typescript-nextjs-basic.archetype.git#v1

# Example prompt answers:
# organization-name: acme-inc
# project-title: Customer Portal
# project-prefix: customer
# Result: customer-frontend/
```

### Development Workflow

```bash
cd customer-frontend

# 1. Install dependencies
npm install

# 2. Run development server
npm run dev

# 3. Run tests
npm test

# 4. Build for production
npm run build

# 5. Start production server
npm start

# 6. Access application
# - Development: http://localhost:3000
```

## 📋 Configuration Prompts

| Property | Description | Example |
|----------|-------------|---------|
| `organization-name` | GitHub organization or username | acme-inc |
| `project-title` | Display name for the application | Customer Portal |
| `project-prefix` | Project identifier (suffix '-frontend' added automatically) | customer |

## ✨ Key Features

### 🏛️ Next.js Features

- **App Router**: Modern file-based routing with layouts and nested routes
- **Server Components**: React Server Components by default for better performance
- **API Routes**: Built-in API endpoints for backend functionality
- **Middleware**: Request/response middleware for auth, redirects, and headers
- **Image Optimization**: Next.js Image component with automatic optimization
- **Font Optimization**: Automatic web font optimization

### 🎨 Developer Experience

- **TypeScript**: Full type safety with strict mode
- **Hot Reload**: Fast refresh during development with Turbopack
- **ESLint**: Configured with Next.js recommended rules
- **Prettier**: Code formatting with pre-commit hooks
- **Path Aliases**: Import aliasing configured (@/components, @/lib, etc.)
- **Environment Variables**: .env file support with type safety

### 🧪 Testing

- **Jest**: Unit testing framework with Next.js configuration
- **React Testing Library**: Component testing utilities
- **Test Coverage**: Coverage reporting configured
- **E2E Ready**: Can integrate Playwright or Cypress for end-to-end tests

### 🚢 Deployment

- **Docker**: Multi-stage Dockerfile optimized for production
- **Kubernetes**: Deployment, Service, and Ingress manifests
- **Environment Variables**: Runtime and build-time environment support
- **Static Export**: Option for static site generation
- **Edge Runtime**: Support for edge functions and middleware

## 🎯 Use Cases

This archetype is ideal for:

1. **Customer-Facing Applications**: Public websites requiring SEO optimization
2. **Admin Dashboards**: Internal tools with server-side rendering
3. **Marketing Sites**: Content-heavy sites with SSG for best performance
4. **E-commerce Platforms**: Product catalogs with dynamic and static pages
5. **Progressive Web Apps**: Applications with offline support and app-like features

## 📚 What's Inside

### Core Configuration

#### Next.js Configuration
Pre-configured `next.config.js` with image optimization, environment variables, and build settings for production deployment.

#### TypeScript Configuration
Strict TypeScript setup with path aliases (@/ imports) and optimized compiler options for Next.js development.

#### Styling
CSS Modules configured with optional support for Tailwind CSS, Sass, or styled-components.

### Development Tools

- **ESLint**: Next.js and TypeScript rules for code quality
- **Prettier**: Consistent code formatting across the project
- **Husky**: Git hooks for pre-commit quality checks
- **VS Code Settings**: Recommended extensions and editor configuration

## 🔧 Next.js-Specific Features

### Rendering Strategies

- **SSR (Server-Side Rendering)**: Dynamic pages rendered on each request for real-time data
- **SSG (Static Site Generation)**: Pre-rendered pages at build time for maximum performance
- **ISR (Incremental Static Regeneration)**: Hybrid approach with page revalidation
- **Client-Side Rendering**: Traditional React rendering when appropriate

### Performance Optimization

- **Automatic Code Splitting**: Route-based code splitting for faster page loads
- **Image Optimization**: Responsive images with lazy loading and WebP format
- **Font Optimization**: Automatic font subsetting and preloading
- **Bundle Analysis**: webpack-bundle-analyzer configured for size monitoring

### API Routes

Built-in API endpoints for:
- Backend-for-Frontend (BFF) patterns
- Authentication and session management
- Third-party API proxying
- Database queries and data fetching

## 📋 Validation

Build and test the generated application:

```bash
npm run build && npm test
```

## 🔗 Related Archetypes

- **[TypeScript Nuxt.js](../typescript-nuxtjs-basic.archetype)** - Vue.js alternative to Next.js with SSR
- **[TypeScript Angular](../typescript-angular-basic.archetype)** - Full-featured Angular framework
- **[TypeScript Svelte](../typescript-svelte-basic.archetype)** - Lightweight compiled framework
- **[Java GraphQL Gateway](../java-spring-boot-graphql-domain-gateway.archetype)** - Backend gateway this app can consume

## 🤝 Contributing

For issues or enhancements, create detailed bug reports or feature requests in the repository.

## 📄 License

MIT License

---

**Ready to build modern web applications with Next.js?** Generate your first app and start building! 🚀
