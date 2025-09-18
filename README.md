# Sourceable

An open source click tracking platform built with Laravel and React.

## Getting Started

### Local Development with Laravel Sail

This project uses Laravel Sail for local development, which provides a complete Docker environment.

#### Prerequisites

- [Docker Desktop](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

#### Installation

```bash
# 1. Fork the repository and clone your fork
git clone <your-fork-url>

# 2. Navigate to the project directory
cd sourceable

# 3. Install PHP dependencies
./vendor/bin/sail composer install

# 4. Copy the environment file
cp .env.example .env

# 5. Start the application with Sail
./vendor/bin/sail up -d

# 6. Generate application key
./vendor/bin/sail artisan key:generate

# 7. Run database migrations
./vendor/bin/sail artisan migrate

# 8. Install frontend dependencies
./vendor/bin/sail npm install

# 9. Start the NPM development server
./vendor/bin/sail npm run dev
```

The application will be available at `http://localhost`.

#### Development Commands

- Start all services: `./vendor/bin/sail up -d`
- Stop all services: `./vendor/bin/sail down`
- View logs: `./vendor/bin/sail logs`
- Run tests: `./vendor/bin/sail artisan test`
- Access the container: `./vendor/bin/sail shell`

For convenience, you can create a shell alias:
```bash
alias sail='sh $([ -f sail ] && echo sail || echo vendor/bin/sail)'
```

Then use `sail` instead of `./vendor/bin/sail` for all commands.

## License

Sourceable is open-sourced software licensed under the [Apache 2.0 license](LICENSE).

## Support

- **Documentation**: [GitHub Wiki](https://github.com/thecodedad/sourceable/wiki)
- **Issues**: [GitHub Issues](https://github.com/thecodedad/sourceable/issues)
- **Discussions**: [GitHub Discussions](https://github.com/thecodedad/sourceable/discussions)
