TomcatMongoRealm
================

A MongoDB Security Realm for Tomcat

Build it as a jar. Copy the TomcatMongoRealm jar into theTomcat libs folder. Note also add the MongoDB Java driver to the Tomcat libs folder. Then just add: 

<pre>
&lt;Realm 
	className="eu.geoffhayward.login.TomcatMongoRealm"
	digest="SHA-256"
	dbName="site-configuration"
	dbCollection="users"
	userUsername="username"
	userPassword="password"
	userRoles="roles"
/&gt;
</pre>

to the context.xml of your Java Web application.

<pre>
// Example document
{
    "_id" : ObjectId("5448f0e8b49162f09826f5f3"),
    "username" : "Geoff",
    "password" : "9f86d081884c7d659a2feaa0c55ad015a3bf4f1b2b0b822cd15d6c15b0f00a08", // test
    "roles" : [ 
        "editor", 
        "admin", 
        "siteadmin"
    ]
}
</pre>
