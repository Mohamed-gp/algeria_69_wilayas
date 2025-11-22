# Contributing to Algeria 69 Wilayas Dataset

First off, thank you for considering contributing to this project! 🎉

## How Can I Contribute?

### Reporting Errors

If you find any errors in the data:

1. **Check existing issues** to see if it's already reported
2. **Create a new issue** with:
   - Wilaya ID and name
   - What's incorrect
   - The correct information (with sources if possible)
   - Any additional context

### Suggesting Enhancements

We welcome suggestions for:

- Additional data fields
- Better organization
- New features
- Documentation improvements

### Data Corrections

When submitting corrections:

1. **Provide sources**: Links to official sources, maps, or documentation
2. **Be specific**: Include exact coordinates, names, or values
3. **Explain**: Why the current data is incorrect

### Pull Requests

1. Fork the repository
2. Create a new branch (`git checkout -b feature/improvement`)
3. Make your changes
4. Test your changes (ensure JSON is valid)
5. Commit with clear messages (`git commit -am 'Fix coordinates for Algiers'`)
6. Push to your branch (`git push origin feature/improvement`)
7. Open a Pull Request

### Data Quality Guidelines

When contributing data:

#### Coordinates

- Use decimal degrees format
- Minimum 4 decimal places for accuracy
- Verify coordinates point to the wilaya capital
- Check on OpenStreetMap or Google Maps

#### Names

- Official names only
- Include both English and Arabic
- Use proper diacritics and spelling

#### Population Data

- Use latest available estimates
- Include source year
- Round to nearest thousand for estimates

#### Notable Features

- Focus on major landmarks, heritage sites, or economic activities
- Keep descriptions concise
- Verify information is current

### Code Style

For JSON:

- Use 2 spaces for indentation
- Keep consistent formatting
- Validate JSON before committing

### Commit Messages

Use clear, descriptive commit messages:

- ✅ Good: "Update Algiers population to 2025 estimate"
- ✅ Good: "Correct coordinates for Tamanrasset"
- ❌ Bad: "Fixed stuff"
- ❌ Bad: "Update"

### Testing Changes

Before submitting:

1. **Validate JSON**: Use a JSON validator
2. **Check formatting**: Ensure consistent indentation
3. **Verify data**: Double-check your changes
4. **Test usage**: Try loading in a simple script

### What We're Looking For

Priority contributions:

1. **Coordinate verification** for new 2025 wilayas
2. **Additional metadata** (tourist sites, historical info)
3. **Economic data** (main industries, agriculture)
4. **Cultural information** (languages, traditions)
5. **Infrastructure data** (airports, ports, universities)
6. **Natural features** (mountains, rivers, parks)

### Questions?

Feel free to:

- Open an issue for discussion
- Ask questions in pull requests
- Suggest new ideas

## Recognition

Contributors will be acknowledged in:

- README.md acknowledgments section
- Release notes for their contributions

Thank you for helping make this dataset better! 🇩🇿
