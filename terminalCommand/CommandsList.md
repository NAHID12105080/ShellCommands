# Change File Extensions from .nix to .mp4 in Ubuntu Terminal

To rename multiple files with a `.nix` extension to a `.mp4` extension in the terminal on Ubuntu, you can use the following command:

```bash
for file in *.nix; do mv -- "$file" "${file%.nix}.mp4"; done
