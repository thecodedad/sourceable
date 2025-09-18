# Sourceable

An open source click tracking platform built with Laravel and React.

## Getting Started

### Local Development with Laravel Sail

This project uses Laravel Sail for local development, which provides a complete Docker environment.

#### Prerequisites

- [Docker Desktop](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

#### Installation

1. Fork the repository and clone your fork:
   ```bash
   git clone <your-fork-url>
   ```

2. Install PHP dependencies:
   ```bash
   ./vendor/bin/sail composer install
   ```

3. Copy the environment file:
   ```bash
   cp .env.example .env
   ```

4. Start the application with Sail:
   ```bash
   ./vendor/bin/sail up -d
   ```

5. Generate application key:
   ```bash
   ./vendor/bin/sail artisan key:generate
   ```

6. Run database migrations:
   ```bash
   ./vendor/bin/sail artisan migrate
   ```

7. Install frontend dependencies:
   ```bash
   ./vendor/bin/sail npm install
   ```

8. Start the NPM development server:
   ```bash
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
