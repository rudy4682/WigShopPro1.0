# GitHub Copilot Instructions for Wig Shop Pro

## Project Overview

Wig Shop Pro is a professional Shopify theme based on Dawn 15.4.0, customized for wig shops and hair product businesses.

## Development Guidelines

### Commit Policy

**IMPORTANT**: Only commit changes after full testing and completion of the requested change.

- DO NOT commit partial or incomplete work
- Test all changes thoroughly before committing
- Verify functionality works as expected
- Run theme checks before committing

### Code Quality Standards

#### Linting and Formatting

- All Markdown files must pass linting with no errors
- Follow proper Markdown formatting rules:
  - Headings surrounded by blank lines
  - Lists surrounded by blank lines
  - Fenced code blocks surrounded by blank lines
  - Use consistent ordered list prefixes
  - Fix all MD022, MD031, MD032 errors

#### Line Endings

- Ensure proper line endings (LF for git, CRLF handled automatically on Windows)
- Files should be saved with UTF-8 encoding
- No trailing whitespace

### Shopify Theme Development

#### Theme Check

Always run theme check before committing:

```bash
shopify theme check
```

Fix all warnings and errors:

- UndefinedObject warnings
- UnusedAssign warnings
- VariableName warnings (use snake_case)
- No false positives should remain unaddressed

#### Liquid Best Practices

- Initialize variables before use
- Use snake_case for variable names (e.g., `anchor_id` not `anchorId`)
- Remove unused variables
- Follow Shopify Liquid standards

### File Management

#### Settings Files

- `config/settings_data.baseline.json` - Tracked in git, clean defaults
- `config/settings_data.json` - Ignored by git, local dev settings only

Never commit `config/settings_data.json` to the repository.

#### Documentation

- Update README.md when adding major features
- Keep release-notes.md current
- Document complex functionality in code comments

### Testing Workflow

1. Make requested changes
2. Run `shopify theme check`
3. Fix all linting errors
4. Test functionality locally
5. Verify no regressions
6. Review all changed files
7. Only then commit with descriptive message
8. Push to repository

### Git Commit Messages

Use clear, descriptive commit messages:

- Start with action verb (Add, Update, Fix, Remove)
- Be specific about what changed
- Reference issue numbers if applicable

Examples:

- ✅ "Add product variant selector for wig types"
- ✅ "Fix mobile menu overflow on small screens"
- ✅ "Update color scheme for brand consistency"
- ❌ "updates"
- ❌ "fix stuff"

### Theme Branding

This theme is branded as "Wig Shop Pro":

- Theme name: Wig Shop Pro
- Author: Adams Computer & Network
- Repository: rudy4682/WigShopPro1.0

Do not reference "Dawn" in user-facing content except in attribution or technical documentation.

### Performance Considerations

- Maintain Dawn's performance-first approach
- Minimize JavaScript usage
- Use native web standards where possible
- Optimize images and assets
- Keep bundle sizes small

### Accessibility

- Maintain WCAG 2.1 AA compliance
- Use semantic HTML
- Ensure keyboard navigation works
- Test with screen readers
- Proper ARIA labels

## Common Tasks

### Adding New Features

1. Create feature branch (optional for solo dev)
2. Implement feature
3. Test thoroughly
4. Run theme check
5. Update documentation if needed
6. Commit with clear message

### Fixing Bugs

1. Reproduce the bug
2. Identify root cause
3. Implement fix
4. Test fix and verify no side effects
5. Run theme check
6. Commit with "Fix:" prefix

### Updating Baseline Settings

Only update `settings_data.baseline.json` when changing defaults for distribution:

1. Make changes in admin theme editor
2. Export settings
3. Update baseline file
4. Test with fresh store
5. Commit with explanation

## Resources

- [Shopify Theme Development](https://shopify.dev/docs/themes)
- [Liquid Reference](https://shopify.dev/docs/api/liquid)
- [Dawn Documentation](https://github.com/Shopify/dawn)
- [Theme Check](https://shopify.dev/docs/themes/tools/theme-check)

## Questions?

For issues or questions, create an issue in the [GitHub repository](https://github.com/rudy4682/WigShopPro1.0/issues).
