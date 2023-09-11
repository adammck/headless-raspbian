# Headless Raspbian

This is a tool to create headless Raspbian images by downloading and patching
the official ones. The only differences are:

* Hostname is set
* Wifi is set up
* SSH is enabled
* SSH pubkeys are configured (via GitHub)
* Password authentication is disabled

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

Once the image is built, one can flash it to a micro SD card using a tool like
[Etcher](https://etcher.balena.io).

## License

MIT.
