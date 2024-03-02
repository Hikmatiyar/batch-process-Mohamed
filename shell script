#!/bin/bash

# Check if the user provided a directory as an argument
if [ $# -ne 1 ]; then
    echo "Usage: $0 DIRECTORY"
    exit 1
fi

# Navigate to the directory provided by the user
cd "$1" || exit

# Loop through each file in the directory
for file in *; do
    # Check if the current item is a file
    if [ -f "$file" ]; then
        # Print the file name
        echo "File: $file"
        # Print the file size
        echo "Size: $(du -h "$file" | cut -f1)"
        # Print the number of words in the file
        echo "Word Count: $(wc -w < "$file" | cut -d' ' -f1)"
        echo "-------------------"
    fi
done
