Like PHP, except you write your script in the bash shell scripting language instead of PHP.

Example script:
```
#!/usr/bin/shp
<?shp

# Get my hostname
HOSTNAME=`hostname`

# Get current time
TIME=`date`

?>

Welcome to <?shp echo -n $HOSTNAME ?>. The current time is <?shp echo -n $TIME ?>.

<?shp if [ `date +%u` -eq 1 ]; then ?>
Today is Monday, too bad.
<?shp else ?>
Today is not Monday, horray!
<?shp fi ?>
```
Example of running that script:
```
$ ./test.shp

Welcome to linux.example.com. The current time is Wed Nov 2 09:48:11 PDT 2011.

Today is not Monday, horray!

```

Read the [man page](ManPage) for details.
