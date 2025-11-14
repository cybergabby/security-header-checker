import requests

def check_security_headers(url):
    try:
        response = requests.get(url, timeout=5)
        headers = response.headers

        security_headers = [
            "Content-Security-Policy",
            "Strict-Transport-Security",
            "X-Content-Type-Options",
            "X-Frame-Options",
            "Referrer-Policy",
            "Permissions-Policy"
        ]

        print(f"\n[*] Scanning: {url}\n")
        for header in security_headers:
            if header in headers:
                print(f"[+] {header}: PRESENT")
            else:
                print(f"[-] {header}: MISSING")

    except Exception as e:
        print(f"Error: {e}")


if __name__ == "__main__":
    target = input("Enter target URL (e.g., https://example.com): ")
    check_security_headers(target)
