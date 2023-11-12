# embedded_rust
Collected guides and information etc. about embedded rust for personal storage

## Rust and cargo

Install rust and nightly toolchain.
### Target
Maybe need to add target via rustup e.g.
```bash
rustup target add riscv32imc-unknown-none-elf
```

### Probe-rs
https://probe.rs/docs/getting-started/installation/

### Serial port udev rules
```bash
echo -e "SUBSYSTEMS==\"usb\", ATTRS{idVendor}==\"303a\", ATTRS{idProduct}==\"1001\", MODE=\"0660\", GROUP=\"plugdev\"" | sudo tee /etc/udev/rules.d/99-esp-rust-board.rules > /dev/null
```
Reload udev rules
```bash
sudo udevadm control --reload-rules && sudo udevadm trigger
```


