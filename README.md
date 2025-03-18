# week-4-python
def modify_file():
    try:
        # Ask the user for a filename
        filename = input("Enter the filename to read: ")

        # Open the file for reading
        with open(filename, "r") as file:
            content = file.read()

        # Modify the content (convert to uppercase)
        modified_content = content.upper()

        # Write the modified content to a new file
        new_filename = "modified_" + filename
        with open(new_filename, "w") as new_file:
            new_file.write(modified_content)

        print(f"Modified content has been saved to {new_filename}")

    except FileNotFoundError:
        print("Error: The file does not exist. Please check the filename and try again.")
    except IOError:
        print("Error: Unable to read the file. Please check file permissions.")

# Run the function
modify_file()
