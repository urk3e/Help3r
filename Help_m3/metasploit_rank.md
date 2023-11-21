Excellent : The exploit will never crash the service. This is the case for SQLI, CMD 
exec, RFI, LFI, etc. No typical memory corruption exploits should be fiven this ranking 
unless there are extraordinary circumstances (WMF Escape()).

Great : The exploit has a default target AND either auto-detects the appropriate target 
or uses an application-specific return address AFTER a version check

Good : The exploit has a default target and it is the "common case" for this type of 
software (English, Windows7 for desktop app, 2012 for server, etc).

Normal : The exploit is otherwise reliable, but depends in specific version and cant 
(or doesnt) reliably autodetect.

Average : The exploit is generally unreliable or difficult to exploit

Low : The exploit is nearly impossible to exploit (under 50% succes rate) for common 
platforms.

Manual : The exploit is unstable or difficult to exploit and basically a DoS. This 
ranking is also used when the module has no use unless specifically configured by the 
user (e.g.: exploit/unix/webapp/php_eval).
