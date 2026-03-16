## Step 1: Create a secondary file for sudoers(leaving the main sudoers file untouched):

``` sudo visudo -f /etc/sudoers.d/rohitkulkarni #username```

## Step 2: Add the rule which will enable passwordless sudo

``` rohitkulkarni ALL(ALL) NOPASSWD: ALL ```

- ALL means this user can run sudo commands from all terminals as all users.
- NOPASSWD as the name suggests no password required for ALL commands.

## Step 3: Save and exit the file, the visudo command checks for syntax errors automatically.

## Step 4: Give permissions for owners and group to read only (strict permissions)

``` sudo chmod 440 /etc/sudoers.d/rohitkulkarni ```

## Step 5: Relogin and run any sudo command to check if command runs without password
