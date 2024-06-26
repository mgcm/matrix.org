+++
title = "Synapse 0.4.2 released!"
path = "/blog/2014/10/31/synapse-0-4-2-released"

[taxonomies]
author = ["Matthew Hodgson"]
category = ["General"]
+++

Hi all,

There's been loads of work going on in various branches on Synapse (<a href="https://github.com/matrix-org/synapse/tree/federation_authorization">federation_authorization</a> and <a href="https://github.com/matrix-org/synapse/tree/event_signing">event_signing</a>) as we land the final features needed for Synapse to be used in production as a Matrix reference server.  Meanwhile the iOS demo client and SDK has been coming on leaps and bounds too over at <a href="https://github.com/matrix-org/matrix-ios-sdk">https://github.com/matrix-org/matrix-ios-sdk</a>.

However, stuff has also been happening on the main Synapse development branch too, and we've just released 0.4.2 onto master for lots of various goodies - see release notes below.

Please upgrade your homeservers and play with the new client - the new JSON viewing/editing features are particularly useful and interesting for powerusers and developers!

Matthew
<pre>
Changes in synapse 0.4.2 (2014-10-31)
=====================================

Homeserver:

 * Fix bugs where we did not notify users of correct presence updates.
 * Fix bug where we did not handle sub second event stream timeouts.

Webclient:

 * Add ability to click on messages to see JSON.
 * Add ability to redact messages.
 * Add ability to view and edit all room state JSON.
 * Handle incoming redactions.
 * Improve feedback on errors.
 * Fix bugs in mobile CSS.
 * Fix bugs with desktop notifications.

</pre>
