# File Driver to create a device /dev/one like the /dev/zero

### QuickStart

When installed, running:
```bash
cat /dev/one | hexdump -v 
```

Prints:
```text
0000000 ffff ffff ffff ffff ffff ffff ffff ffff
```


### Install

1. `git clone https://github.com/tinmarino/dev_one DevOne && cd DevOne  # Download`
2. `make build        # Compile`
3. `make key          # Generate key for signing`
4. `sudo make sign    # Sign driver module to permit MOK enforcement (security)`
5. `sudo reboot now   # Reboot and enable Mok`
  1.  
6. `sudo make load    # Load`
7. `sudo make device  # Create /dev/one`
8. `make test         # Test if all is ok`


### Source

*  Device Driver: https://www.apriorit.com/dev-blog/195-simple-driver-for-linux-os
*  Signing driver: https://gist.github.com/Garoe/74a0040f50ae7987885a0bebe5eda1aa
*  Mok: https://ubuntu.com/blog/how-to-sign-things-for-secure-boot


### Util
  sudo mokutil --list-new
  sudo mokutil --reset


### Licence

* Author: Tinmarino
* Date: 2020-10-12
* License: GPL => Open Source
