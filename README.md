# Docker Nginx Setups

This repository is used to version and manage different Docker-based Nginx setups across multiple hosts.

## Repository Structure

Each branch represents a different host-specific Nginx setup.

- `main` contains the base Docker Nginx setup.
- Host-specific branches contain configuration changes for individual servers.
- Runtime files such as logs are ignored and should not be committed.
- Site-specific Nginx configs can be added per host branch as needed.

## Branch Strategy

### `main`

The `main` branch is the shared base setup. It should contain only common Docker, Nginx, and directory structure files that are useful across all hosts.

Use `main` for:

- Base `docker-compose.yml`
- Base `nginx.conf`
- Common folder structure
- Placeholder files such as `.gitkeep`
- Shared defaults

### Host Branches

Each host should have its own branch.

Example:

```bash
git checkout -b ajvn-server
