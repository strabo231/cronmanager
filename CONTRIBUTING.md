# Contributing to CronManager

Thanks for your interest! 🎉

## Reporting Bugs

- Check existing issues first
- Include your OS/bash version
- Provide the command you ran
- Include error messages
- Show your crontab (if relevant)

## Suggesting Features

- Explain the use case
- Describe how it would work
- Consider if it fits the project scope

## Pull Requests

1. Fork the repo
2. Create feature branch
3. Test thoroughly
4. Follow existing code style
5. Update README if needed
6. Submit PR with clear description

## Testing

```bash
# Test without modifying your crontab
chmod +x cronman
./cronman --help
./cronman examples
./cronman validate "0 2 * * *"

# Test with a separate user (safer)
# Or backup first: crontab -l > backup.txt
```

## Code Style

- 4 spaces indentation
- Clear variable names
- Comment complex logic
- Follow existing patterns

## License

By contributing, you agree your contributions will be licensed under MIT.
