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

$ shdw-drive upload-multiple-files --keypair ~/keys/thugbirdz/thugbirdz.json --directory data/new-metadata-files
This is beta software running on Solana's Mainnet. Use at your own discretion.
Writing upload logs to /Users/nunya/solanasanctuary/thugbirdz-utils/shdw-drive-upload-16576584172.json.
✔ Collecting all files
✔ Which storage account do you want to use? › thugbirdz reloaded - 3FEuxTiG1J6VSc54pUGxGcZsqk4BMZ6h52FyX9V2jhCm - 5.00 MB available - V2
Starting upload of 3311 files to 3FEuxTiG1J6VSc54pUGxGcZsqk4BMZ6h52FyX9V2jhCm with concurrency 3
Upload Progress | █████████████████░░░░░░░░░░░░░░░░░░░░░░░ | 42% || 1395/3311 Files
/Users/nunya/.nvm/versions/node/v16.13.0/lib/node_modules/@shadow-drive/cli/node_modules/rxjs/dist/cjs/internal/util/reportUnhandledError.js:13
            throw err;
            ^
FetchError: invalid json response body at https://shadow-storage.genesysgo.net/upload reason: Unexpected token B in JSON at position 0
    at /Users/nunya/.nvm/versions/node/v16.13.0/lib/node_modules/@shadow-drive/cli/node_modules/node-fetch/lib/index.js:273:32
    at runMicrotasks (<anonymous>)
    at processTicksAndRejections (node:internal/process/task_queues:96:5)
    at async /Users/nunya/.nvm/versions/node/v16.13.0/lib/node_modules/@shadow-drive/cli/dist/shdw-drive.js:576:28 {
  type: 'invalid-json'
}

$ shdw-drive upload-multiple-files --keypair ~/keys/thugbirdz/thugbirdz.json --directory data/new-metadata-files
This is beta software running on Solana's Mainnet. Use at your own discretion.
Writing upload logs to /Users/nunya/solanasanctuary/thugbirdz-utils/shdw-drive-upload-16576592495.json.
✔ Collecting all files
✔ Which storage account do you want to use? › thugbirdz reloaded - 3FEuxTiG1J6VSc54pUGxGcZsqk4BMZ6h52FyX9V2jhCm - 3.29 MB available - V2
Starting upload of 1911 files to 3FEuxTiG1J6VSc54pUGxGcZsqk4BMZ6h52FyX9V2jhCm with concurrency 3
Upload Progress | ████████████████████████████████████████ | 100% || 1911/1911 Files
1911 files uploaded.
```
