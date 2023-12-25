Url Endpoint Sorter
===================

This Python script is designed to sort and extract unique URL prefixes from a given input file. It can be particularly useful for analyzing and organizing a list of URLs based on their common prefixes.

Usage
-----

### Prerequisites

*   Python 3.x

### Installing the Tool

To use the tool, Install via pip:

    pip install endpointsorter

### Running the Script

To use the script, follow these steps:

    endpointsorter -i input_file.txt -o output_file.txt

Replace `script_name.py` with the actual name of the script, `input_file.txt` with the path to your input file containing URLs, and `output_file.txt` with the desired output file path.

### Command-Line Options

*   `-i, --input`: Specify the input file containing URLs. This option is **required**.
*   `-o, --output`: Specify the output file where sorted URL prefixes will be saved. This option is **required**.

Example
-------

    endpointsorter -i input.txt -o output.txt

Description
-----------

The script utilizes regular expressions to extract URLs from the input file and then sorts and extracts unique prefixes. The sorted prefixes are saved to the specified output file. This can be helpful for understanding the structure and organization of URLs in a given dataset.

Error Handling
--------------

The script includes basic error handling to manage interruptions and unexpected errors during execution. If an error occurs, an error message is displayed, and the script exits with an error code.

Author
------

Praveen

Feel free to modify and enhance this script according to your specific requirements. If you encounter any issues or have suggestions for improvements, please open an issue or submit a pull request.