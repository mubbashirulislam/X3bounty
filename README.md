# X3bounty

X3bounty is a Bash script designed to automate the process of discovering subdomains and performing WHOIS lookups for a given target domain. It leverages various tools and APIs to gather and validate subdomain information, providing users with a comprehensive view of potential subdomains associated with their target.

## Features

- **Subdomain Discovery**: Collects subdomains from multiple sources including crt.sh and SecurityTrails.
- **WHOIS Lookup**: Retrieves WHOIS information for the target domain.
- **Subdomain Validation**: Validates discovered subdomains by checking DNS resolution and HTTP connectivity.
- **Progress Bar**: Displays a progress bar with animation during subdomain validation.
- **Workspace Management**: Organizes results in a dedicated workspace for each scan.
- **Interactive Menu**: Provides an interactive menu for ease of use.
- **Previous Results Viewing**: Allows users to view results from previous scans.

## Installation

To use X3bounty, ensure you have the following tools installed on your system:

- `dig`
- `host`
- `curl`
- `jq`
- `nmap`
- `whois`

You can install these tools using the following command:

```bash
sudo apt install dnsutils curl jq nmap whois
```

## Usage

Clone the repository and navigate to the script directory:

```bash
git clone https://github.com/mubbashirulislam/X3bounty.git
cd X3bounty
```

Make the script executable:

```bash
chmod +x x3bounty.sh
```

Run the script with the desired options:

```bash
./x3bounty.sh [options]
```

### Options

- `-h, --help`: Show the help message.
- `-t, --target`: Specify the target domain for scanning.
- `-v, --version`: Display the version information.
- `-l, --list`: List previous scan results.

### Examples

Start a new scan for a domain:

```bash
./x3bounty.sh -t example.com
```

List previous scan results:

```bash
./x3bounty.sh --list
```

## Script Details

### Functions

- **show_banner**: Displays the tool's banner with metadata.
- **progress_bar**: Shows a progress bar with animation during operations.
- **check_requirements**: Checks for the presence of required tools.
- **whois_lookup**: Performs a WHOIS lookup for the target domain.
- **validate_subdomain**: Validates subdomains by checking DNS and HTTP connectivity.
- **normalize_subdomain**: Normalizes subdomain names for consistency.
- **find_active_subdomains**: Finds and validates active subdomains.
- **setup_workspace**: Sets up a workspace for storing scan results.
- **start_scan**: Initiates the scanning process for a specified target.
- **view_previous_results**: Displays results from previous scans.
- **cleanup**: Cleans up temporary files and handles script exit.
- **show_help**: Displays usage instructions and options.
- **show_menu**: Provides an interactive menu for user interaction.

### Execution Flow

1. **Initialization**: The script checks for required tools and displays the banner.
2. **Argument Parsing**: Command-line arguments are parsed to determine the operation mode.
3. **Scan Execution**: If a target is specified, a scan is initiated; otherwise, the interactive menu is displayed.
4. **Result Management**: Results are saved in a structured workspace, and previous results can be viewed.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions or support, please contact the developer at [GitHub](https://github.com/mubbashirulislam).

  
