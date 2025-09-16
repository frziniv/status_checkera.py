# status_checkera.py
import requests

def check_website_status(url):
import requests
import sys # Import the sys module to read command-line arguments

def check_website_status(url):
    """Checks if a website is online and prints a simple status message."""
    print(f"Checking status for: {url}")
    try:
        # Send a request to the URL with a 5-second timeout
        response = requests.get(url, timeout=5)
        if response.status_code == 200:
            print(f"✅ Success! The website is online and returned status code 200.")
        else:
            print(f"⚠️ Warning! The website is reachable but returned status code: {response.status_code}")
    except requests.RequestException as e:
        print(f"❌ Error! The website is down or unreachable. Details: {e}")

# --- Main Logic ---
# Check if a URL was provided when running the script
if len(sys.argv) > 1:
    # Use the URL provided by the user
    target_website = sys.argv[1]
    check_website_status(target_website)
else:
    # If no URL is provided, show instructions
    print("Usage: python status_checker.py <website_url>")
    print("Example: python status_checker.py https://www.github.com")    print(f"Checking status for: {url}")
    try:
        # Send a request to the URL with a 5-second timeout
        response = requests.get(url, timeout=5)
        if response.status_code == 200:
            print(f"✅ Success! The website is online and returned status code 200.")
        else:
            print(f"⚠️ Warning! The website is reachable but returned status code: {response.status_code}")
    except requests.RequestException as e:
        print(f"❌ Error! The website is down or unreachable. Details: {e}")

# --- Configuration ---
# The website URL you want to check
target_website = "https://www.google.com"

# --- Run Checker ---
check_website_status(target_website)
