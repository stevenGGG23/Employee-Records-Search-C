# Employee Records Search

A C program that reads employee data from a CSV file into a struct and lets you search through the records by name, zip code, or salary.

## Files

- `lab6Problem1.c` — main source file
- `records.csv` — employee data (first name, last name, zip code, department, salary)

## How It Works

Employee records are loaded from `records.csv` into an array of `Struct_Employee_Info` structs. Three search functions are implemented:

- **searchByName** — finds employees matching a given first and last name
- **searchByZipCode** — finds all employees in a given zip code
- **searchBySalary** — filters employees by salary using a comparison operator (`>`, `<`, `>=`, `<=`, `==`)

If no records match a search, the program prints `No matching records found.`

## Compilation & Usage

```bash
gcc lab6Problem1.c -o lab6Problem1
./lab6Problem1
```

Make sure `records.csv` is in the same directory when you run it.

## Sample Output

```
Search Results by Name: Jack Sparrow
Name: Jack Sparrow       Zip Code: 07801   Department: Movies            Salary: 40000

Search Results by Zip Code: 37128
Name: Pablo Picasso      Zip Code: 37128   Department: Arts              Salary: 65000
Name: Charles Babbage    Zip Code: 37128   Department: Computer Science  Salary: 55000

Search Results by Salary: >= 45000
Name: Pablo Picasso      Zip Code: 37128   Department: Arts              Salary: 65000
Name: Jackie Chan        Zip Code: 12345   Department: Martial Arts      Salary: 50000
Name: Charles Babbage    Zip Code: 37128   Department: Computer Science  Salary: 55000

Search Results by Salary: == 500000
No matching records found.
```

## CSV Format

Records should follow this format with no header row:

```
FirstName,LastName,ZipCode,Department,Salary
```

Example:
```
Pablo,Picasso,37128,Arts,65000
Jack,Sparrow,07801,Movies,40000
```
