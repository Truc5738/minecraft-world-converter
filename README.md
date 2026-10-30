# Minecraft World Converter

This repository converts a Minecraft Java world ZIP into a Bedrock `.mcworld` file using the official [HiveGamesOSS Chunker CLI](https://github.com/HiveGamesOSS/Chunker).

## How to convert

1. Open the `input` folder and upload your Java world as `world.zip`.
2. Make sure `level.dat` is at the ZIP root, beside the `region` folder. Zip the world's contents, not the parent folder.
3. Commit the upload. The **Convert Java World to Bedrock** GitHub Actions workflow starts automatically.
4. Open the **Actions** tab, select the latest run, and wait for it to finish.
5. Under **Artifacts**, download `converted-bedrock-world`. Extract the downloaded artifact ZIP to get `converted-world.mcworld`.
6. Open the `.mcworld` file on Android and choose Minecraft to import it.

You can also start the workflow manually from **Actions → Convert Java World to Bedrock → Run workflow** and choose the Bedrock output format.

## Notes

- The workflow uses the latest official Chunker CLI release and verifies its SHA-256 digest when provided.
- Conversion is not lossless. Chunker documents limitations for some entities and structure data; inspect the converted world in Minecraft.
- GitHub Actions artifacts are temporary downloads and are retained for 14 days.
