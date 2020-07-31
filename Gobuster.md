![](https://redteamtutorials.com/wp-content/uploads/2018/11/gobuster-1.png)

# GoBuster Courses : 

Gobuster is a tool for brute forcing URIs (Files and Directories) and DNS subdomains.
The help section can provide options for Gobuster.

`gobuster -h`

![](https://redteamtutorials.com/wp-content/uploads/2018/11/help.png)

### Common Command line options :

- -fw – force processing of a domain with wildcard results.
- -np – hide the progress output.
- -m  – which mode to use, either dir or dns (default: dir).
- -q – disables banner/underline output.
- -t
-  – number of threads to run (default: 10).
- -u  – full URL (including scheme), or base domain name.
- -v – verbose output (show all results).
- -w  – path to the wordlist used for brute forcing (use – for stdin).

#### Command line options for dns mode :

- -cn – show CNAME records (cannot be used with ‘-i’ option).
- -i – show all IP addresses for the result.

#### Command line options for dir mode :

- -a <user agent string> – specify a user agent string to send in the request header.
- -c <http cookies> – use this to specify any cookies that you might need (simulating auth).
- -e – specify extended mode that renders the full URL.
- -f – append / for directory brute forces.
- -k – Skip verification of SSL certificates.
- -l – show the length of the response.
- -n – “no status” mode, disables the output of the result’s status code.
- -o <file> – specify a file name to write the output to.
- -p <proxy url> – specify a proxy to use for all requests (scheme much match the URL scheme).
- -r – follow redirects.
- -s <status codes> – comma-separated set of the list of status codes to be deemed a “positive” (default: 200,204,301,302,307).
- -x <extensions> – list of extensions to check for, if any.
- -P <password> – HTTP Authorization password (Basic Auth only, prompted if missing).
- -U <username> – HTTP Authorization username (Basic Auth only).
- -to <timeout> – HTTP timeout. Examples: 10s, 100ms, 1m (default: 10s).

### Wordlist Usage :

`gobuster -w <wordlist.txt>`

![](https://redteamtutorials.com/wp-content/uploads/2018/11/gobusterexample-wordlist-1024x499.png)

The wordlist switch specifies a wordlist that can be used for brute forcing directories.

### URL Usage

`gobuster -u <url>`

![](https://redteamtutorials.com/wp-content/uploads/2018/11/gobusterexample-url-1024x499.png)

The URL switch specifies the website name that will be scanned.

### Thread Usage

`gobuster -t <Num>`

![](https://redteamtutorials.com/wp-content/uploads/2018/11/gobusterexample-threads-1024x499.png)

The thread switch specifies the number of concurrent threads that will run at the same time.

### Extension Usage

`gobuster -x <ext>`

![](https://redteamtutorials.com/wp-content/uploads/2018/11/gobusterexample-ext-1024x499.png)

The extension switch specifies the file extensions. Multiple extensions may be listed separated by commas.

### String Usage

`gobuster -s “<string>”`

![](https://redteamtutorials.com/wp-content/uploads/2018/11/gobusterexample-string-edit-1024x304.png)

The string switch species the results that are being displayed.

### Expanded Mode Usage

`gobuster -e`

![](https://redteamtutorials.com/wp-content/uploads/2018/11/gobusterexample-expanded-edit-1024x293.png)

### No Status Usage

`gobuster -n

![](https://redteamtutorials.com/wp-content/uploads/2018/11/gobusterexample-nostatus-1024x305.png)

The no status mode will exclude the status codes in the results.

### Verbose Mode

`gobuster -v`

![](https://redteamtutorials.com/wp-content/uploads/2018/11/gobusterexample-verbose.png)

The verbose mode will increase the logging level of the search results.

### User Agent

`gobuster -a <useragent>`

![](https://redteamtutorials.com/wp-content/uploads/2018/11/gobusterexample-useragent.png)

### Export Option

`gobuster -o <filename>`

![](https://redteamtutorials.com/wp-content/uploads/2018/11/gobusterexample-output.png)

The output option saves the results to file in text format.

