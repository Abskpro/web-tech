## How can you define event Handler? Write a javascript to demonstrate event handling?

    In javascript events are something that happens in the browser in a particular instance of time.
    Event handler are the those functions that handle the events in the browser dom.Events like onsubmit
    onkeypress,onKeydown,onmouseover,onsubmit etc cause an event handler to execute. Event handler executes
    only when an event occurs in the browser dom.
    Eg of event handling
        <button onClick="alert("hello world")">Click me</button>
    In the above example when the button it is clicked is fires an event handler that executes the code
    that alerts hello world to the browser screen.

## Discuss the use of session with suitable example

    A Sessions can be defined as a server-side storage of information that is desired to persist throughtout
    the users interaction with the web site or web application. This session id is passed to the web server
    every time the browser makes an http request.

    uses of sessions
    1. Session increase the performance of a website by temporarily storing data in server.
    2. It reduce server processiong
    3. Session remove the storing data to the database.

## Shotnotes on SMTP

    SMTP  is a tcp/ip protocol used in sending and receiving email. However, since it is limited in
    its ability to queue message at the receiveing end, it is usually used with one of two other
    protocols, POP3(Post office protocol) or IMAP (internet message access protocol), that let the
    user save message in a server mailbox and download them periodically from the server.
    SMTP is generally used to send message from a mail client to a mail server. SMTP uses port 25.

## XQuery
    XQuery is a specification for a query language thatr allowes a user or programmer to extract 
    information from an Extensible Markup Language file or any collection of data that can be XML.
    The syntax is intended to be easy to understand and use. Using XQuery, it is possible to view a
    relational database table as an XML document.
    
    Benifits of XQuery 
    * Using XQuery, both hierarchical and tabular data can be retrieved.
    * It can be directlhy used to query webpages.
    * It can be directly used to build webpages.
    * It can be used to transform xml document.

## FTP
    File transfer protocol is standard internet protocols for transmitting files between computers 
    on the internet over TCP/IP connections. FTP is a client-server protocol where a client will 
    ask for a file, and a local or remote server will provide it.
    FTP is a client-server protocol that relies on two communications channels between client and
    server : a command channel for controlling the conversation and data channel for transmitting 
    file content. Client initiate conversation with servers by requesting to download a file . 
    Using FTP a client initiate conversations with servers by requesting a download file.
    
    
## What are the advantages of using XML? Explain the rules of writing xml
    Advantages of xml are 
    1. XML uses human language. So xml is readable and understandable.
    2. Xml is compatible with java and 100% portable.
    3. xml is extendable ie we can create our own tag
    4. It seperates content from presentation
    
    Rules of writing xml
    1. All xml must have a root element.
    2. all tags must be closed
    3. All tag must be properly nested.
    4. Tag names are case sensitive.
    5. HTML tags should be avoided
    

## DTD
    Dtd is an approach for defining the structure of xml document. A DTD defines the document 
    structure of XML document. A Dtd defines the document structure with a list of legal elements
    and attributes.
    Dtd is a set of markup declarations that define a document type for family markup languages
    (SGML,XML,HTML)
    We use DTD beacuse with a DTD each of your xml files can carry a description of its own format
    With a DTD independent groups of peaople can agree to use a standard DTD for interchanging data.
    
    syntax: <!DOCTYPE element DTD identifier [ declaration1 declaration2 ]>
    
    Internal dtd syntax
        <!DOCTYPE root-element[element-declaration]>
    External DTD syntax
        <!DOCTYPE root-element SYSTEM "file-name">

    Difference between external and internal dtd
    Internal dtd
    
    <?xml version="1.0" encoding="UTF-8">
    <!DOCTYPE Address[
    <!Element Address(Name,Company,phone)
    <!Element Name(#PCDATA)>
    <!Element Company(#PCDATA)
    ]>

    External dtd
    <!DOCTYPE Address SYSTEM "Add.dtd">
    
---------------------------------------------------------------------
    
## What are anti overload techniues in web server?
    At time webserver can be overloaded beacause of 
    1. too much web traffic
    2. Distributed Denial of Service attacks
    3. Computer worms
    4. Hardware and software failures
    5. Client request are served more slowly and the number of connections icreases so much that server
        limits are reached
    
    To partially overcome load limits we use techniuques like
    1. Managing network traffic by using firewalls
    2. Redirect or reqrite request having bad http patterns
    3. Deploying web cahe techniques
    4. Add more hardware resource
    5. Use many web server
    6. Using load balancer to redirect traffic to different servers
    
## What are cookies? Explain with an example
    A cookie is the term given to describe a type of message that is given to a web browser by a web
    server. The main purpose of a cookie is to idenify user or to save site login information
    There are two types of cookies 
    1. Session cookie 
       It is the type of cookie that is erased when browser is closed ie the cookie is saved temporarily
       
    2. Persistent cookie
        It is the type of cookie that is permanently stored in browser until the user decides to remove it.
        
    A cookie have six paramenter that can be passed to them:
    1. name of the cookie
    2. value of the cookie
    3. Expiration date of the cookie
    4. the path that cookie is valid for
    5. the domain the cookie is valid for
    6. The need for a secure connection
    
    Javascript using cookies
    
    function setCookie(cname,cvalue,exdays){
        var d = new Date();
        d.setTime(d.getTime() + (exdays*24*60*60*1000));
        var expires = "expires=" + d.toGMTString();
        document.cookie = cname + "=" + cvalue+ ";" +expires+ ";path=/";
    }
    
    function getCookie(cname){
        var name=cname+ "=";
         var decodedCookie = decodeURIComponent(document.cookie);
           var ca = decodedCookie.split(';');
           for(var i = 0; i < ca.length; i++) {
               var c = ca[i];
               while (c.charAt(0) == ' ') {
                     c = c.substring(1);
               }
               if (c.indexOf(name) == 0) {
                     return c.substring(name.length, c.length);
               }
           }
             return "";
    }


    function checkCookie() {

        var user=getCookie("username");
        if (user != "") {
            alert("Welcome again " + user);
        } else {
            user = prompt("Please enter your name:","");
            if (user != "" && user != null) {
              setCookie("username", user, 30);
            }
        }
    }

==============================================
# Web Server
    Web server is software or hardware that uses HTTP and other protocols to respond to
    client request made over the www. Web server software controls how a user accesses
    hosted files. It is accessed through the domain name of websites and ensures the
    delivery of the site's content to the requesting user. As a hardware a web server 
    is a computer that hold's web server software and other files related to a website,
    such as HTML documnets, images and js

# Domain vs DNS
    Domain
        An identification string that defines a realm of administrative autonomy or control
        within internet. Help user to identify a specific website
    DNS
        A hierarachical decentralized naming system for computer services and other resource
        connected to internet. COnverts the domain name to ip address
