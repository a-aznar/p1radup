# URL Parameter Deduplicator (paradup)

## Overview

This Python script is designed to process a list of URLs from an input file, remove duplicate query parameters, and save the modified URLs to an output file. The primary goal is to ensure that each unique parameter is included only once for each distinct hostname.

## Features

- **Duplicate Query Parameter Removal:** The script identifies duplicate query parameters within each URL and retains only the first occurrence of each parameter for a given hostname.

- **Output Format:** The processed URLs are saved to an output file, preserving the original URL structure while removing redundant query parameters.

## Usage

### Prerequisites

- Python 3.x installed on your system.

### Running the Script

1. Clone or download the script to your local machine.

2. Open a terminal and navigate to the directory containing the script.

3. Run the script using the following command:

   ```bash
   python paradup.py -i input_file.txt -o output_file.txt
   ```

Replace paradup.py with the actual name of the script file, input_file.txt with the path to your input file containing URLs, and output_file.txt with the desired output file path.

### Command-line Arguments

* **-i** or **--input**: Path to the input file containing a list of URLs.
* **-o** or **--output**: Path to the output file where processed URLs will be saved.

### Example

Suppose you have an input file (input_urls.txt) with the following content:

```
https://example.com/page?param1=value1&param2=value2
https://example.com/page?param1=value3&param4=value4
https://anotherdomain.com/path?param1=value5&param2=value6
```

### Running the script:

python paradup.py -i input_urls.txt -o output_urls.txt

Will generate an output file (output_urls.txt) with the following content:

```
https://example.com/page?param1=value1&param2=value2
https://example.com/page?param4=value4
https://anotherdomain.com/path?param1=value5&param2=value6
```
### License

This script is released under the MIT License, allowing for free and open use, modification, and distribution.

### Acknowledgments

Feel free to contribute, report issues, or suggest improvements!
