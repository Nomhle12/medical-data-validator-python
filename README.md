Medical Records Validator
Overview
This project implements a Python-based medical record validation system.
The validator ensures that patient records follow the expected data structure, required keys, and value constraints. It is designed to detect formatting errors and invalid field values within a dataset of medical records.

Features
The validator performs the following checks:
- Ensures the input data is a list or tuple
- Verifies each item is a dictionary
- Checks that all required keys are present
- Validates field values using type checks and pattern matching
- Returns detailed error messages for invalid records

Validation Rules
Each medical record must contain the following fields:
- 'patient_id' → string matching pattern 'P####'
- 'age' → integer (18 or older)
- 'gender' → "male" or "female" (case-insensitive)
- 'diagnosis' → string or None
- 'medications' → list of strings
- 'last_visit_id' → string matching pattern 'V####'

Regular expressions are used to validate ID formats.

If invalid data is found, the program prints descriptive validation messages indicating:
- The position of the record
- The invalid field
- The incorrect value

If all records pass validation, the program prints:
Valid format.
