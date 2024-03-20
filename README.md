# Paste.sh

Paste.sh is a simple command-line tool that allows you to easily paste files and generate shareable URLs. It provides a convenient way to share files with others by creating a temporary web server and hosting the pasted files.

## Features

- Paste files from the command line
- Generate unique URLs for each pasted file
- Automatically create HTML pages for easy viewing of pasted files
- Start a simple web server to serve the pasted files
- Display the public IP address and local IP address for accessing the pasted files

## Prerequisites

- Bash shell
- `curl` command-line tool
- `nc` (netcat) command-line tool

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/inabakumori/paste.sh.git
   ```

2. Navigate to the project directory:

   ```bash
   cd paste.sh
   ```

3. Make the script executable:

   ```bash
   chmod +x paste.sh
   ```

## Usage

To paste a file and generate a shareable URL, follow these steps:

1. Run the script with the path to the file you want to paste:

   ```bash
   ./paste.sh /path/to/your/file
   ```

2. The script will generate a unique URL for the pasted file and display it in the console.

3. Access the pasted file using the provided URL in a web browser.

   - If you are running the script on the same machine, you can use the `localhost` URL (e.g., `http://localhost:55554/filename.html`).
   - If you want to access the pasted file from another device on the same network, use the local IP address URL (e.g., `http://192.168.0.10:55554/filename.html`).
   - If you want to access the pasted file from a different network or the internet, use the public IP address URL (e.g., `http://203.0.113.10:55554/filename.html`). However, note that you might be behind a NAT (Network Address Translation), and the public IP address may not be directly accessible. In such cases, you may need to configure port forwarding on your router to allow incoming connections to the specified port (55554).

4. The script will start a simple web server using `nc` (netcat) and serve the pasted files. It will continue running until you stop it manually by pressing `Ctrl+C`.

**Note:** This script has been successfully tested on macOS and Linux.

## License

This project is licensed under the GNU General Public License v3.0. See the [LICENSE](LICENSE) file for more information.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

## Acknowledgements

- The script uses the `curl` command-line tool to retrieve the public IP address from `http://ifconfig.me`.
- The script uses the `nc` (netcat) command-line tool to start a simple web server.

## Disclaimer

This script is provided as-is and comes with no warranty or guarantee. Use it at your own risk. The author is not responsible for any misuse or damage caused by this script.

---
