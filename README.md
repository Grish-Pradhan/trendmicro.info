DNS Records Lookup
This Python script allows users to perform DNS record lookups for a specified domain. It queries various DNS record types, including A, AAAA, MX, NS, and TXT, and returns the results in a readable format.

Features
Supports multiple DNS record types (A, AAAA, MX, NS, TXT).
Uses Google's public DNS servers (8.8.8.8, 8.8.4.4).
Handles DNS queries with a timeout of 2 seconds and a lifetime of 2 seconds to ensure quick responses.
Displays the DNS records in a clear and organized manner.
Handles exceptions and errors gracefully, providing meaningful error messages.
Requirements
Python 3.x
dns.resolver module (usually part of dnspython)
Installation
Clone this repository to your local machine:

bash
Copy
Edit
git clone https://github.com/Grish-Pradhan/DNS_Records_Lookup.git
Navigate to the project directory:

bash
Copy
Edit
cd DNS_Records_Lookup
Install the required Python package (if not already installed):

bash
Copy
Edit
pip install dnspython
Usage
Run the script:

bash
Copy
Edit
python DNS_Records_Lookup.py
Enter the domain name when prompted. For example:

css
Copy
Edit
Enter the domain name to lookup: example.com
The script will output the DNS records for the specified domain, including:

A (IPv4 addresses)
AAAA (IPv6 addresses)
MX (Mail exchange servers)
NS (Name servers)
TXT (Text records)
Example Output
yaml
Copy
Edit
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
Contributing
Fork this repository.
Create a new branch (git checkout -b feature-branch).
Commit your changes (git commit -am 'Add new feature').
Push to the branch (git push origin feature-branch).
Create a new pull request.
License
This project is open-source and available under the MIT License.
