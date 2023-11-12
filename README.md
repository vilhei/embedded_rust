# embedded_rust
Collected guides and information etc. about embedded rust for personal storage

## Rust and cargo

Install rust and nightly toolchain.

### Probe-rs
https://probe.rs/docs/getting-started/installation/

### Serial port udev rules
```
echo -e "SUBSYSTEMS==\"usb\", ATTRS{idVendor}==\"303a\", ATTRS{idProduct}==\"1001\", MODE=\"0660\", GROUP=\"plugdev\"" | sudo tee /etc/udev/rules.d/99-esp-rust-board.rules > /dev/null
```
Reload udev rules
```
sudo udevadm control --reload-rules && sudo udevadm trigger
```
