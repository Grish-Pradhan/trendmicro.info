# DNS Records Lookup

## Overview

The **DNS Records Lookup** Python script is designed to query multiple DNS record types for a given domain name. The script allows users to retrieve essential DNS records, including `A`, `AAAA`, `MX`, `NS`, and `TXT`, and presents the results in an easy-to-read format.

## Key Features

- **Multi-Record Lookup**: Queries the following DNS records:
  - `A`: IPv4 addresses
  - `AAAA`: IPv6 addresses
  - `MX`: Mail exchange servers
  - `NS`: Name servers
  - `TXT`: Text records
- **Fast DNS Resolution**: Uses Google's DNS servers (`8.8.8.8` and `8.8.4.4`) for fast, reliable lookups.
- **Error Handling**: The script gracefully handles errors during DNS queries and provides clear error messages.
- **Customizable**: You can easily modify resolver settings like timeout and lifetime.

## Installation Guide

1. **Clone the Repository**

   Open a terminal and run the following command to clone the repository:

   ```bash
   git clone https://github.com/Grish-Pradhan/DNS_Records_Lookup.git
   ```

2. **Navigate to the Project Directory**

   Change into the directory of the cloned project:

   ```bash
   cd DNS_Records_Lookup
   ```

3. **Install Required Dependencies**

   You need the `dnspython` library for DNS queries. Install it using pip:

   ```bash
   pip install dnspython
   ```

## Usage Instructions

1. **Run the Python Script**

   To run the script, execute the following command:

   ```bash
   python DNS_Records_Lookup.py
   ```

2. **Enter the Domain Name**

   The script will prompt you to enter the domain name. For example:

   ```
   Enter the domain name to lookup: example.com
   ```

3. **Review the Results**

   The script will output the DNS records for the domain, categorized by record type:

   - `A Records`
   - `AAAA Records`
   - `MX Records`
   - `NS Records`
   - `TXT Records`

### Example Output

```bash
Enter the domain name to lookup: example.com

Looking up A records...
Looking up AAAA records...
Looking up MX records...
Looking up NS records...
Looking up TXT records...

DNS Records for example.com:
--------------------------------------------------

A Records:
  93.184.216.34

AAAA Records:
  2606:2800:220:1:248:1893:25c8:1946

MX Records:
  10 mail.example.com.

NS Records:
  ns1.example.com.
  ns2.example.com.

TXT Records:
  v=spf1 include:_spf.google.com ~all
```

## How It Works

- **DNS Query Types**: The script queries five types of DNS records—`A`, `AAAA`, `MX`, `NS`, and `TXT`.
- **Google DNS**: It uses Google’s public DNS servers (`8.8.8.8`, `8.8.4.4`) for resolving the domain name.
- **Configurable Timeout**: The script has a configurable timeout and lifetime of 2 seconds for each DNS query to ensure efficiency.

## Contributing

We welcome contributions from the community. To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -am 'Add new feature'`).
4. Push your changes to the branch (`git push origin feature-branch`).
5. Open a pull request and describe your changes.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

---

## Contact

For any questions or suggestions, feel free to reach out to me via [GitHub - Grish Pradhan](https://github.com/Grish-Pradhan).

