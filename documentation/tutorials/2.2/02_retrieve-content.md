As we mentioned in the [introduction
paper](/technical-resources/restlet-framework/guide/2.2/introduction/overview), the Restlet framework is at the
same time a client and a server framework. For example, Restlet can
easily work with remote resources using its HTTP client connector. A
connector in REST is a software element that enables the communication
between components, typically by implementing one side of a network
protocol. Restlet provides several implementations of client connectors
based on existing open-source projects. The
[connectors](/technical-resources/restlet-framework/guide/2.2/core/base/connectors) section lists all
available client and server connectors and explain how to use and
configure them.

Here we will get the representation of an existing resource and output
it in the JVM console:

<pre class="language-java"><code class="language-java">// Outputting the content of a Web page
new ClientResource("http://restlet.com").get().write(System.out);
</code></pre>

Note that the example above uses a simplified way to issue calls via the
ClientResource class. If you need multi-threading or more control it is
still possible to manipulate use the Client connector class or the
Request objects directly. The example below how to set some preferences
in your client call, like a referrer URI. It could also be the languages
and media types you prefer to receive as a response:

<pre class="language-java"><code class="language-java">// Create the client resource
ClientResource resource = new ClientResource("http://restlet.com");

// Customize the referrer property
resource.setReferrerRef("http://www.mysite.org");

// Write the response entity on the console
resource.get().write(System.out);
</code></pre>
