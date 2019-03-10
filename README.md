# ssoapiclient
SonicWall SSO API client

Special thanks to John-Michael Denton and Ian Puleston.
Their help was instrumental in getting the security layer figured out.

This script can log users in and out of SonicOS using the 3rd-Party Single-Sign-On API feature.

While this script works, it is unfinished. It currently doesn't support certificates

#Usage:
ssoapiclient.py [-h] [-u USER_NAME] [-d USER_DOMAIN]
                         [-r LOGOUT_REASON]
                         user_action user_ip

SSO API Client integrates with the 3rd-Party Single-Sign-On API feature in
SonicOS. That feature is not to be configured with the SonicOS API, which this
client does not support.

positional arguments:

user_action       "add" to send login, "delete" for log out, and "options"
                    for parameters.

user_ip           The host IP to login


optional arguments:

-h, --help        show this help message and exit
  
  -u USER_NAME      User name to login. Required for logins, optional for
                    logout.
  
  -d USER_DOMAIN    User's FQDN or NETBIOS domain name. Optional. SonicOS will
                    still check LDAP if enabled.
  
  -r LOGOUT_REASON  Reason for logout. Optional. SonicOS uses this for logging
                    only.
