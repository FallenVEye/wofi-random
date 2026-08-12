Disclaimer: AI was involed in creation of this script

# A hotkey random generator

## Description
Wofi used as an input to determine which character types to include and the length of the random string to generate. The generated password is automatically typed into the active window using `ydotool`.

## Input Format
The input consists of two parts separated by a space:

**Character Type Flags** (first part):
- Use any combination of these characters to specify which types to include:
  - `1` or any digit (0-9) → include digits
  - `a-z` or any lowercase letter → include lowercase letters
  - `A-Z` or any uppercase letter → include uppercase letters
- The script only checks for the *presence* of these character types; the actual characters/digits you use don't matter
  - `1gN`, `f3H`, `13g2CnG`, `8Vd4`, `69Nice` all generate strings with digits, lowercase, and uppercase letters
  - Only the *types* present matter, not their count or order

**Length** (second part):
- An integer specifying how many characters the generated string should be

## Usage Examples

Generate random **digits only**, length 4:
- Input: `1 4` → Output: `1165`

Generate random **digits and lowercase letters**, length 8:
- Input: `1h 8` → Output: `80sn9j9y`

Generate random **digits and [lower/upper]case letters**, length 16:
- Input: `1fG 16` → Output: `7481SU05pHWlnbl`
