# Apache
**For most usecases we recommend [nginx](#nginx) over Apache**


### .htaccess files

.htaccess files are used to set several options for the same directory or subdirectory

### Useful codeblocks

**Securing a directory**

    php_admin_value     open_basedir /var/www/:/tmp/
    # Note that the : can be used to specify multiple directories as one common rights set. (Scripts can talk to the other directory)