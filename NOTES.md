- Using ShadowDrive

```bash
$ solana address --keypair ~/keys/thugbirdz/thugbirdz.json
BVKUniNc55ZWrm9SVko6af6rr3NRpQovjjH5iMrFb2cB

$ solana balance -um --keypair ~/keys/thugbirdz/thugbirdz.json
0.01 SOL

$ spl-token accounts -um --owner ~/keys/thugbirdz/thugbirdz.json
Token                                         Balance
---------------------------------------------------------------
SHDWyBxihqiCj6YekG2GUr7wqKLeLAMK1gHZck9pL6y   1

$ shdw-drive create-storage-account --keypair ~/keys/thugbirdz/thugbirdz.json --name "thugbirdz reloaded" --size 5MB
This is beta software running on Solana's Mainnet. Use at your own discretion.
✔ By creating your first storage account on Shadow Drive, you agree to the Terms of Service as outlined here: https://shadowdrive.org. Confirm? … yes
✔ This storage account will require an estimated 0.001220703 SHDW to setup. Would you like to continue? … yes
✔ Successfully created your new storage account of 5MB located at the following address on Solana: 3FEuxTiG1J6VSc54pUGxGcZsqk4BMZ6h52FyX9V2jhCm

$ solana balance -um --keypair ~/keys/thugbirdz/thugbirdz.json
0.00530592 SOL

$ spl-token accounts -um --owner ~/keys/thugbirdz/thugbirdz.json
Token                                         Balance
---------------------------------------------------------------
SHDWyBxihqiCj6YekG2GUr7wqKLeLAMK1gHZck9pL6y   0.998779297
```
