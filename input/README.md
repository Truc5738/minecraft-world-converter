# World input

Upload either one Java world archive named `world.zip`, or split parts named:

- `world.zip.part00`
- `world.zip.part01`
- `world.zip.part02`

When uploading through GitHub's web interface, use split parts smaller than 25 MB each. Upload every part together into this folder and commit them. The workflow joins them back into `world.zip` before conversion.

The reconstructed ZIP must contain `level.dat` at its root, beside the `region/` folder, not inside an extra parent directory.

Do not upload passwords, account tokens, or other secrets.
