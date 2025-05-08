FROM node:20-alpine AS base

# Install pnpm
RUN corepack enable && corepack prepare pnpm@latest --activate

# Set up workspace
WORKDIR /app

# Build stage
FROM base AS builder
# Copy only package files first to leverage Docker caching
COPY pnpm-lock.yaml ./
COPY package.json ./

# Install dependencies (with caching)
RUN pnpm fetch 

# Copy application code
COPY . .

# Install with offline mode (using cache)
RUN pnpm install --frozen-lockfile --offline

# Build the application
RUN pnpm build

# Production stage
FROM base AS runner
WORKDIR /app

# Copy necessary files from builder
COPY --from=builder /app/next.config.js ./
COPY --from=builder /app/public ./public
COPY --from=builder /app/.next ./.next
COPY --from=builder /app/package.json ./
COPY --from=builder /app/pnpm-lock.yaml ./

# For standalone output mode (if configured)
# COPY --from=builder /app/.next/standalone ./

# Only copy production dependencies
RUN pnpm install --prod --frozen-lockfile

EXPOSE 3000
CMD ["pnpm", "start"]
