# Kemon
An Open-Source Pre and Post Callback-Based Framework for macOS Kernel Monitoring.

## What is Kemon?
An open-source Pre and Post callback-based framework for macOS kernel monitoring.
With the power of Kemon, we can easily implement LPC communication monitoring, MAC policy filtering, kernel driver firewall, etc. In general, from an attacker's perspective, this framework can help achieve more powerful Rootkit. From the perspective of defense, Kemon can help construct more granular monitoring capabilities. I also implemented a kernel fuzzer [1] through this framework, which helped me find many vulnerabilities, such as: CVE-2017-7155, CVE-2017-7163, CVE-2017-13883 [2] and CVE-2018-4350, CVE-2018-4396, CVE-2018-4418 [3], etc.

## Supported Features
Kemon's features include：
- file operation monitoring
- process creation monitoring
- dynamic library and kernel extension monitoring
- network traffic monitoring
- Mandatory Access Control (MAC) policy monitoring, etc.

In addition, Kemon project can also extend the Pre and Post callback-based monitoring interfaces for any macOS kernel function.

## Getting Started
### How to build the Kemon driver
Please use Xcode project or makefile to build the Kemon kext driver

### How to use the Kemon driver
- Please turn off macOS System Integrity Protection (SIP) check if you don't have a valid kernel certificate
- Use the command "sudo chown -R root:wheel kemon.kext" to change the owner of the Kemon driver
- Use the command "sudo kextload kemon.kext" to install the Kemon driver
- Use the command "sudo kextunload kemon.kext" to uninstall the Kemon driver


## Contributing
Welcome to contribute by creating issues or sending pull requests. See Contributing Guide for guidelines.

## License
Kemon is licensed under the Apache License 2.0. See the LICENSE file.

## References
1. https://www.defcon.org/html/defcon-26/dc-26-speakers.html#Wang
2. https://support.apple.com/en-us/HT208331
3. https://support.apple.com/en-us/HT209193

