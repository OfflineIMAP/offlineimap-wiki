You might want to copy/paste the following content to your bug report.
Remove unused options. ,-)

***

	### Issue

	Python exception traces, warnings, comments, etc...

	### Used configuration options

	* maxsyncaccounts = 1
	* ui = basic
	* ignore-readonly = no
	* pythonfile = 
	* socktimeout = 60

	* [mbnames] (details)

	* account name: 
	* localrepository = 
	* remoterepository = 

	* status_backend = plain
	* maildir-windows-compatible = no

	* synclabels = no

	* labelsheader = X-Keywords
	* ignorelabels = \Inbox, \Starred, \Sent, \Draft, \Spam, \Trash, \Important
	* filterheaders = X-Some-Weird-Header

	### Local Repository options

	* type = Maildir
	* localfolders = ~/Test
	* sep = .

	### Remote Repository options

	* ssl = yes
	* sslclientcert = /path/to/file.crt
	* sslclientkey = /path/to/file.key
	* sslcacertfile = /path/to/cacertfile.crt

	* preauthtunnel = ssh -q imaphost '/usr/bin/imapd ./Maildir'
	* transporttunnel = openssl s_client -host myimap -port 993 -quiet

	* reference = Mail

	* maxconnections = 2

	* idlefolders = ['INBOX', 'INBOX.Alerts']
	* nametrans = lambda foldername: re.sub('^INBOX\.*', '.', foldername)
	* dynamic_folderfilter = False
	* folderfilter = lambda foldername: foldername in ['INBOX', 'Sent']
	* folderincludes = ['debian.user', 'debian.personal']
	* createfolders = True
