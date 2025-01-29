import dns.resolver
import time

def get_dns_records(domain):
    # Create a new resolver
    resolver = dns.resolver.Resolver()
    
    # Configure the resolver
    resolver.timeout = 2
    resolver.lifetime = 2
    
    # Use Google's DNS servers
    resolver.nameservers = ['8.8.8.8', '8.8.4.4']
    
    record_types = ['A', 'AAAA', 'MX', 'NS', 'TXT']
    results = {}
    
    for record_type in record_types:
        print(f"Looking up {record_type} records...")
        try:
            answers = resolver.resolve(domain, record_type)
            results[record_type] = [str(answer) for answer in answers]
        except Exception as e:
            print(f"Error getting {record_type} records: {str(e)}")
            results[record_type] = []
        
        # Add a small delay between queries
        time.sleep(0.1)
    
    return results

def print_results(domain, records):
    print(f"\nDNS Records for {domain}:")
    print("-" * 50)
    
    for record_type, values in records.items():
        if values:
            print(f"\n{record_type} Records:")
            for value in values:
                print(f"  {value}")

if __name__ == "__main__":
    # Ask the user for the domain name
    domain = input("Enter the domain name to lookup: ")
    
    try:
        records = get_dns_records(domain)
        print_results(domain, records)
    except Exception as e:
        print(f"An error occurred: {str(e)}")
