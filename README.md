# fedora-machine
Minimal Fedora rootfs tarball builds for systemd-nspawn.

## Usage
1. **Download and unzip** the latest artifact.

2. **Import the tarball as a machine:**
   ```
   importctl import-tar -m fedora-rootfs.tar.xz fedora
   ```

3. **[Optional] Enable host networking:**
   - Run:
     ```
     run0 machinectl edit fedora
     ```
   - This opens your `$EDITOR`. Add the following content:
     ```
     [Network]
     VirtualEthernet=no
     ```

4. **Start the machine:**
   ```
   machinectl start fedora
   ```

5. **Enter the machine:**
   ```
   machinectl shell fedora
   ```
