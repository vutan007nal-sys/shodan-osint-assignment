# Shodan OSINT Assignment

## 1. Tool Name

**Shodan**

## 2. Description

Shodan is a search engine for Internet-connected devices and services. It collects publicly accessible service information such as banners, ports, software versions, operating systems, and other metadata.

Shodan is useful for security research, network reconnaissance, asset discovery, vulnerability awareness, and cybersecurity education.

## 3. Objective

The objective of this assignment is to understand how Shodan can be used for passive reconnaissance and Internet-facing asset discovery.

## 4. Environment

- Operating System: Kali Linux
- Tool: Shodan CLI
- Activity Type: OSINT / Passive Reconnaissance
- Target: Publicly indexed information
- Purpose: Educational cybersecurity research

## 5. Installation

Install the Shodan CLI:

```bash
python3 -m pip install shodan
```

Verify installation:

```bash
shodan version
```

## 6. API Configuration

Configure the Shodan API key:

```bash
shodan init YOUR_SHODAN_API_KEY
```

Verify configuration:

```bash
shodan info
```

Do not publish your API key on GitHub.

## 7. Basic Searches

Search for publicly indexed nginx services:

```bash
shodan search --limit 10 nginx
```

Search for Apache:

```bash
shodan search --limit 10 apache
```

Search for HTTPS services:

```bash
shodan search --limit 10 "port:443"
```

Search for HTTP services:

```bash
shodan search --limit 10 "port:80"
```

## 8. Saving Results

Save a search result as JSON:

```bash
shodan search --limit 10 --format json nginx > results/shodan-nginx.json
```

Save a text result:

```bash
shodan search --limit 10 nginx > results/shodan-nginx.txt
```

## 9. Information Observed

Depending on the search, Shodan may display information such as:

- IP address
- Port
- Organization
- Hostname
- Operating system
- Service/banner information
- HTTP information
- Location information
- Software information

## 10. Advantages

1. Useful for Internet-wide asset discovery.
2. Helps security professionals identify exposed services.
3. Useful for cybersecurity research.
4. Provides service/banner information.
5. Helps organizations understand their external attack surface.
6. Useful for reconnaissance during authorized security assessments.

## 11. Limitations

1. Shodan data may not always be current.
2. Results depend on Shodan's scanning and indexing.
3. A discovered service does not automatically mean it is vulnerable.
4. Some information may require a paid Shodan account.
5. Results should be verified before making security conclusions.

## 12. Ethical and Legal Considerations

Shodan should be used only for lawful and authorized security research.

This assignment does not involve:

- Exploiting systems
- Bypassing authentication
- Unauthorized access
- Password attacks
- Denial-of-service attacks
- Attempting to compromise discovered devices

The searches performed are intended for educational OSINT research.

## 13. Screenshots

Add screenshots demonstrating:

1. Shodan installation
2. `shodan version`
3. API initialization
4. A sample search
5. Saved result file
6. GitHub repository

Screenshots are stored in:

```text
screenshots/
```

## 14. Conclusion

Shodan is a useful OSINT and cybersecurity reconnaissance tool for discovering publicly indexed Internet-facing services. It can help security professionals understand external exposure and identify potentially interesting assets for authorized investigation.

## 15. References

- Shodan: https://www.shodan.io/
- Shodan CLI documentation: https://cli.shodan.io/
- Shodan Developer Documentation: https://developer.shodan.io/
