# Coolify Compose Collection

A curated collection of Docker Compose files and documentation for use with [Coolify.io](https://coolify.io) - the open-source & self-hosted Heroku/Netlify alternative.

## 🎯 Purpose

This repository serves multiple purposes:

1. Archive default Coolify one-click service configurations
2. Provide custom compose files optimized for Coolify
3. Share documentation and guides for common deployment patterns
4. Maintain scripts and tools for Coolify management

## 📁 Repository Structure

```
.
├── coolify-defaults/     # Official Coolify one-click configurations
├── custom/              # Custom compose configurations
├── docs/                # Guides and documentation
│   ├── databases/      # Database setup guides
│   ├── deployment/     # Deployment patterns
│   └── examples/       # Example configurations
└── scripts/            # Helper scripts and tools
```

## 🚀 Getting Started

### Prerequisites

- A running [Coolify instance](https://coolify.io/docs/installation)
- Basic understanding of Docker Compose
- Familiarity with Coolify's UI and concepts

### Using Compose Files

1. Choose a compose file from either `coolify-defaults/` or `custom/`
2. Create a new service in Coolify using "Docker Compose" as the source
3. Paste the compose configuration
4. Configure environment variables through Coolify's UI
5. Deploy!

## 📚 Documentation

### Database Guides

- [PostgreSQL with External Access](docs/databases/postgresql-external.md)
- [Database Backup Strategies](docs/databases/backup-strategies.md)

### Deployment Patterns

- [NextJS + PostgreSQL Stack](docs/deployment/nextjs-postgres.md)
- [Moving from Vercel to Coolify](docs/deployment/vercel-migration.md)

## 🔧 Features

- Optimized for Coolify's UI components
- Database backup integration
- Service-specific configuration fields
- Environment variable management
- Health check implementations

## 🤝 Contributing

Contributions are welcome! Please read our [Contributing Guide](CONTRIBUTING.md) for details on:

- Code of Conduct
- Submission process
- Compose file standards
- Documentation guidelines

## ⚠️ Security

- Never commit sensitive data or secrets
- Use Coolify's UI for managing sensitive environment variables
- Follow security best practices in compose configurations

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔗 Resources

- [Coolify Documentation](https://coolify.io/docs)
- [Docker Compose Documentation](https://docs.docker.com/compose/)
- [Coolify GitHub Repository](https://github.com/coollabsio/coolify)
