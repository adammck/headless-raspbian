# Headless Raspbian

This is a tool to create headless Raspbian images by downloading and patching
the official ones. The only differences are:

* SSH is enabled
* Password authentication is disabled
* SSH pubkeys are configured (via GitHub)
* Wifi SSID and password is set
* Hostname is set

This is just enough to get the thing booted up and ready to provision over SSH
with Ansible or whatever. I know that I should be building proper images with
pi-gen, but this seems simpler to keep up to date.

This is only tested on my Mac, but it might work wherever Vagrant does.

## Usage

    git clone https://github.com/adammck/headless-raspbian.git
    cd headless-raspbian
    cp vars.sh.example vars.sh
    vi vars.sh
    bin/run

## License

MIT.
