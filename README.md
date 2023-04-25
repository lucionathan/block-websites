# Block Websites Script

This script helps you block or unblock a list of distracting websites, such as social media platforms, by modifying your `/etc/hosts` file. It can be used to increase productivity and avoid distractions.

## Installation

1. Download the script and place it in a directory of your choice.
2. Open a terminal, navigate to the directory where the script is located, and run the following command to give the script execution permission:

```bash
chmod 777 block_websites.sh
```

3. Optionally, you can create a symbolic link to the script to make it globally accessible from anywhere in your terminal. Run the following command, replacing `/path/to/your/script` with the actual path to the script:

```bash
sudo ln -s /path/to/your/script/block_websites.sh /usr/local/bin/block_websites
```

Now you can use the `block_websites` command instead of the script path.

## Usage

### To block distracting websites:

Run the following command:

```bash
sudo ./block_websites on
```
or, if you created a symbolic link:

```bash
sudo block_websites on
```

This command will block all websites listed in the `arr` variable inside the script by modifying the `/etc/hosts` file.

### To unblock distracting websites:

Run the following command:

```bash
sudo ./block_websites off
```

or, if you created a symbolic link:

```bash
sudo block_websites off
```

This command will unblock all websites listed in the `arr` variable by removing their entries from the `/etc/hosts` file.

### To add a new website to the list:

Run the following command, replacing `example.com` with the actual website you want to add:

```bash
sudo ./block_websites add example.com
```

or, if you created a symbolic link:

```bash
sudo block_websites add example.com
```

This command will update the script file, adding the new website to the `arr` variable. To block the newly added website, run the `sudo block_websites on` command again.

### To remove a website from the list:

Run the following command, replacing `example.com` with the actual website you want to remove:

```bash
sudo ./block_websites remove example.com
```

or, if you created a symbolic link:

```bash
sudo block_websites remove example.com
```

This command will update the script file, removing the website from the `arr` variable. To unblock the removed website, run the `sudo block_websites off` command again.
