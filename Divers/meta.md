# Add Meta as open menu shortcut

NOTE: This feature is supported by default in Plasma 5.8 and above.

## Installation

1. Install dependencies. On Ubuntu:

    sudo apt-get install git gcc make libx11-dev libxtst-dev pkg-config

On some systems you also need to install the build-essential package.

2. Clone project and compile:

    cd /usr/local/bin
    git clone https://github.com/hanschen/ksuperkey.git
    cd ksuperkey
    make
    mv ksuperkey ../ksuperkey2
    cd ..
    rm -rf ksuperkey
    mv ksuperkey2 ksuperkey

Launch ksuperkey. Make sure that the shortcut for the application launcher is set to Alt+F1.

## Startup

Set ksuperkey to be auto-started.

# Sources

https://github.com/hanschen/ksuperkey
