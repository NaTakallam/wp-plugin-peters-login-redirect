### Peter's Login Redirect
#### By Peter Keung
Define a set of redirect rules for specific users, users with specific roles, users with specific capabilities, and a blanket rule for all other users. Also, set a redirect URL for post-registration. This is all managed in Settings > Login/logout redirects.

You can use the syntax [variable]username[/variable] in your URLs so that the system will build a dynamic URL upon each login, replacing that text with the user’s username. In addition to username, there is “userslug”, “homeurl”, “siteurl”, “postid-23”, “http_referer” and you can also add your own custom URL “variables”. See Other Notes / How to Extend for documentation.

You can add your own code logic before and between any of the plugin’s normal redirect checks if needed. See Other Notes / How to Extend for documentation. Some examples include: redirecting the user based on their IP address; and redirect users to a special page on first login.

This plugin also includes a function rul_register that acts the same as the wp_register function you see in templates (typically producing the Register or Site Admin links in the sidebar), except that it will return the custom defined admin address. rul_register takes three parameters: the “before” code (by default “<li>”), the “after” code (by default “</li>”), and whether to echo or return the result (default is true and thus echo)