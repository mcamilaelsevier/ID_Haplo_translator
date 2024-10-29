

# ID Converter

This Python script is designed to convert references to IDs in an Excel file. The script reads an input Excel file containing IDs, applies the `ref_to_id` function to each ID, and creates a new column with the resulting IDs. The updated DataFrame is then saved back to the same Excel file.

## Prerequisites
- Python 3.x
- pandas library

## Installation
1. Clone this repository to your local machine.
```bash
git clone https://github.com/your_repository.git
```

2. Install the required dependencies using pip.
```bash
pip install pandas
```

## Usage
1. Place the script (`script_name.py`) and the input Excel file (`input_ids.xlsx`) in the same directory.
2. Run the script to convert the IDs using the `ref_to_id` function.
```bash
python script_name.py
```

## Functionality
The `ref_to_id` function in the script converts references to IDs based on specific rules for different characters. It handles alphanumeric characters, digits, and special cases to generate the resulting IDs.

## File Structure
- `script_name.py`: Python script for ID conversion.
- `input_ids.xlsx`: Input Excel file containing IDs.

## Output
Upon successful execution, the script will create an updated Excel file (`input_ids.xlsx`) with a new column of resulting IDs.
