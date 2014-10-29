TomcatMongoRealm
================

A MongoDB Security Realm for Tomcat

Build it as a jar. Copy the TomcatMongoRealm jar into theTomcat libs folder. Note also add the MongoDB Java driver to the Tomcat libs folder. Then just add: 

<pre>
&lt;Realm 
		className="org.geoffhayward.login.TomcatMongoRealm"
		digest="SHA-256"
		[...]
/&gt;
</pre>

to the context.xml of your Java Web application.
