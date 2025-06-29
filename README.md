## English Description 

A Perl project that generates Markdown coverage reports from Devel::Cover data. Converts code coverage statistics into readable tables showing statement, branch, condition coverage percentages for better code quality analysis.

## Russian Description 

Perl проект для генерации Markdown отчетов покрытия кода из данных Devel::Cover. Преобразует статистику покрытия в читаемые таблицы с процентами операторов, ветвлений, условий для анализа качества кода.

# Perl Coverage to Markdown

A Perl project that converts Devel::Cover code coverage data into readable Markdown reports. This tool helps developers analyze code coverage statistics by generating formatted tables showing statement, branch, condition, and subroutine coverage percentages.

## Features

- 🔍 **Coverage Analysis** - Analyzes Perl code coverage data from Devel::Cover
- 📊 **Markdown Reports** - Generates clean, readable Markdown tables
- 🎯 **Multiple Metrics** - Shows statement, branch, condition, subroutine, and time coverage
- 🚀 **Easy to Use** - Simple command-line interface
- 📈 **Quality Insights** - Helps identify untested code areas

## Project Structure

```
my_perl_project/
├── coverage_to_markdown.pl    # Main coverage conversion script
├── simple_coverage_script.pl  # Simplified version for basic reports
├── lib/
│   └── MyModule.pm            # Sample Perl module
├── t/
│   └── basic.t                # Test files
├── cover_db/                  # Devel::Cover database (auto-generated)
├── coverage.md                # Generated Markdown report
└── README.md                  # This file
```

## Prerequisites

- Perl 5.x
- Devel::Cover module
- File::Find (usually included with Perl)
- Data::Dumper (usually included with Perl)
- Storable (usually included with Perl)

## Installation

1. **Install Devel::Cover** (if not already installed):
   ```bash
   # Using CPAN
   cpan Devel::Cover
   
   # Or using system package manager (Ubuntu/Debian)
   sudo apt-get install libdevel-cover-perl
   ```

2. **Clone or download this project**:
   ```bash
   git clone <your-repository-url>
   cd my_perl_project
   ```

## Usage

### Step 1: Generate Coverage Data

Run your Perl scripts with coverage analysis:

```bash
# For a single script
perl -MDevel::Cover your_script.pl

# For running tests with coverage
perl -MDevel::Cover t/basic.t

# Or use cover command (if available)
cover -test
```

### Step 2: Generate Markdown Report

Run the coverage conversion script:

```bash
# Main script (diagnostic version)
perl coverage_to_markdown.pl

# Or simple version
perl simple_coverage_script.pl
```

### Step 3: View Results

Open the generated `coverage.md` file to see your coverage report.

## Commands Reference

| Command | Description |
|---------|-------------|
| `perl -MDevel::Cover script.pl` | Run script with coverage analysis |
| `perl coverage_to_markdown.pl` | Generate diagnostic coverage report |
| `perl simple_coverage_script.pl` | Generate basic coverage report |
| `cover -delete` | Delete existing coverage database |
| `ls -la cover_db/` | View coverage database contents |

## Understanding Coverage Metrics

- **Statements**: Percentage of code lines executed
- **Branches**: Percentage of conditional branches taken
- **Conditions**: Percentage of boolean expressions evaluated
- **Subroutines**: Percentage of functions/methods called
- **Time**: Time distribution across code sections
- **Total**: Overall coverage percentage

## Example Output

```markdown
# Покрытие кода

| Файл | Операторы | Ветвления | Условия | Подпрограммы | Время | Общее |
|------|-----------|-----------|---------|--------------|-------|-------|
| MyModule.pm | 85.7% | 75.0% | 66.7% | 100.0% | 45.2% | 82.1% |
| script.pl | 92.3% | 83.3% | 87.5% | n/a | 54.8% | 89.7% |
```

## Troubleshooting

### Common Issues

1. **"Can't locate Devel::Cover"**
   ```bash
   cpan Devel::Cover
   ```

2. **"Coverage database not found"**
   ```bash
   # Generate coverage data first
   perl -MDevel::Cover your_script.pl
   ```

3. **"cover command not found"**
   ```bash
   # Use perl -MDevel::Cover instead
   perl -MDevel::Cover -e "your code here"
   ```

4. **Empty coverage report**
   - Ensure your code actually runs
   - Check that no early exits or errors occur
   - Verify coverage database was created

### Debug Commands

```bash
# Check coverage database contents
ls -la cover_db/

# View coverage files
find cover_db -name "*.html" -exec echo {} \;

# Check if Devel::Cover is properly installed
perl -MDevel::Cover -e "print 'OK'"
```

## Development

### Adding New Features

1. Fork the repository
2. Create a feature branch
3. Add your improvements to the conversion scripts
4. Test with various Perl projects
5. Submit a pull request

### Testing

```bash
# Run basic test
perl t/basic.t

# Run with coverage
perl -MDevel::Cover t/basic.t

# Generate report
perl coverage_to_markdown.pl
```

## Contributing

Contributions are welcome! Please:

1. Follow Perl best practices
2. Add comments in both English and Russian
3. Test your changes with different coverage scenarios
4. Update documentation as needed


## Author

Created for better Perl code coverage analysis and reporting.

---

**Русская версия**

# Perl Coverage to Markdown

Проект для преобразования данных покрытия кода Devel::Cover в читаемые Markdown отчеты. Инструмент помогает разработчикам анализировать статистику покрытия кода, генерируя форматированные таблицы с процентами покрытия операторов, ветвлений, условий и подпрограмм.

## Использование

# Создание Markdown отчета
perl coverage_to_markdown.pl

# Просмотр результатов
cat coverage.md
```
