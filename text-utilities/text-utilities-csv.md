# CSV

CSV (Comma-Separated Values) is a file format used to represent tabular data. This format is popular because it is easy to read and write, and can be understood by many software applications.

In a CSV file, each line represents a row of data, and each value is separated by a comma (or another delimiter, such as a semicolon). The first line of the file often contains headers that describe the columns of data.

For example, a CSV file representing a simple list of contacts might look like:

```
Name,Email,Phone
John Smith,john@example.com,555-1234
Jane Doe,jane@example.com,555-5678
```

It is important to note that CSV files do not have a standard definition, and different software applications may interpret them slightly differently. Some applications may use different delimiters or allow for additional formatting options.

CSV files are commonly used for data exchange between different software applications or databases. They can be easily exported and imported, and can be opened and edited in software applications such as Microsoft Excel or Google Sheets.

Here is an example of how to read data from a CSV file in Python:

```
import csv

with open('contacts.csv') as csvfile:
    reader = csv.DictReader(csvfile)
    for row in reader:
        print(row['Name'], row['Email'], row['Phone'])
```

This code opens a file called `contacts.csv` and reads the data using the `csv.DictReader` method. It then prints out the values for each row of data.

CSV files can also be written using Python. Here is an example that writes data to a CSV file:

```
import csv

data = [
    ['John Smith', 'john@example.com', '555-1234'],
    ['Jane Doe', 'jane@example.com', '555-5678']
]

with open('contacts.csv', 'w') as csvfile:
    writer = csv.writer(csvfile)
    writer.writerow(['Name', 'Email', 'Phone'])
    writer.writerows(data)
```

This code creates a list of data and writes it to a file called `contacts.csv` using the `csv.writer` method. It first writes the header row, and then writes the data rows using the `writerows` method.

Overall, CSV files are a useful and widely-used format for representing tabular data. They are easy to read and write, and can be understood by many different software applications.
