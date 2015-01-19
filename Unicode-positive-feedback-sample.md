You might want to copy/paste the following content to your bug report.
Remove unused options. ,-)

Create a new issue for each positive feedback. Notice that the report is usefull
only if you have non-ASCII characters somewhere for the tested option.  Select
the lines according to your tests. Remove each not having Unicode characters in
the **Tests on Unicode** section).

Please, keep the syntax for better Github formatting.

***

	### Positive feedback

	* **Test frequency**: (or approximate number of syncs)
	* **OfflineIMAP version**
	* Output of **`offlineimap --info`** (can be sent by mail to me directly with
		github issue reference/number for confidentiality).


	### Tests on Unicode

	* Downloaded mails
	* Uploaded mails
	* Mbnames
	* Folders filtering
	* Folders includes
	* Folders idle
	* Nametrans
	* Labels
	* Filter Headers
	* Paths
	* Commands (preauthtunnel, transporttunnel)

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
