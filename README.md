# pwned
Interact with the pwned database

    pwned 1.2  - Alessandro Forghieri <alf@orion.it>
    SYNOPSYS:
       Verify that a password is not in the pwned database


    USAGE:
     pwned [-d] [-v] [-l logfile] pwd1 pwd2 ...
     pwned [flags] < pwdfile
	
	        -d   debug (repeat for ( increased verbosity)
                -v   verbose
                -l   logfile
                -q   be very quiet
   
	Checks passwords against the pwned database.

    EXAMPLES:
        # pwned -q Alessandro || echo 'You've been pwned'
        You've been pwned

        # pwned qwerty
        Fri Jan 18 11:31:09 2019 - ERROR - pwned - 160 - main::unsafe - PWNED! qwerty has been pwned 3810555 times.

        # pwned quarantaquattrogattiinfilaperseicolresto di due
        Fri Jan 18 11:33:57 2019 - INFO - pwned - 160 - main::unsafe - NOT PWNED! quarantaquattrogattiinfilaperseicolresto does not appear in the pwned database
        Fri Jan 18 11:33:57 2019 - ERROR - pwned - 160 - main::unsafe - PWNED! di has been pwned 2250 times.
        Fri Jan 18 11:33:57 2019 - ERROR - pwned - 160 - main::unsafe - PWNED! due has been pwned 605 times.

        # pwned < pwdlist
        ...

        See also:
        https://haveibeenpwned.com/Passwords   
