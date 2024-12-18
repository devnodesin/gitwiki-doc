## Create User

To create a new user: `wiki:useradd`

There are two roles for a user: `admin` and `reader`.

1. **admin** user can create and delete other users from UI
2. **reader** user can only that are private pages

Here is the example of creating a new admin user

{.code .rounded}
```bash
$ php artisan wiki:useradd

Enter name:
> Mohamed Thalib
Enter email:
> mohamed@example.com.com

Enter password:
>

Select role [admin]:
 [0] admin
 [1] reader
> 0

User created successfully.
```

Here is the example of creating a new reader user

{.code .rounded}
```bash
$ php artisan wiki:useradd

Enter name:
> Tawfiq
Enter email:
> tawfiq@example.com.com

Enter password:

Select role [admin]:
 [1] reader
> 1

User created successfully.
```

## Delete User

To delete an existing user, use the `wiki:userdel` command followed by the user's email address:

The command will:
1. Ask for confirmation before deleting the user
2. Show an error if the user is not found
3. Display a success message after deletion

Here's an example of deleting a user:

{.code .rounded}
```bash
$ php artisan wiki:userdel tawfiq@example.com.com
Are you sure you want to delete user: tawfiq@example.com.com? (yes/no) [no]:
> yes

User deleted successfully.
```

If the user is not found, you'll see an error message:

{.code .rounded}
```bash
$ php artisan wiki:userdel nonexistent@example.com
User not found.
```

### Code Formatting

When formatting code, use triple backticks **`**


## Directory and File Filtering

The WikiFileService now includes enhanced filtering logic for directories and files:

### Directory Filtering

- Directories are excluded if they match any of the following:
  - `.git`
  - `node_modules`
  - `vendor`
- Additionally, directories must only contain lowercase alphabetic characters, numbers, and hyphens. Any directory name not matching this pattern will be skipped.

### File Filtering

- Files are excluded if they end with the `.ignore` extension.
- Valid filenames must consist of lowercase alphabetic characters, numbers, hyphens, and periods.
- Only files with the extensions `.md` or `.markdown` are considered valid for processing.