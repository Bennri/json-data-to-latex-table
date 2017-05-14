# Parse JSON data to LaTeX table

Extract data from JSON files and create a table containing those values. The created table is a simple one without coloring or other styling. It is useful if you store result of a series of tests in a separate JSON file. The class is able to create a table like following one:

| Header One     | Header Two     | Header Three     | Header Four     |
| :------------- | :------------- | :------------- | :------------- |
| Value1 of JSON 1 | Value2 of JSON 1| Value3 of JSON 1 |Value4 of JSON 1|
| Value1 of JSON 2 | Value2 of JSON 2| Value3 of JSON 2 |Value4 of JSON 2|
| Value1 of JSON 3 | Value2 of JSON 3| Value3 of JSON 3 |Value4 of JSON 3|
| Value1 of JSON 3 | Value2 of JSON 3| Value3 of JSON 3 |Value4 of JSON 3|
...

## Usage

Create an object of the class:
```python
path = "/some/path/to/json/files/*/*.json"
output_file = "test_output.tex"
parser = JSONtoLaTeXtableParser(path, output_file)
parser.parse_first_level_to_latex_tab("key1", "key2", "key3", "key4")
parser.create_latex_table()
parser.write_table_to_file()
```

The table is then written to the file specified in `output_file`.
