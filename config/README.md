# Settings Configuration

## Files

### `settings_data.baseline.json`

- **Purpose**: Clean baseline settings for distribution
- **Use**: Starting point for new stores or theme sales
- **Tracked**: ✅ Committed to git
- **Contains**: Default Wig Shop Pro theme settings without store-specific customizations

### `settings_data.json`

- **Purpose**: Dev store specific settings for testing
- **Use**: Local development and testing on your dev store
- **Tracked**: ❌ Ignored by git (in `.gitignore`)
- **Contains**: Your custom settings, test data, and dev store configurations

## Usage

### For New Store Setup

1. Copy `settings_data.baseline.json` to `settings_data.json`
2. Customize as needed for the specific store

### For Development

- Edit `settings_data.json` freely - changes won't be committed
- Only update `settings_data.baseline.json` when you want to change the default distribution settings

### For Theme Distribution/Sale

- Use `settings_data.baseline.json` as the clean starting point
- Ensure it contains sensible defaults without store-specific data
