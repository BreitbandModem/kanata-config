Setup:

- Install kanata
  - `brew install kanata`
  - the current release is  not compatible with the latest version of karabiner-elements, so you will need to build from source
    - `git clone https://github.com/jtroo/kanata`
    - `cd kanata`
    - `cargo build`
    - `cp target/debug/kanata ~/.local/bin/`
- Install karabiner-elements
  - `brew install --cask karabiner-elements`
- Link the kanata.kbd file to the karabiner-elements config directory
  - `ln -s /Users/<user>/git/kanata-config/kanata.kbd /Users/<user>/Library/Application\ Support/kanata/`
- Set no pwd for sudo
  - `sudo visudo -f /private/etc/sudoers.d/kanata`
  - `<user> ALL=(root) NOPASSWD: /Users/<user>/.local/bin/kanata`
  - `<user> ALL=(root) NOPASSWD: /Library/Application\ Support/org.pqrs/Karabiner-DriverKit-VirtualHIDDevice/Applications/Karabiner-VirtualHIDDevice-Daemon.app/Contents/MacOS/Karabiner-VirtualHIDDevice-Daemon`
- Start karabiner in one terminal tab, and kanata in another
  - `sudo '/Library/Application Support/org.pqrs/Karabiner-DriverKit-VirtualHIDDevice/Applications/Karabiner-VirtualHIDDevice-Daemon.app/Contents/MacOS/Karabiner-VirtualHIDDevice-Daemon'`
  - `sudo kanata`
