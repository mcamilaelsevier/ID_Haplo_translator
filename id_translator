import pandas as pd

# Updated ref_to_id function to handle all characters
def ref_to_id(ref):
    if not isinstance(ref, str):
        return None

    untranslated = ""
    for char in ref:
        code = ord(char)
        if char.isdigit():
            untranslated += char
        elif char == 'q':
            untranslated += '0'
        elif char.isalpha() and char != 'u':
            if code == 113:
                untranslated += 'a'
            elif code > 116:
                untranslated += chr(code - 20)
        else:
            untranslated += char

    try:
        id = int(untranslated, 16)
        return id
    except ValueError:
        return None

# Read the input Excel file
df = pd.read_excel("input_ids.xlsx")

# Apply ref_to_id function to each ID and create a new column with the resulting IDs
df['Resulting ID'] = df['ID'].apply(ref_to_id)

# Save the updated DataFrame to the same Excel file
with pd.ExcelWriter("input_ids.xlsx", engine='openpyxl') as writer:
    df.to_excel(writer, index=False)

print("Updated Excel file created successfully with resulting IDs.")