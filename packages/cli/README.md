# @stackweld/cli

[![Version](https://img.shields.io/badge/version-0.3.0-blue.svg)](https://github.com/mundowise/Stackweld/releases)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

The Stackweld CLI. Define, validate, scaffold, and launch development environments from the terminal.

## Installation

```bash
npm install -g @stackweld/cli
```

Requires Node.js >= 22.0.0.

## Usage

Run `stackweld` with no arguments to open the interactive menu:

```bash
stackweld
```

The wizard guides you through creating a project, browsing technologies, checking compatibility, and more — no commands to memorize.

### Common commands

```bash
# Create a new project interactively
stackweld init

# Generate a project in one shot
stackweld generate \
  --name "my-app" \
  --path "/home/user/projects" \
  --techs "nextjs,fastapi,postgresql,redis,docker" \
  --profile production \
  --git

# Scaffold from a built-in template
stackweld create t3-stack --path /home/user/projects

# Check compatibility between two technologies
stackweld score nextjs prisma

# Audit an existing project
stackweld health ./my-app

# Check system requirements
stackweld doctor

# Generate shell completions
stackweld completion bash   # or zsh, fish
```

### All 38 commands

| Command | Description |
|---------|-------------|
| `stackweld init` | Interactive stack creation wizard |
| `stackweld generate` | One-shot project generation |
| `stackweld create <id>` | Scaffold from a template |
| `stackweld list` | List saved stacks |
| `stackweld info <id>` | Show stack or technology details |
| `stackweld browse` | Browse technology catalog |
| `stackweld browse --templates` | Browse templates |
| `stackweld doctor` | Check system requirements |
| `stackweld doctor --suggest` | Suggest fixes for missing tools |
| `stackweld up` | Start Docker services |
| `stackweld down` | Stop Docker services |
| `stackweld down --volumes` | Stop and remove volumes |
| `stackweld status` | Show running service status |
| `stackweld logs [service]` | View service logs |
| `stackweld logs -f` | Follow log output |
| `stackweld export <id>` | Export stack to YAML or JSON |
| `stackweld import <file>` | Import stack from file |
| `stackweld save <id>` | Save version snapshot |
| `stackweld delete <id>` | Delete a stack |
| `stackweld clone <id>` | Duplicate a stack |
| `stackweld scaffold <id>` | Generate project files from saved stack |
| `stackweld version list <id>` | Show version history |
| `stackweld version diff <id> <a> <b>` | Compare two versions |
| `stackweld version rollback <id> --to <v>` | Rollback to version |
| `stackweld template list` | List built-in templates |
| `stackweld template save <id>` | Save stack as custom template |
| `stackweld template saved` | List your custom templates |
| `stackweld template use-custom <id>` | Create from custom template |
| `stackweld config list` | Show preferences |
| `stackweld config set <key> <value>` | Set a preference |
| `stackweld ai suggest "<desc>"` | Get stack suggestion from description |
| `stackweld ai readme <id>` | Generate README from stack |
| `stackweld ai explain <id>` | Explain stack architecture |
| `stackweld completion <shell>` | Generate shell completions (bash/zsh/fish) |
| `stackweld score <techA> [techB]` | Compatibility score between technologies |
| `stackweld analyze [path]` | Detect stack from existing project |
| `stackweld benchmark <id>` | Performance profile for a stack |
| `stackweld cost <id>` | Estimate monthly hosting costs |

See the [full command reference](https://github.com/mundowise/Stackweld/wiki) for all flags and options.

## Requirements

- Node.js >= 22.0.0
- Docker + Docker Compose (for `up`, `down`, `status`, `logs` commands)

## Repository

[github.com/mundowise/Stackweld](https://github.com/mundowise/Stackweld)

## License

MIT
