# bash_profile


source ~/.profile
# Use MAMP version of PHP
PHP_VERSION=`ls /Applications/MAMP/bin/php/ | sort -n | tail -1`
export PATH=/Applications/MAMP/bin/php/${PHP_VERSION}/bin:$PATH
# Export MAMP MySQL executables as functions
# Makes them usable from within shell scripts (unlike an alias)
mysql() {
    /Applications/MAMP/Library/bin/mysql "$@"
}
mysqladmin() {
    /Applications/MAMP/Library/bin/mysqladmin "$@"
}
export -f mysql
export -f mysqladmin
