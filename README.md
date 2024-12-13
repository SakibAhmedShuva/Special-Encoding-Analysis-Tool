# Special Encoding Analysis Tool

A robust Python utility for analyzing text files containing special characters, Unicode encodings, and non-ASCII content. This tool is particularly useful for natural language processing tasks, text preprocessing, and identifying encoding-related issues in text data.

## Features

- Comprehensive special character detection and analysis
- Detailed Unicode character information including names and categories
- Token-level analysis for words containing special characters
- Frequency counting of special character occurrences
- Support for specific character set detection (German umlauts, Greek letters, etc.)
- Robust error handling and detailed logging

## Requirements

- Python 3.6+
- Standard library modules:
  - `re` (regular expressions)
  - `collections` (for Counter)
  - `logging` (for output handling)
  - `unicodedata` (for Unicode character analysis)

## Installation

Clone the repository:

```bash
git clone https://github.com/SakibAhmedShuva/Special-Encoding-Analysis-Tool.git
cd Special-Encoding-Analysis-Tool
```

No additional package installation is required as the tool uses Python standard library modules only.

## Usage

### Basic Usage

```python
from special_encoding_analyzer import read_text_file, analyze_text_tokens

# Read and analyze a text file
text = read_text_file('path/to/your/file.txt')
if text:
    token_results = analyze_text_tokens(text)
```

### Advanced Usage

```python
from special_encoding_analyzer import check_specific_special_chars, detect_character_set

# Read the text file
text = read_text_file('path/to/your/file.txt')

if text:
    # Check for specific special characters
    specific_chars = check_specific_special_chars(text)
    
    # Analyze complete character set
    char_set = detect_character_set(text)
    
    # Perform token analysis
    token_results = analyze_text_tokens(text)
```

## Output Format

The tool provides detailed analysis through logging output:

1. **Input Text Statistics**
   - Total character count
   - Basic text metrics

2. **Special Characters Details**
   - Unicode name and category for each special character
   - Character frequency counts

3. **Token Analysis**
   - Total and unique token counts
   - Frequency distribution of tokens containing special characters

4. **Character Set Analysis**
   - Comprehensive list of all non-ASCII characters
   - Unicode information for each character

## Functions

### `read_text_file(file_path)`
Reads a text file with UTF-8 encoding and proper error handling.

### `check_specific_special_chars(text)`
Checks for predefined special characters (German umlauts, Greek letters, etc.).

### `analyze_text_tokens(text)`
Performs comprehensive token-level analysis of text containing special characters.

### `detect_character_set(text)`
Analyzes and categorizes all unique characters in the text.

## Error Handling

The tool includes robust error handling for:
- File reading issues
- Encoding problems
- Unicode character recognition
- Invalid input text

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

[Sakib Ahmed Shuva](https://github.com/SakibAhmedShuva)

## Acknowledgments

- Inspired by the need for robust text analysis in multilingual NLP projects
- Built to handle complex Unicode and special character scenarios in text processing
