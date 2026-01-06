# Contributing to MCP Manager

Thank you for your interest in contributing to MCP Manager! We welcome contributions from the community.

## 🚀 Getting Started

### Prerequisites

- [.NET 10.0 SDK](https://dotnet.microsoft.com/download/dotnet/10.0)
- Git
- A code editor (VS Code, Visual Studio, Rider, etc.)

### Setting Up Your Development Environment

1. Fork the repository
2. Clone your fork:
   ```bash
   git clone https://github.com/YOUR_USERNAME/McpManager.git
   cd McpManager
   ```
3. Add the upstream remote:
   ```bash
   git remote add upstream https://github.com/JerrettDavis/McpManager.git
   ```
4. Restore dependencies:
   ```bash
   dotnet restore
   ```
5. Build the project:
   ```bash
   dotnet build
   ```
6. Run tests:
   ```bash
   dotnet test
   ```

## 📝 How to Contribute

### Reporting Bugs

If you find a bug, please create an issue using the [Bug Report template] and include:
- Clear description of the bug
- Steps to reproduce
- Expected vs actual behavior
- Environment details (OS, .NET version, etc.)

### Suggesting Features

For feature requests, use the [Feature Request template] and describe:
- The problem you're trying to solve
- Your proposed solution
- Any alternatives you've considered

### Submitting Pull Requests

1. **Create a branch** from `main`:
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make your changes**:
   - Follow the existing code style
   - Write clear, concise commit messages
   - Add tests for new functionality
   - Update documentation as needed

3. **Run tests locally**:
   ```bash
   dotnet test
   ```

4. **Commit your changes**:
   ```bash
   git add .
   git commit -m "feat: add your feature description"
   ```
   
   We follow [Conventional Commits](https://www.conventionalcommits.org/):
   - `feat:` for new features
   - `fix:` for bug fixes
   - `docs:` for documentation changes
   - `test:` for test changes
   - `chore:` for maintenance tasks
   - `refactor:` for code refactoring

5. **Push to your fork**:
   ```bash
   git push origin feature/your-feature-name
   ```

5. **Open a Pull Request** on GitHub using the [PR template]

## 🏷️ Versioning (Automated!)

**Zero Developer Overhead - Fully Automated!**

We use [Semantic Versioning](https://semver.org/) with **100% automated version management**. You don't touch `version.json` - our CI does it!

### How It Works

1. **Title your PR with conventional commits**
2. **Workflow automatically**: Detects bump type → Updates version.json → Commits to your PR → Validates
3. **On merge to main**: Creates tag → Builds release → Publishes artifacts

### PR Title Format

```
<type>[scope][!]: <description>

Examples:
feat: add server discovery         → 0.1.0 → 0.2.0 (MINOR)
fix: resolve routing bug            → 0.1.0 → 0.1.1 (PATCH)
feat!: redesign API                 → 0.1.0 → 1.0.0 (MAJOR)
```

### Version Bump Rules

| PR Title Pattern | Bump | Example |
|-----------------|------|---------|
| `feat!:` or `BREAKING` | **MAJOR** | 0.1.0 → 1.0.0 |
| `feat:` or label `feature` | **MINOR** | 0.1.0 → 0.2.0 |
| `fix:`, `chore:`, `docs:`, etc. | **PATCH** | 0.1.0 → 0.1.1 |

### Commit Types

- `feat`: New feature (minor)
- `fix`: Bug fix (patch)
- `docs`: Documentation (patch)
- `style`, `refactor`, `perf`, `test`, `chore`, `ci`: Other (patch)

Add `!` for breaking: `feat!:` or `fix!:` → **MAJOR** bump

### What You DON'T Do

❌ Edit `version.json` manually  
❌ Create tags  
❌ Calculate versions  
❌ Worry about conflicts  

### What Happens Automatically

✅ Version detection from PR title/labels  
✅ `version.json` auto-update in your PR  
✅ Version validation  
✅ Helpful PR comments  
✅ Tag creation on merge  
✅ Release builds  

See the automated comment on your PR for version details!

## 🏗️ Project Structure

```
McpManager/
├── src/
│   ├── McpManager.Core/           # Domain models and interfaces
│   ├── McpManager.Application/    # Business logic and services
│   ├── McpManager.Infrastructure/ # Agent connectors and registries
│   └── McpManager.Web/            # Blazor Server web application
├── tests/
│   └── McpManager.Tests/          # Unit and integration tests
├── docs/                          # Documentation
└── .github/                       # GitHub workflows and templates
```

## 🎯 Coding Guidelines

### General Guidelines

- Follow [C# coding conventions](https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions)
- Use meaningful variable and method names
- Keep methods small and focused (Single Responsibility Principle)
- Write unit tests for new code
- Document public APIs with XML comments

### Architecture Guidelines

- Follow **Clean Architecture** principles
- Keep dependencies flowing inward (Core → Application → Infrastructure/Web)
- Use interfaces for abstraction (`IAgentConnector`, `IServerRegistry`, etc.)
- Implement new agent connectors by extending `IAgentConnector`

### Testing Guidelines

- Write tests using xUnit
- Follow the Arrange-Act-Assert pattern
- Use descriptive test names: `MethodName_Scenario_ExpectedBehavior`
- Mock external dependencies
- Aim for high code coverage

Example test:
```csharp
[Fact]
public void GetAgents_WhenCalled_ReturnsAllAgents()
{
    // Arrange
    var service = new AgentService();
    
    // Act
    var agents = service.GetAgents();
    
    // Assert
    Assert.NotNull(agents);
    Assert.NotEmpty(agents);
}
```

## 🔄 Development Workflow

1. **Sync your fork** before starting work:
   ```bash
   git fetch upstream
   git checkout main
   git merge upstream/main
   ```

2. **Create a feature branch** for your work

3. **Make small, focused commits** as you work

4. **Push regularly** to your fork to backup your work

5. **Open a PR** when ready for review

6. **Address feedback** from reviewers

7. **Celebrate** when your PR is merged! 🎉

## 🧪 Running Tests

```bash
# Run all tests
dotnet test

# Run with coverage
dotnet test /p:CollectCoverage=true

# Run specific test
dotnet test --filter "FullyQualifiedName~YourTestName"
```

## 📚 Additional Resources

- [Clean Architecture by Robert C. Martin](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)
- [SOLID Principles](https://en.wikipedia.org/wiki/SOLID)
- [Model Context Protocol Specification](https://modelcontextprotocol.io/)
- [.NET Documentation](https://docs.microsoft.com/en-us/dotnet/)
- [Blazor Documentation](https://docs.microsoft.com/en-us/aspnet/core/blazor/)

## 📜 Code of Conduct

Be respectful and inclusive. We want to maintain a welcoming environment for all contributors.

## 📄 License

By contributing, you agree that your contributions will be licensed under the MIT License.

Thank you for contributing to MCP Manager! 🙏
