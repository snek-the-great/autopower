# AutoPower

AutoPower is a bash script designed to automatically manage CPU power modes on a Linux laptop based on the current power source (AC or battery). It allows for configuration, status checks, and management of power modes using a systemd timer.

## Features

- Automatically switches CPU power modes based on AC or battery power.
- Configurable power profiles for both AC and battery.
- Systemd timer for periodic power mode checks.
- Logging and notifications for power mode changes.
- Easy configuration using a built-in editor.
- Supports GNU GPL Warranty and Copyright display.

## Installation

### From GitHub Releases

1. **Download the latest `.deb` package from [GitHub Releases](https://github.com/snek-the-great/autopower/releases):**
   - Navigate to the [Releases page](https://github.com/snek-the-great/autopower/releases).
   - Download the latest version of the `.deb` package.

2. **Install the `.deb` package:**
   ```bash
   sudo dpkg -i autopower_<version>.deb
   ```

   If you encounter any dependency issues, you can resolve them with:
   ```bash
   sudo apt-get install -f
   ```

3. **Run the script:**
   ```bash
   sudo autopower -h
   ```

## Usage

```bash
sudo autopower [options]
```

### Options

- `-c` : Configure settings (e.g., power profiles, timer interval).
- `-s` : Show the current power mode and system status.
- `-h` : Display help message with usage instructions.
- `-p` : Pause automatic power management.
- `-a` : Enable auto start at boot and start the service.
- `-u` : Update power mode immediately based on the current power source.
- `-w` : Show GNU GPL Warranty disclaimer.
- `-c` : Show GNU GPL Copyright notice.

## Configuration

AutoPower uses a configuration file located at `/etc/autopower/autopower.conf`. You can configure the following options:

- `ac_mode` : Power mode to use when on AC power (e.g., `performance`).
- `battery_mode` : Power mode to use when on battery power (e.g., `power-saver`).
- `check_interval` : Interval in seconds for the systemd timer to check the power source.
- `log_file` : Path to the log file for recording power mode changes.

To edit the configuration file, use the `-c` option:

```bash
sudo autopower -c
```

## License

AutoPower is licensed under the GNU General Public License v3.0. See the `LICENSE` file for more details.

## Contributing

Contributions are welcome! Please fork the repository, make your changes, and submit a pull request.

## Author

Created by [SnekTheGreat](https://github.com/snek-the-great).

## Acknowledgments

Special thanks to the open-source community for providing tools and resources to make this project possible.

## Support

If you encounter any issues or have questions, please open an issue on GitHub.