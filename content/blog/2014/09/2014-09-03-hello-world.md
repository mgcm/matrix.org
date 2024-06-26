+++
title = "Hello world"
path = "/blog/2014/09/03/hello-world"

[taxonomies]
author = ["Matthew Hodgson"]
category = ["General"]
+++

I'm Matthew, and I'm responsible for the techie side of what we're up to with Matrix.

Matrix is the result of a lot of work my team's done over the last 10 years or so (first at <a href="http://www.mxtelecom.com">MX Telecom</a>, then <a href="http://www.openmarket.com">OpenMarket</a>, and then <a href="http://www.amdocs.com/UnifiedCommunications">Amdocs</a>) in developing next-generation IP communication solutions.  First we started with an <a href="http://www.asterisk.org">Asterisk</a>-based platform running basic PSTN IVR services, and then shifted to an in-house IAX-based IVR platform built in Java, and then added circuit-switched (<a href="http://en.wikipedia.org/wiki/3G-324M">3G-324M</a>) video calling, then switched to SIP/RTP, C++ and a massively-distributed softswitch architecture affectionately called 'The Next Generation'.  Then the iPhone and Android came along, and we realised we didn't have to be constrained by built-in phone capabilities and ported our whole C++ SIP/RTP VoIP stack over to iOS/Android and got writing Video/VoIP calling apps.  This evolved to developing full-blown unified communication apps (e.g. <a href="http://www.blah.com">Blah</a>), using XMPP at first for messaging before switching to our own HTTP-based messaging APIs.

Somewhere along the way it became painfully obvious that VoIP and IM hasn't really evolved as well as the rest of the internet.  Back when SIP/RTP first emerged, it simply wasn't mature enough to work on the open internet as well as HTTP or SMTP or even FTP - it needed STUN, ICE, TURN, Opus and many other refinements to be really usable in the wild.  And similarly XMPP hasn't taken over the world quite as much as we once hoped.  Meanwhile, many folks went and built their own proprietary walled-garden solutions (be it Skype, FaceTime, Viber, WhatsApp, or even our own efforts) and we've ended up in the current horrible situation where our online communication is fragmented across hundreds of isolated apps and websites.  It's like a world where email was never unified, and half the world is still stuck on Compuserve.  And it's counter to the whole ethos of the internet as an open platform for collaboration and communication.

We decided that we want to fix this and so we have built and published a new open standard, together with open source (ASLv2) reference server (Python/Twisted) and client (JS/Angular, Python, Perl) codebases, and so provide new building blocks that can be used to build truly interoperable federated IM and VoIP functionality.  We consider this effectively an investment in the industry: by creating a strictly non-profit initiative like Matrix, we both make the world a better place for end users - as well as creating new business opportunities (both opensource and commercial) for the telecoms industry as a whole.

The standard and code are all brand new and very much still in creation at this point, but we're releasing it early to get as much feedback and input from the community as early on as we possibly can. Right now our focus is on fully decentralised federated group messaging, but VoIP and identity management is coming together well too.  You can think of it as "making VoIP/IM as interoperable and flexible as email", or perhaps "the missing signalling layer for WebRTC", "XMPP for an HTTP world", or “what would happen if IRC, XMPP, SIP, SMTP, IMAP and NNTP had kids?” Here are some reasons we think that you should use Matrix:
<ul>
	<li><span style="font-size: 1rem; line-height: 1.714285714;">Simple pragmatic RESTful HTTP/JSON APIs.  No more XMPP or SIP stacks and wrestling XML streams or torture-testing SIP parsers.</span>
</li>
	<li><span style="font-size: 1rem; line-height: 1.714285714;">No single points of control for channels of communication (unless you really want it for moderation or similar). Room state for a room is synchronised with eventual consistency over all participating Matrix servers - no single server controls the room.</span>
</li>
	<li><span style="font-size: 1rem; line-height: 1.714285714;">No more netsplits - history re-heals itself if the matrix fractures</span>
</li>
	<li><span style="font-size: 1rem; line-height: 1.714285714;">All communication is group by default: 1:1 chat is just a subset of group chat.</span>
</li>
	<li><span style="font-size: 1rem; line-height: 1.714285714;">Multi-device aware: all state is stored and synchronised in realtime across all devices, and away-state and notifications are aware of multiple devices.</span>
</li>
	<li><span style="font-size: 1rem; line-height: 1.714285714;">Uses arbitrary 3rd party identifiers - doesn't rely on JIDs or SIP URIs for identity.</span>
</li>
	<li><span style="font-size: 1rem; line-height: 1.714285714;">Share the same simple HTTP signalling channel for messaging and VoIP</span>
</li>
	<li><span style="font-size: 1rem; line-height: 1.714285714;">Support more efficient transports if you want (e.g. low-bandwidth/low-roundtrip sync on mobile)</span>
</li>
	<li><span style="font-size: 1rem; line-height: 1.714285714;">Built for mobile - e.g. support push notification and low-bandwidth/low-latency client-server transports if needed (in progress)</span>
</li>
	<li><span style="font-size: 1rem; line-height: 1.714285714;">TLS (HTTPS) by default, either with self-signed certs with published public keys or proper SSL CA signed certs (in progress)</span>
</li>
	<li><span style="font-size: 1rem; line-height: 1.714285714;">End-to-end PKI encryption (in progress)</span>
</li>
	<li><span style="font-size: 1rem; line-height: 1.714285714;">Trusted federation of public identity servers available for publishing your PKI public keys and tracking your validated 3rd party IDs</span>
</li>
</ul>
If this sounds good to you, then please take a look at the <a href="http://matrix.org/docs/spec">spec</a>, or our <a href="http://matrix.org/docs/howtos">tutorials</a>, or jump straight into playing with the <a href="http://matrix.org/docs/api">APIs</a>, or try running your own Matrix homeserver, or sign up to our <a href="http://matrix.org/mailman">mailing lists</a> - and whatever else, come swing by <a href="http://matrix.org/alpha">#matrix:matrix.org</a> and say hi!

<a href="http://xkcd.com/927/"><img class="aligncenter" style="box-shadow: 0 0 0 ! important" src="http://imgs.xkcd.com/comics/standards.png" alt="" /></a>
